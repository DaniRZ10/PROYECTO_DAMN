## 4. Viabilidad técnica

Viabilidad de la **plataforma web** de AIComp (tienda online, configurador por caso de uso y área de cliente), no del montaje de los equipos.

### 1. Recursos tecnológicos

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Frontend: React + Tailwind CSS | Stack previsto por sugerencia del profesor; gratuito y muy documentado | Ninguno lo hemos usado en un proyecto real |
| Backend: Laravel (API REST) | Stack previsto; base de PHP | Aprender Laravel y conectarlo con React (CORS, autenticación por token) |
| Base de datos: **PostgreSQL en Supabase** (decidido) | SQL y MySQL de primero; Supabase es gratis (500 MB y 2 proyectos) y Laravel se conecta como a cualquier PostgreSQL (Laravel, s. f.-a; Supabase, 2026) | Usarlo solo como base de datos (el login lo gestiona Laravel); el plan gratuito se pausa tras una semana sin uso (Fila, 2026); para desarrollar, mejor un PostgreSQL local por persona |
| Git, GitHub y GitHub Projects | Repositorio con ramas protegidas, PR revisadas y tablero Kanban funcionando | Conflictos al trabajar cuatro personas en paralelo |
| Herramientas | VS Code, Postman o Thunder Client, WhatsApp | Mismas versiones de PHP, Node y Composer en todos los equipos |

### 2. Materiales e infraestructura

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Entorno local | Portátiles propios. **Abierto:** XAMPP o Docker con Laravel Sail (Laravel, s. f.-b) | Elegir uno común y un `.env.example` compartido. Con XAMPP hay que activar `pdo_pgsql` para PostgreSQL. Repos fuera de OneDrive |
| Entorno de pruebas | Nada todavía | Desplegar `develop` para enseñarlo en cada Sprint Review |
| Hosting | Frontend React: **Cloudflare Pages o Vercel** (elegir uno; Vercel, 2026). API Laravel: **pendiente** | Ni Cloudflare ni Vercel ejecutan Laravel de forma normal: la API necesita un hosting con PHP (Laravel Cloud (Laravel, s. f.-c), un servicio con Docker o un VPS), a comparar en el Sprint 2. Créditos del GitHub Student Developer Pack (Capital & Compute, 2026) |
| Dominio | Subdominio gratuito del hosting | Dominio propio opcional: el GitHub Student Developer Pack incluye uno durante un año (Capital & Compute, 2026); no es imprescindible |
| Pagos | **Pendiente (Sprint 2).** Opciones: presupuesto y pago por transferencia, o Stripe en modo prueba con tarjetas ficticias (Stripe, s. f.) | Nunca se cobra dinero real |
| Correo | **Pendiente (Sprint 2):** correos automáticos de registro y pedidos | En desarrollo se capturan en una bandeja de pruebas (Mailtrap o Mailpit) |

### 3. Competencias del equipo

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Lo que ya sabemos | HTML, CSS, JavaScript, PHP, SQL, Java y Git básico | Nivel desigual entre los miembros |
| Lo que hay que aprender | — | React (componentes, estado, rutas), Laravel (migraciones, Eloquent, API), Tailwind, PostgreSQL y despliegue |
| Riesgo principal | Rotamos por todas las áreas | Aprender y producir a la vez: empezar con una prueba pequeña por tecnología |

### 4. Limitaciones

- **Tiempo:** sprints de una semana y pocas horas por persona, compaginadas con el resto de módulos. Propuesta de núcleo del MVP, pendiente de validar con el PO: catálogo, configurador, área de cliente, carrito, pedido y panel de administración básico.
- **Qué se simula y qué queda fuera: pendiente de debatir en el Sprint 2.** Propuesta inicial: simular pagos, stock (o mostrar plazo de entrega, ya que los equipos se montan a medida), envíos y catálogo; dejar fuera el montaje físico, la instalación real de modelos de IA, la integración con mayoristas, la facturación legal, la app móvil y los varios idiomas.
- **También pendiente:** cómo se venden los servicios (instalación, personalización, mantenimiento), los roles de usuario y el alcance del configurador.

**Conclusión:** la plataforma es viable con herramientas gratuitas si acotamos el alcance y reservamos tiempo para aprender React y Laravel.

### Referencias

- Capital & Compute. (2026, 16 de septiembre). *GitHub Student Pack 2026: What it is actually worth*. https://capitalandcompute.net/blog/github-student-developer-pack-2026/
- Fila, R. (2026, 8 de junio). *Supabase free tier limits 2026*. Automation Atlas. https://automationatlas.io/answers/supabase-free-tier-limits-2026/
- Laravel. (s. f.-a). *Database: Getting started* (Versión 13.x). Recuperado el 3 de noviembre de 2026, de https://laravel.com/docs/13.x/database
- Laravel. (s. f.-b). *Laravel Sail* (Versión 13.x). Recuperado el 3 de noviembre de 2026, de https://laravel.com/docs/13.x/sail
- Laravel. (s. f.-c). *Plans and pricing*. Laravel Cloud. Recuperado el 3 de noviembre de 2026, de https://laravel.com/cloud/docs/pricing
- Stripe. (s. f.). *Sandboxes*. Recuperado el 3 de noviembre de 2026, de https://docs.stripe.com/sandboxes
- Supabase. (2026, 3 de septiembre). *Use Supabase with Laravel*. https://supabase.com/docs/guides/getting-started/quickstarts/laravel
- Vercel. (2026, 14 de septiembre). *Vercel Hobby plan*. https://vercel.com/docs/plans/hobby
