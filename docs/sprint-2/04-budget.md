## 4. Presupuesto

Costes directos de **construir y desplegar la plataforma web de AIComp** durante el desarrollo (enero a mayo de 2027). No es el presupuesto de la empresa, que está en la viabilidad del Sprint 1. Importes en euros con IVA cuando la fuente lo indica; los dólares se convierten a 1 € = 1,1127 $ (Banco Central Europeo, 2026).

### 4.1 Costes directos

| Partida | Concepto | Cálculo | Importe |
| --- | --- | --- | --- |
| Equipamiento | Amortización de 4 portátiles propios | 900 € × 4 equipos ÷ 48 meses × 5 meses (estimación propia) | 375,00 € |
| Material fungible | No previsto | — | 0,00 € |
| Licencias de software | Claude Pro (Anthropic, s. f.) | 20 $ × 4 personas × 5 meses + 21 % de IVA = 484 $ | 434,98 € |
| Licencias de software | GitHub, VS Code, XAMPP y PostgreSQL | Gratuitos | 0,00 € |
| Servicios externos | Hosting de la API: Laravel Cloud Starter (Laravel, s. f.) | 5 $ × 4 meses (el primer mes es gratis; el uso cabe en los 5 $ incluidos) = 20 $ | 17,97 € |
| Servicios externos | Hosting del frontend: Cloudflare Pages, plan gratuito (Cloudflare, 2026) | — | 0,00 € |
| Servicios externos | Base de datos: Supabase, plan gratuito, 500 MB y 2 proyectos (Supabase, s. f.) | — | 0,00 € |
| Servicios externos | Dominio .es (OVHcloud, s. f.) | Primer año con IVA; la renovación sería de 8,46 € | 7,25 € |
| Servicios externos | Pagos con Stripe en modo prueba y correo con Mailpit | Gratuitos | 0,00 € |
| | **Total sin personal** | | **835,20 €** |
| Personal | 4 desarrolladores junior (estimación propia; ver 4.2) | 672 h × 17,73 €/h | 11.912,73 € |
| | **Total con personal** | | **12.747,93 €** |
| Contingencias | 10 % del total con personal | 12.747,93 € × 0,10 | 1.274,79 € |
| | **TOTAL** | | **14.022,72 €** |

### 4.2 Personal (estimación propia)

- **Horas:** 4 personas × 8 h a la semana × 21 semanas (del 4 de enero al 28 de mayo de 2027) = **672 h**. El reparto por módulo queda pendiente de decidir hasta que se cierre la lista de módulos (issue #29).
- **Coste por hora:** 24.000 € brutos al año, el punto medio del rango de un desarrollador junior en Sevilla, de 20.000 a 28.000 € (JobRise Team, 2026). Con un 30 % de cotizaciones a cargo de la empresa, el coste es de 31.200 € al año; dividido entre 1.760 h anuales, sale a **17,73 €/h**.
- El equipo no cobra: la partida muestra lo que costaría el trabajo si se pagara.

### 4.3 Contingencias

Un **10 %**, el mínimo del rango: los precios de licencias y servicios están comprobados en su fuente y el personal ya se calcula aparte con supuestos explícitos. Cubre, por ejemplo, superar los 5 $ de uso de Laravel Cloud o tener que pasar a un plan de pago de Supabase.

**Supuestos:** desarrollo de enero a mayo de 2027, con 8 h semanales por persona (supuesto del equipo); portátiles de 900 € con 4 años de vida útil, 30 % de cotizaciones y 1.760 h anuales (estimaciones propias); IVA del 21 % sobre Claude Pro; tipo de cambio del 11 de noviembre de 2026.

### Referencias

- Anthropic. (s. f.). *How much does Claude Pro cost?* Recuperado el 12 de noviembre de 2026, de https://support.anthropic.com/en/articles/8325610-how-much-does-claude-pro-cost
- Banco Central Europeo. (2026, 11 de noviembre). *US dollar (USD)*. Euro exchange rates charts. https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/eurofxref-graph-usd.en.html
- Cloudflare. (2026, 5 de septiembre). *Limits*. Cloudflare Pages docs. https://developers.cloudflare.com/pages/platform/limits/
- JobRise Team. (2026, 20 de mayo). *Salario Developer Junior en España 2026*. JobRise. https://jobrise.io/es/blog/salario-developer-junior-espana-2026/
- Laravel. (s. f.). *Plans and pricing*. Laravel Cloud. Recuperado el 12 de noviembre de 2026, de https://laravel.com/cloud/docs/pricing
- OVHcloud. (s. f.). *Dominio .es: comprar y registrar un dominio .es*. Recuperado el 12 de noviembre de 2026, de https://www.ovhcloud.com/es-es/domains/tld/es/
- Supabase. (s. f.). *Pricing & fees*. Recuperado el 12 de noviembre de 2026, de https://supabase.com/pricing
