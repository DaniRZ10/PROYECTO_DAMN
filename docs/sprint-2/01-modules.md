# Sprint 2 · Módulos de la plataforma y su integración

> **Issue #29** · Responsable: Manuel Jesús Jiménez Romero · Entregable: 1 slide en la presentación del Sprint 2.
>
> Este documento fija **qué partes tiene la plataforma web de AIComp, cuáles entran en el MVP y cómo encajan entre sí**, para que el equipo y el Product Owner compartan el mismo alcance antes de empezar a programar.
>
> El diseño (diagramas, esquemas, prototipos y wireframes) queda **aplazado al Sprint 3** por indicación del Product Owner. Por eso aquí la integración se explica en texto y tablas, sin diagramas.

## 1. Módulos de la plataforma

Cada módulo se clasifica en uno de estos tres estados:

| Estado | Significado |
| --- | --- |
| **MVP** | Entra en el producto mínimo y se construye de verdad. |
| **Simulado** | Entra en el MVP, pero con un comportamiento controlado y sin integración real con terceros. |
| **Después** | Fuera del MVP. Se cuenta como evolución del producto, no se construye. |

| # | Módulo | Qué hace | Estado |
| --- | --- | --- | --- |
| 1 | **Páginas públicas y contenido por sector** | Portada, una página por sector (despachos, gestorías, clínicas), "cómo funciona" y contacto. Es donde se explica el diferencial de AIComp y la puerta de entrada al configurador. | MVP |
| 2 | **Catálogo de equipos** | Listado y ficha de los equipos por nivel, con datos de ejemplo: componentes, qué modelos de IA admite, servicios asociados y precio orientativo. | MVP |
| 3 | **Configurador por sector y caso de uso** | Cuestionario con reglas sobre el catálogo que recomienda un equipo y sus servicios. Pieza clave del producto (apartado 3). | MVP |
| 4 | **Cuentas y acceso** | Registro y acceso de la empresa cliente, datos de la empresa y permisos según el rol. | MVP |
| 5 | **Carrito, presupuesto y pedido** | Guarda la recomendación del configurador, genera el presupuesto y lo convierte en pedido. | MVP |
| 6 | **Servicios y cuota de mantenimiento** | Muestra la puesta en marcha y la cuota de mantenimiento, y permite contratarlas junto al equipo. | MVP |
| 7 | **Área de cliente** | Pedidos, presupuestos guardados, servicios contratados y estado de cada pedido. | MVP |
| 8 | **Panel de administración** | Alta y edición del catálogo, mantenimiento de las reglas del configurador, y gestión de los pedidos y sus estados. | MVP |
| 9 | **Pago** | Presupuesto y transferencia: el pedido queda "pendiente de pago" y un administrador lo marca como pagado. Stripe en modo prueba queda como extra, fuera del MVP. | Simulado |
| 10 | **Avisos por correo** | Correo de registro y de confirmación de pedido, contra Mailpit en desarrollo. No sale ningún correo real. | Simulado |
| 11 | **Logística y plazos** | No hay stock: la ficha muestra un plazo de entrega estimado y un estado de pedido que mueve el administrador. | Simulado |
| 12 | **Demostración con documentos de ejemplo** | Probar un modelo con documentos propios desde la web. Se cuenta en la presentación, no se construye. | Después |
| 13 | **Correo real en producción** | Envío de correo con un proveedor real. | Después |
| 14 | **Varios idiomas** | La web en más de un idioma. | Después |
| 15 | **App móvil** | Aplicación nativa. | Después |

### Ajustes sobre el MVP propuesto, y por qué

- **Se añaden dos módulos propios** que en la propuesta estaban implícitos: *Cuentas y acceso* (sin acceso no existen ni el área de cliente ni el panel de administración) y *Páginas públicas y contenido por sector* (el diferencial por sector no se ve en ninguna parte si no hay páginas que lo expliquen). Separarlos permite estimar sus horas en el presupuesto (#32).
- **Se separan del módulo de pedido** *Pago*, *Avisos por correo* y *Logística y plazos*, porque entran en el MVP pero **simulados**. Conviene que figuren así para que el PO no espere integraciones reales.
- **El resto del MVP propuesto en la actualización v2.3 se mantiene sin cambios.**

## 2. Roles de usuario

| Rol | Qué puede hacer | Qué no puede hacer |
| --- | --- | --- |
| **Visitante** | Ver las páginas y el catálogo, usar el configurador y ver el presupuesto resultante. Registrarse. | Guardar el presupuesto ni confirmar un pedido: para eso hay que registrarse. |
| **Cliente (empresa)** | Todo lo del visitante, y además guardar presupuestos, confirmar pedidos, contratar la puesta en marcha y el mantenimiento, consultar sus pedidos y su estado, y editar los datos de su empresa. | Ver datos de otros clientes, tocar el catálogo ni cambiar el estado de un pedido. |
| **Administrador (AIComp)** | Mantener el catálogo, las reglas del configurador y los servicios y cuotas. Ver los pedidos de todos los clientes, marcarlos como pagados y mover su estado. | Comprar: no es un rol de cliente. |

**Alcance del MVP:** un solo usuario por empresa cliente. Varios usuarios de la misma empresa, con permisos distintos, queda para después del MVP.

## 3. El configurador por sector y caso de uso

Es la pieza clave porque es donde se ve el diferencial de AIComp: una solución por sector, se compra un resultado y no un equipo, y la recomendación es independiente del hardware.

**Qué pregunta** (tres datos, nada más):

1. **Sector**: despacho, gestoría, clínica u "otro".
2. **Número de usuarios** que van a usar la IA.
3. **Uso**: a qué se va a dedicar (por ejemplo, consultar documentos propios, redactar o transcribir).

**Qué devuelve**

- **Un equipo del catálogo**, con el nivel que corresponde a esas respuestas y una explicación corta de por qué se ha elegido ese y no otro.
- **La puesta en marcha**: instalación del equipo y modelo de IA abierto ya preparado para ese uso.
- **La cuota de mantenimiento** mensual, que mantiene los modelos al día.
- Los tres juntos como **presupuesto**: el visitante lo ve y el cliente lo guarda o lo pasa al carrito.

**Qué queda fuera**

- **No lleva IA dentro.** Son reglas deterministas sobre el catálogo, no un modelo que decide. Así el resultado es explicable y el administrador lo puede ajustar.
- **No dimensiona ni mide** el rendimiento real del equipo: no hay pruebas de carga ni cálculo técnico fino.
- **No personaliza el modelo** con los documentos del cliente: eso es un servicio, no una función de la web.
- **No recomienda nada fuera del catálogo** ni calcula precios dinámicos: los precios son datos de ejemplo del catálogo.
- **No pide datos sensibles** ni permite subir documentos.

## 4. Cómo se integran los módulos

### 4.1 Qué módulo usa a cuál

| Módulo | Usa | Para qué |
| --- | --- | --- |
| Páginas por sector | Configurador | Llevar al visitante al cuestionario con su sector ya marcado. |
| Configurador | Catálogo | Leer los equipos y sus niveles para aplicar las reglas. |
| Configurador | Servicios y cuota | Añadir la puesta en marcha y el mantenimiento a la recomendación. |
| Configurador | Carrito y presupuesto | Crear el presupuesto con el equipo y los servicios recomendados. |
| Carrito y presupuesto | Cuentas y acceso | Exigir acceso antes de confirmar el pedido. |
| Pedido | Pago (simulado) | Registrar el pedido como pendiente de pago. |
| Pedido | Avisos por correo | Confirmar el pedido al cliente. |
| Área de cliente | Pedido, Servicios | Mostrar pedidos, estados y servicios contratados. |
| Panel de administración | Catálogo, Reglas del configurador, Pedido | Mantener los datos y mover los estados de los pedidos. |

El camino completo del MVP es: **página de sector → configurador → presupuesto → carrito → pedido (pago simulado) → área de cliente**, con el panel de administración detrás manteniendo el catálogo y moviendo los pedidos.

### 4.2 Reparto entre frontend, API y base de datos

| Capa | Tecnología | De qué se encarga |
| --- | --- | --- |
| **Frontend** | React + Tailwind CSS (Cloudflare Pages) | Pantallas, el cuestionario del configurador, el carrito en el navegador y el área de cliente. No decide nada por su cuenta: pregunta a la API. |
| **API** | Laravel, API REST (Laravel Cloud) | Reglas del configurador, acceso y permisos por rol, precios y presupuestos, pedidos y sus estados, y el panel de administración. |
| **Base de datos** | PostgreSQL en Supabase, solo como base de datos | Equipos del catálogo, reglas del configurador, empresas y usuarios, presupuestos, pedidos y servicios contratados. |

Dos reglas de reparto:

- **Las reglas del configurador y los precios viven en la API**, nunca en el frontend. Así el resultado no se puede manipular desde el navegador y el administrador puede cambiarlos sin tocar código.
- **El acceso lo gestiona Laravel**, no Supabase Auth: de Supabase se usa solo la base de datos.

### 4.3 Qué se simula

| Qué | Cómo se simula |
| --- | --- |
| **Pago** | Presupuesto y transferencia. El pedido queda "pendiente de pago" y el administrador lo marca pagado a mano. Stripe en modo prueba, como extra fuera del MVP. |
| **Envíos** | No hay transportista ni seguimiento real: solo un estado y una fecha estimada que mueve el administrador. |
| **Estado del pedido** | Estados fijos (recibido, en montaje, enviado, entregado) que cambia el administrador desde el panel. |
| **Plazo de entrega en lugar de stock** | Los equipos se montan bajo pedido, así que la ficha muestra un plazo de entrega estimado, no unidades disponibles. Es coherente con la viabilidad: AIComp no vive del stock. |
| **Correo** | Mailpit en desarrollo. El correo real queda fuera del MVP. |
| **Datos del catálogo** | Equipos, componentes y precios de ejemplo, partiendo de las cifras estimadas de `docs/sprint-1/04-feasibility.md`. |

## 5. Para después del MVP

Con el MVP se recorre entero el camino del cliente —página de sector, configurador, presupuesto, pedido y área de cliente— con el pago, los envíos y el correo simulados; para después del MVP quedan la demostración con documentos de ejemplo, el pago y el correo reales, varios usuarios por empresa, los idiomas y la app móvil.

---

**Pendiente de validar con el PO en la revisión del 12/11:** la lista de sectores del configurador, que el configurador no lleve IA dentro (son reglas) y que en el MVP haya un solo usuario por empresa cliente.
