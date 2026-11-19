## 1. Arquitectura y flujos funcionales

Cómo funciona la plataforma web de AIComp, en tres diagramas: qué piezas tiene, qué camino sigue el cliente y cómo decide el configurador. Cuadra con los módulos (`docs/sprint-2/01-modules.md`) y los recursos materiales (`docs/sprint-2/03-material-resources.md`) del Sprint 2.

### 1.1 Arquitectura

```mermaid
flowchart LR
    U["Navegador del usuario<br/>visitante, cliente o administrador"]

    subgraph CF["Cloudflare Pages"]
        FE["Frontend<br/>React + Tailwind CSS"]
    end

    subgraph LC["Laravel Cloud"]
        API["API REST Laravel<br/>reglas del configurador y precios<br/>presupuestos y pedidos<br/>acceso y permisos por rol"]
        PAY["Pago simulado<br/>el administrador marca<br/>el pedido como pagado"]
    end

    subgraph SB["Supabase"]
        DB[("PostgreSQL<br/>solo como base de datos")]
    end

    subgraph DEV["Solo en desarrollo"]
        MP["Mailpit"]
    end

    U -->|HTTPS| FE
    FE -->|"HTTPS / JSON"| API
    API -->|consultas SQL| DB
    API -->|"correos de registro y de pedido"| MP
```

El usuario solo habla con el frontend, que pinta las pantallas y no decide nada: todo lo pregunta a la API en HTTPS/JSON. La API concentra la lógica (las reglas del configurador, los precios, los presupuestos, los pedidos y el acceso por rol), así que el resultado no se puede manipular desde el navegador. Supabase se usa solo como base de datos PostgreSQL; el acceso lo gestiona Laravel. No hay pasarela de pago ni correo real: el pago se simula y los correos se recogen en Mailpit durante el desarrollo.

### 1.2 Camino del cliente

```mermaid
flowchart TD
    A["Página de sector<br/>despacho, gestoría, clínica u otro"] --> B["Configurador<br/>con el sector ya marcado"]
    B --> C["Presupuesto<br/>equipo + puesta en marcha + cuota"]
    C --> K["Carrito"]
    K --> L{"¿Ha iniciado sesión?<br/>Hace falta para guardar el<br/>presupuesto o confirmar el pedido"}
    L -->|No| REG["Registro o acceso<br/>el visitante pasa a cliente"]
    REG --> O
    L -->|Sí| O["Pedido<br/>pendiente de pago<br/>+ correo de confirmación"]
    O --> AC["Área de cliente<br/>pedidos, presupuestos guardados,<br/>servicios y estado"]

    subgraph ADM["Administrador, desde el panel"]
        P1["Marca el pedido como pagado"]
        P2["Mueve el estado<br/>recibido → en montaje → enviado → entregado"]
    end

    O -.-> P1
    O -.-> P2
    P1 -.-> AC
    P2 -.-> AC
```

El visitante entra por la página de su sector, responde al configurador y ve su presupuesto sin registrarse. Para guardar ese presupuesto o confirmar el pedido tiene que registrarse o iniciar sesión, y desde ese momento es cliente. El pedido nace pendiente de pago y el cliente recibe un correo de confirmación. El administrador, desde el panel, lo marca como pagado cuando llega la transferencia y mueve su estado (recibido, en montaje, enviado, entregado). El cliente sigue todo desde su área.

### 1.3 Configurador

```mermaid
flowchart LR
    subgraph FE["Frontend: tres preguntas"]
        Q1["Sector"]
        Q2["Número de usuarios"]
        Q3["Uso<br/>p. ej. consultar documentos,<br/>redactar o transcribir"]
    end

    subgraph API["API: reglas sin IA"]
        R["Reglas sobre el catálogo"]
        E["Equipo más económico que cumple<br/>+ por qué se ha elegido"]
        S["Puesta en marcha"]
        M["Cuota de mantenimiento"]
    end

    CAT[("Catálogo y reglas<br/>los mantiene el administrador")]

    Q1 --> R
    Q2 --> R
    Q3 --> R
    CAT --> R
    R --> E
    R --> S
    R --> M
    E --> P["Presupuesto"]
    S --> P
    M --> P
```

El configurador solo pide tres datos: sector, número de usuarios y uso. La API aplica reglas deterministas sobre el catálogo, sin IA, y devuelve el equipo más económico que cumple, con una explicación corta de por qué se ha elegido. A ese equipo le suma la puesta en marcha y la cuota mensual de mantenimiento, y los tres juntos forman el presupuesto. Como el catálogo y las reglas están en la base de datos, el administrador puede ajustarlos sin tocar código.

---

Diagramas de detalle (base de datos, API) en la fase de desarrollo.
