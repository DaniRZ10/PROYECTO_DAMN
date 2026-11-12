## 3. Recursos materiales

Recursos materiales y técnicos para construir y desplegar la plataforma web de AIComp. Con este bloque quedan cerradas todas las decisiones técnicas que el Sprint 1 dejó abiertas. Los importes y su total están en el [presupuesto](04-budget.md).

### 3.1 Equipos y herramientas

| Recurso | Detalle | Coste |
| --- | --- | --- |
| Equipos | Cuatro portátiles propios | Solo su amortización |
| Desarrollo | VS Code, Git, Node, Composer y Postman o Thunder Client | Gratuitos |
| Gestión | GitHub, con ramas protegidas y PR revisadas, y GitHub Projects como tablero | Gratuitos |
| Asistente de IA | Claude Pro, una licencia por persona | 20 $ al mes por persona, más impuestos (Anthropic, s. f.) |

### 3.2 Decisiones técnicas

| Pieza | Decisión | Por qué | Coste |
| --- | --- | --- | --- |
| Hosting del frontend | **Cloudflare Pages**, plan gratuito | Permite 500 builds al mes y dominios propios (Cloudflare, 2026). Vercel Hobby se limita a uso personal y no comercial (Vercel, 2026), y AIComp es una tienda | 0 € |
| Hosting de la API | **Laravel Cloud**, plan Starter | Pensado para Laravel: incluye 5 $ de uso al mes, el primer mes es gratis, se apaga sin tráfico y admite dominio propio (Laravel, s. f.). Railway cuesta lo mismo, pero es genérico (Railway, s. f.). Un VPS de Hetzner sale a 5,99 € al mes, hay que administrarlo y el más barato no se podía contratar en octubre de 2026 (Dragos, 2026) | 5 $ al mes |
| Base de datos | **PostgreSQL en Supabase**, plan gratuito, solo como base de datos | 500 MB y dos proyectos. Se pausa tras una semana sin uso (Fila, 2026), así que se desarrolla contra un PostgreSQL local | 0 € |
| Entorno local | **XAMPP** con la extensión `pdo_pgsql` y PostgreSQL local | Es el entorno que el equipo ya conoce. Docker queda descartado por el tiempo de aprendizaje | 0 € |
| Dominio | **`.es`** | 7,25 € el primer año con IVA y 8,46 € la renovación (OVHcloud, s. f.) | 7,25 € |
| Pagos | **Presupuesto y transferencia, simulados** | La venta a empresas suele ir por presupuesto. Stripe en modo prueba queda como extra (Stripe, s. f.) | 0 € |
| Correo | **Mailpit** en desarrollo | El correo real queda fuera del MVP | 0 € |

No queda ninguna decisión técnica pendiente ni abierta.

### Referencias

- Anthropic. (s. f.). *How much does Claude Pro cost?* Recuperado el 10 de noviembre de 2026, de https://support.anthropic.com/en/articles/8325610-how-much-does-claude-pro-cost
- Cloudflare. (2026, 5 de septiembre). *Limits*. Cloudflare Pages docs. https://developers.cloudflare.com/pages/platform/limits/
- Dragos. (2026, 20 de octubre). *Precios de Hetzner Cloud y planes Cost-Optimized (2026): CX23, CPX y alternativas*. Bitdoze. https://www.bitdoze.com/es/hetzner-cloud-precios-2026/
- Fila, R. (2026, 8 de junio). *Supabase free tier limits 2026*. Automation Atlas. https://automationatlas.io/answers/supabase-free-tier-limits-2026/
- Laravel. (s. f.). *Plans and pricing*. Laravel Cloud. Recuperado el 10 de noviembre de 2026, de https://laravel.com/cloud/docs/pricing
- OVHcloud. (s. f.). *Dominio .es: comprar y registrar un dominio .es*. Recuperado el 10 de noviembre de 2026, de https://www.ovhcloud.com/es-es/domains/tld/es/
- Railway. (s. f.). *Pricing plans*. Railway Docs. Recuperado el 10 de noviembre de 2026, de https://docs.railway.com/pricing/plans
- Stripe. (s. f.). *Sandboxes*. Recuperado el 3 de noviembre de 2026, de https://docs.stripe.com/sandboxes
- Vercel. (2026, 14 de septiembre). *Vercel Hobby plan*. https://vercel.com/docs/plans/hobby
