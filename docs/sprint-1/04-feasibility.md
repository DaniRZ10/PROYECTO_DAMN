## 4. Viabilidad técnica

Viabilidad de la **plataforma web** de AIComp (tienda online, configurador por caso de uso y área de cliente), no del montaje de los equipos.

### 1. Recursos tecnológicos

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Frontend: React + Tailwind CSS | Stack previsto por sugerencia del profesor; gratuito y muy documentado | Ninguno lo hemos usado en un proyecto real |
| Backend: Laravel (API REST) | Stack previsto; base de PHP | Aprender Laravel y conectarlo con React (CORS, autenticación por token) |
| Base de datos | SQL y MySQL de primero | **Pendiente de decidir** en el Sprint 2 (MySQL o PostgreSQL, ambas compatibles con Laravel [1]); depende del modelo de datos |
| Git, GitHub y GitHub Projects | Repositorio con ramas protegidas, PR revisadas y tablero Kanban funcionando | Conflictos al trabajar cuatro personas en paralelo |
| Herramientas | VS Code, Postman o Thunder Client, WhatsApp | Mismas versiones de PHP, Node y Composer en todos los equipos |

### 2. Materiales e infraestructura

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Entorno local | Portátiles propios | Instalación común (Laragon, XAMPP o Docker con Laravel Sail [2]) y un `.env.example` compartido |
| Entorno de pruebas | Nada todavía | Desplegar `develop` para enseñarlo en cada Sprint Review |
| Hosting | Nada contratado. **Propuesta, cambiable en el Sprint 2:** React en Vercel Hobby (gratis, uso no comercial) [3]; API y BD en Laravel Cloud Starter (5 $/mes, primer mes gratis) [4] | Límites de los planes (servidor que se suspende sin tráfico, BD pequeña) y que cambien. Alternativa: créditos del GitHub Student Developer Pack [5] |
| Dominio | Subdominio gratuito del hosting | Dominio propio opcional: el GitHub Student Developer Pack incluye uno durante un año [5]; no es imprescindible |
| Pasarela de pago | Stripe en modo prueba (*sandbox*): tarjetas ficticias y sin dinero real [6] | Integrar su API; nunca se cobra dinero real |
| Correo | Bandeja de pruebas (por ejemplo, Mailtrap) | Solo para confirmar registros y pedidos |

### 3. Competencias del equipo

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Lo que ya sabemos | HTML, CSS, JavaScript, PHP, SQL, Java y Git básico | Nivel desigual entre los miembros |
| Lo que hay que aprender | — | React (componentes, estado, rutas), Laravel (migraciones, Eloquent, API), Tailwind, Stripe y despliegue |
| Riesgo principal | Rotamos por todas las áreas | Aprender y producir a la vez: empezar con una prueba pequeña por tecnología |

### 4. Limitaciones

- **Tiempo:** sprints de una semana y pocas horas por persona, compaginadas con el resto de módulos. Propuesta de núcleo del MVP, pendiente de validar con el PO: catálogo, configurador, área de cliente, carrito, pedido y panel de administración básico.
- **Simulado:** pagos (Stripe en modo prueba), stock (cantidades ficticias editadas desde el panel), envíos (estado del pedido cambiado a mano, sin transportista) y catálogo (equipos y precios de referencia).
- **Fuera del proyecto (propuesta):** montaje físico, instalación real de modelos de IA, integración con mayoristas, facturación legal, app móvil y varios idiomas.

**Conclusión:** la plataforma es viable con herramientas gratuitas si acotamos el alcance y reservamos tiempo para aprender React y Laravel.

<sub>Fuentes (consultadas en octubre de 2026): [1] [Laravel: bases de datos](https://laravel.com/docs/13.x/database) · [2] [Laravel Sail](https://laravel.com/docs/13.x/sail) · [3] [Vercel: plan Hobby](https://vercel.com/docs/plans/hobby) · [4] [Laravel Cloud: precios](https://laravel.com/cloud/docs/pricing) · [5] [GitHub Student Developer Pack en 2026](https://capitalandcompute.net/blog/github-student-developer-pack-2026/) · [6] [Stripe: sandboxes](https://docs.stripe.com/sandboxes)</sub>
