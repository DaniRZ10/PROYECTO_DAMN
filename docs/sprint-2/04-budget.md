## 4. Presupuesto

Costes directos de **construir y desplegar la plataforma web de AIComp** durante el desarrollo (enero a mayo de 2027). Los socios dirigimos el proyecto y no cobramos: el trabajo lo hacen los profesionales contratados y externos definidos en los [recursos humanos](02-human-resources.md). Los servicios y sus precios vienen de los [recursos materiales](03-material-resources.md). Los dólares se convierten a 1 € = 1,1127 $ (Banco Central Europeo, 2026); los honorarios van sin IVA.

### 4.1 Costes directos

| Partida | Concepto | Cálculo | Importe |
| --- | --- | --- | --- |
| Equipamiento | Amortización de los 4 portátiles de los socios | 900 € × 4 equipos ÷ 48 meses × 5 meses (estimación propia) | 375,00 € |
| Equipamiento | Amortización de 2 portátiles para los desarrolladores | 900 € × 2 equipos ÷ 48 meses × 5 meses (estimación propia) | 187,50 € |
| Material fungible | No previsto | — | 0,00 € |
| Licencias de software | Claude Pro (Anthropic, s. f.) | 20 $ × 4 personas × 5 meses + 21 % de IVA = 484 $ | 434,98 € |
| Licencias de software | GitHub, VS Code, XAMPP y PostgreSQL | Gratuitos | 0,00 € |
| Servicios externos | Hosting de la API: Laravel Cloud Starter (Laravel, s. f.) | 5 $ × 4 meses (el primer mes es gratis; el uso cabe en los 5 $ incluidos) = 20 $ | 17,97 € |
| Servicios externos | Hosting del frontend: Cloudflare Pages, plan gratuito (Cloudflare, 2026) | — | 0,00 € |
| Servicios externos | Base de datos: Supabase, plan gratuito, 500 MB y 2 proyectos (Supabase, s. f.) | — | 0,00 € |
| Servicios externos | Dominio .es (OVHcloud, s. f.) | Primer año con IVA; la renovación sería de 8,46 € | 7,25 € |
| Servicios externos | Pagos con Stripe en modo prueba y correo con Mailpit | Gratuitos | 0,00 € |
| | **Total sin personal** | | **1.022,70 €** |
| Personal | Desarrollador/a frontend, contratado (ver 4.2) | 31.200 € al año × 5 ÷ 12 | 13.000,00 € |
| Personal | Desarrollador/a backend, contratado (ver 4.2) | 31.200 € al año × 5 ÷ 12 | 13.000,00 € |
| Honorarios | Diseñador/a UI/UX, externo (UI/UX Jobs Board, s. f.) | 80 h × 20 €/h (estimación propia de horas) | 1.600,00 € |
| Honorarios | Gestoría (Billeo, 2026) | 160 € al mes × 5 meses | 800,00 € |
| Honorarios | Asesoría legal en protección de datos (Atico34, s. f.) | Cuota anual | 180,00 € |
| | **Total de personal y honorarios** | | **28.580,00 €** |
| | **Total** | | **29.602,70 €** |
| Contingencias | 10 % del total | 29.602,70 € × 0,10 | 2.960,27 € |
| | **TOTAL CON CONTINGENCIAS** | | **32.562,97 €** |

### 4.2 Personal y honorarios (estimación propia)

- **Desarrolladores:** dos contratados a jornada completa durante los cinco meses. Sueldo de 24.000 € brutos al año, el punto medio del rango de un desarrollador junior en Sevilla, de 20.000 a 28.000 € (JobRise Team, 2026). Con un 30 % de cotizaciones a cargo de la empresa, cada uno cuesta 31.200 € al año.
- **Diseñador UI/UX:** externo, 80 horas al inicio del desarrollo a 20 €/h, el punto medio de la tarifa de un perfil intermedio, de 17 a 23 €/h (UI/UX Jobs Board, s. f.).
- **Gestoría y protección de datos:** cuotas publicadas para una sociedad con operativa sencilla (Billeo, 2026) y para la adaptación al RGPD (Atico34, s. f.).

**Reparto de las horas de desarrollo por módulo** (2 personas × 40 h a la semana × 21 semanas, del 4 de enero al 28 de mayo de 2027 = 1.680 h; los módulos son los de [01-modules.md](01-modules.md)):

| Módulo | Horas |
| --- | --- |
| Páginas públicas y contenido por sector | 120 |
| Catálogo de equipos | 160 |
| Configurador por sector y caso de uso | 320 |
| Cuentas y acceso | 140 |
| Carrito, presupuesto y pedido | 220 |
| Servicios y cuota de mantenimiento | 100 |
| Área de cliente | 140 |
| Panel de administración | 200 |
| Módulos simulados: pago, avisos por correo, y logística y plazos | 80 |
| Entorno, integración, pruebas y despliegue | 200 |
| **Total** | **1.680** |

### 4.3 Contingencias

Un **10 %**, el mínimo del rango: los precios de licencias y servicios están comprobados en su fuente y el personal se calcula con supuestos explícitos. Cubre, por ejemplo, superar los 5 $ de uso de Laravel Cloud, tener que pasar a un plan de pago de Supabase o necesitar más horas de diseño.

### 4.4 Después del lanzamiento (fuera de este presupuesto)

Operar AIComp exige los puestos del bloque B de los recursos humanos. Como referencia, su coste mensual sería de unos **5.143 €**: un técnico de sistemas e IA y un comercial, cada uno a 23.000 € brutos al año más un 30 % de cotizaciones (2.491,67 € al mes cada uno; Navalon Pascual, 2026; calculadornomina.es, 2026), y la gestoría (160 € al mes).

**Supuestos:** desarrollo de enero a mayo de 2027; portátiles de 900 € con 4 años de vida útil, 30 % de cotizaciones, horas del diseñador y reparto de horas por módulo (estimaciones propias); IVA del 21 % sobre Claude Pro; tipo de cambio del 11 de noviembre de 2026.

### Referencias

- Anthropic. (s. f.). *How much does Claude Pro cost?* Recuperado el 12 de noviembre de 2026, de https://support.anthropic.com/en/articles/8325610-how-much-does-claude-pro-cost
- Atico34. (s. f.). *Contratar protección de datos con una empresa líder*. Recuperado el 12 de noviembre de 2026, de https://protecciondatos-lopd.com/contratar/
- Banco Central Europeo. (2026, 11 de noviembre). *US dollar (USD)*. Euro exchange rates charts. https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/eurofxref-graph-usd.en.html
- Billeo. (2026, 26 de septiembre). *Precios de gestoría y gestión de nóminas*. https://www.billeo.es/blog/precios-gestorias-empresas-espana
- calculadornomina.es. (2026, enero). *Sueldo de Comercial / vendedor/a en España 2026: bruto y neto*. https://calculadornomina.es/salarios/sueldo-comercial-espana-2026/
- Cloudflare. (2026, 5 de septiembre). *Limits*. Cloudflare Pages docs. https://developers.cloudflare.com/pages/platform/limits/
- JobRise Team. (2026, 20 de mayo). *Salario Developer Junior en España 2026*. JobRise. https://jobrise.io/es/blog/salario-developer-junior-espana-2026/
- Laravel. (s. f.). *Plans and pricing*. Laravel Cloud. Recuperado el 12 de noviembre de 2026, de https://laravel.com/cloud/docs/pricing
- Navalon Pascual, E. (2026, 17 de febrero). *¿Cuánto gana un Técnico en Sistemas Microinformáticos 2026?* ILERNA. https://www.ilerna.es/blog/salario-sistemas-microinformaticos-redes
- OVHcloud. (s. f.). *Dominio .es: comprar y registrar un dominio .es*. Recuperado el 12 de noviembre de 2026, de https://www.ovhcloud.com/es-es/domains/tld/es/
- Supabase. (s. f.). *Pricing & fees*. Recuperado el 12 de noviembre de 2026, de https://supabase.com/pricing
- UI/UX Jobs Board. (s. f.). *UI/UX designer salary in Spain 2026*. Recuperado el 12 de noviembre de 2026, de https://uiuxjobsboard.com/salary/ui-ux-designer/spain
