## 4. Viabilidad

Viabilidad de **AIComp como empresa**: crearla y operarla, no solo construir su web. Para cada ámbito se indica el riesgo principal, cómo lo resolvemos y qué haríamos si esa solución no basta. Las cifras sin fuente son estimaciones propias.

### 4.1 Viabilidad por ámbitos

| Ámbito | Riesgo | Solución | Alternativa |
| --- | --- | --- | --- |
| **Técnico: equipos y modelos** | Montar, instalar y mantener los modelos exige ingeniería de IA, y el equipo fundador es de desarrollo web | Procesos y plantillas por sector; contratar o subcontratar la ingeniería de IA, como hace AIHARD con socios externos (AIHARD, s. f.) | Empezar con un solo sector y un catálogo corto de equipos probados |
| **Técnico: plataforma web** | Aprender React y Laravel mientras se construye; la API necesita un hosting con PHP | Stack con planes gratuitos y alcance acotado (detalle en el apartado 4.4) | Simular lo que no dé tiempo a construir, como los pagos o los envíos |
| **Económico** | Margen del hardware bajo y volátil; unos 60.700 € que financiar antes de vender | Montaje bajo pedido, sin stock; el margen sale sobre todo de los servicios (apartado 4.2) | Vender solo servicios sobre el hardware del cliente |
| **Legal** | RGPD, AI Act y licencias de modelos con restricciones | Contrato de encargado del tratamiento cuando el mantenimiento acceda a datos del cliente (Reglamento [UE] 2016/679, 2016); documentación de cumplimiento por sector; catálogo solo con modelos Apache 2.0 o MIT, porque Llama 4 excluye a las empresas con sede en la UE en sus modelos multimodales (Wevelsiep, 2026) | Asesoría jurídica externa para los sectores más regulados (salud y abogacía) |
| **Operativo** | Dependencia de los mayoristas y de los plazos de memoria y GPU; el soporte presencial no escala | Mostrar plazo de entrega en lugar de stock; soporte en remoto por defecto | Varios mayoristas y varias gamas (NVIDIA, AMD y Apple) |
| **Mercado** | PcComponentes y otros grandes entran en la IA local con muchos más recursos (PcComponentes, 2026) | Especialización por sector y relación de mantenimiento (ver el [bloque 3](03-innovation.md)) | Ofrecer puesta en marcha y mantenimiento a quien compró el equipo en otra tienda |

### 4.2 Cifras estimadas

Las cifras de inversión y de costes salen del [presupuesto del primer año](../budget/aicomp-budget.xlsx) (enero a diciembre de 2027, sin IVA y con un 12 % de contingencias), que sustituye a las estimaciones iniciales de este apartado.

**Lo que hace falta antes de vender**

| Concepto | Importe | Qué incluye |
| --- | --- | --- |
| Inversión inicial | 21.855,74 € | Constitución de la SL y marca, equipamiento del local y del taller, portátiles y equipos de demostración (un DGX Spark y un mini PC de entrada) |
| Construcción de la plataforma (enero a mayo de 2027) | 37.272,47 € | Dos desarrolladores contratados, diseñador, gestoría y servicios, y el local desde mayo |
| Fianza del local | 1.600,00 € | Desembolso recuperable |
| **Total que hay que financiar** | **≈ 60.700 €** | |

**Cómo se financia** (estimación propia). El capital social de la SL son 3.000 € y no basta. La línea Jóvenes Emprendedores de ENISA presta de 25.000 a 75.000 € a sociedades de menos de 24 meses con socios jóvenes, siempre que la empresa aporte fondos propios de al menos la mitad del préstamo (González, 2025). Una combinación posible: unos 20.000 € de los socios y un préstamo de 40.000 €. Si no se consigue, la alternativa es abaratar la construcción: un solo desarrollador o una web más pequeña.

**Margen por cliente** (ejemplo: pyme de 10–20 usuarios)

| Concepto | Margen para AIComp | Notas |
| --- | --- | --- |
| Equipo de 128 GB (≈ 8.000 €) | ≈ 800 € | Estimación propia: margen de tienda del 10 % |
| Puesta en marcha por sector: instalación, documentos y formación | ≈ 1.500 € | Estimación propia |
| Mantenimiento: actualización de modelos y soporte | ≈ 1.200 € al año | Estimación propia: 100 € al mes |
| **Total el primer año** | **≈ 3.500 €** | Desde el segundo año, solo el mantenimiento |

**Punto de equilibrio.** Los socios no cobran sueldo. Operar AIComp cuesta unos **8.974 € al mes** sin contingencias: el técnico de sistemas e IA (23.000 € brutos al año), el comercial, un desarrollador a media jornada para mantener la web, el local, la gestoría, el software y el marketing. Son unos **108.000 € al año**. Con 3.500 € de margen por cliente, AIComp necesita unos **31 clientes nuevos al año**, unos 2,6 al mes (estimación propia).

- **Desde el segundo año baja:** si los clientes del primer año renuevan el mantenimiento (31 × 1.200 € = 37.200 € al año), bastan unos **20 clientes nuevos**.
- **Margen de maniobra:** sin el desarrollador a media jornada, el punto de equilibrio baja a unos 26 clientes al año; subir la puesta en marcha a 2.000 € lo deja en unos 27.
- **Encaje con el mercado:** el escenario ilustrativo de `pitch.md` (un 2 % de un mercado de unos 9,7 M€, unos 32 equipos al año) queda justo en el punto de equilibrio. AIComp es viable, pero con poco colchón el primer año: por eso el mantenimiento recurrente es la pieza clave del negocio.

### 4.3 Escenarios

**Si los componentes siguen subiendo.** La memoria DDR5 costaba de media en julio de 2026 un 448 % más que un año antes (Equipo Editorial blog COOLMOD, 2026). TrendForce prevé otra subida del 10–15 % en los precios de contrato de la DRAM en el cuarto trimestre de 2026, y SK Hynix espera escasez de memoria al menos hasta 2030 (Kleinbaum, 2026). El fabricante Team Group no ve equilibrio entre oferta y demanda antes de la segunda mitad de 2028 (3dpoder, 2026). Nuestras respuestas, de menor a mayor cambio:

1. **Sin stock.** Montaje bajo pedido, presupuestos con validez corta y una parte del pago por adelantado: el riesgo de precio no se queda en el almacén.
2. **Menos hardware por cliente.** Modelos más pequeños y cuantizados. Un portátil con NPU ya ejecuta modelos de 7 a 13 mil millones de parámetros (Cañete, 2026).
3. **Otras gamas.** Un mini PC con AMD Ryzen AI Max cuesta desde 2.629 €, frente a los 6.999 € de un DGX Spark (PcComponentes, s. f.). También equipos reacondicionados.
4. **Si el hardware deja de ser rentable.** AIComp vende solo la puesta en marcha y el mantenimiento sobre el equipo del cliente. Con las cifras del apartado 4.2, son unos 2.700 € por cliente el primer año.

**Si cambia la situación de la IA.**

| Cambio | Efecto en AIComp | Respuesta |
| --- | --- | --- |
| Los modelos útiles caben en cualquier portátil | Se venden menos equipos dedicados | Más peso de la puesta en marcha por sector y del mantenimiento, sobre los equipos del cliente |
| La nube privada o soberana baja de precio | Parte de los clientes prefiere no tener un equipo en la oficina | Ofrecer el mismo servicio por sector sobre una nube europea |
| Cambian las licencias de los modelos abiertos | Un modelo deja de poder usarse | Catálogo con varias familias Apache 2.0 o MIT, sin depender de un solo fabricante (Wevelsiep, 2026) |
| Más regulación (AI Act) | Más carga para las pymes | Oportunidad: la documentación de cumplimiento por sector ya forma parte del servicio |

### 4.4 Viabilidad técnica de la plataforma web

Viabilidad de la plataforma que construimos nosotros: tienda online, configurador por caso de uso y sector, y área de cliente.

**Recursos tecnológicos**

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Frontend: React + Tailwind CSS | Stack previsto por sugerencia del profesor; gratuito y muy documentado | Ninguno lo hemos usado en un proyecto real |
| Backend: Laravel (API REST) | Stack previsto; base de PHP | Aprender Laravel y conectarlo con React (CORS, autenticación por token) |
| Base de datos: **PostgreSQL en Supabase** (decidido) | SQL y MySQL de primero; Supabase es gratis (500 MB y 2 proyectos) y Laravel se conecta como a cualquier PostgreSQL (Laravel, s. f.-a; Supabase, 2026) | Usarlo solo como base de datos (el login lo gestiona Laravel); el plan gratuito se pausa tras una semana sin uso (Fila, 2026); para desarrollar, mejor un PostgreSQL local por persona |
| Git, GitHub y GitHub Projects | Repositorio con ramas protegidas, PR revisadas y tablero Kanban funcionando | Conflictos al trabajar cuatro personas en paralelo |
| Herramientas | VS Code, Postman o Thunder Client, WhatsApp | Mismas versiones de PHP, Node y Composer en todos los equipos |

**Materiales e infraestructura**

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Entorno local | Portátiles propios. **Abierto:** XAMPP o Docker con Laravel Sail (Laravel, s. f.-b) | Elegir uno común y un `.env.example` compartido. Con XAMPP hay que activar `pdo_pgsql` para PostgreSQL. Repos fuera de OneDrive |
| Entorno de pruebas | Nada todavía | Desplegar `develop` para enseñarlo en cada Sprint Review |
| Hosting | Frontend React: **Cloudflare Pages o Vercel** (elegir uno; Vercel, 2026). API Laravel: **pendiente** | Ni Cloudflare ni Vercel ejecutan Laravel de forma normal: la API necesita un hosting con PHP (Laravel Cloud [Laravel, s. f.-c], un servicio con Docker o un VPS). Créditos del GitHub Student Developer Pack (Capital & Compute, 2026) |
| Dominio | Subdominio gratuito del hosting | Dominio propio opcional: el GitHub Student Developer Pack incluye uno durante un año (Capital & Compute, 2026) |
| Pagos | **Pendiente (Sprint 2).** Presupuesto y pago por transferencia, o Stripe en modo prueba con tarjetas ficticias (Stripe, s. f.) | Nunca se cobra dinero real |
| Correo | **Pendiente (Sprint 2):** correos automáticos de registro y pedidos | En desarrollo se capturan en una bandeja de pruebas (Mailtrap o Mailpit) |

**Competencias del equipo**

| Recurso | Qué tenemos | Qué falta / riesgo |
| --- | --- | --- |
| Lo que ya sabemos | HTML, CSS, JavaScript, PHP, SQL, Java y Git básico | Nivel desigual entre los miembros |
| Lo que hay que aprender | — | React (componentes, estado, rutas), Laravel (migraciones, Eloquent, API), Tailwind, PostgreSQL y despliegue |
| Riesgo principal | Rotamos por todas las áreas | Aprender y producir a la vez: empezar con una prueba pequeña por tecnología |

**Limitaciones**

- **Tiempo:** sprints de una semana y pocas horas por persona, compaginadas con el resto de módulos. Propuesta de núcleo del MVP, pendiente de validar con el PO: catálogo, configurador, área de cliente, carrito, pedido y panel de administración básico.
- **Qué se simula y qué queda fuera: pendiente de debatir en el Sprint 2.** Propuesta inicial: simular pagos, stock (o mostrar plazo de entrega, ya que los equipos se montan a medida), envíos y catálogo; dejar fuera el montaje físico, la instalación real de modelos de IA, la integración con mayoristas, la facturación legal, la app móvil y los varios idiomas.
- **También pendiente:** cómo se venden los servicios (instalación, personalización y mantenimiento), los roles de usuario y el alcance del configurador.

### 4.5 Conclusión

AIComp es viable si vive de los servicios y no del stock: el hardware se monta bajo pedido, el margen sale de la puesta en marcha y del mantenimiento, y el catálogo no depende de un solo fabricante ni de un solo modelo. Si el hardware se encarece demasiado o la IA cambia, el negocio de servicios sigue en pie. La plataforma web es viable con herramientas gratuitas si acotamos el alcance y reservamos tiempo para aprender React y Laravel.

### Referencias

- AIHARD. (s. f.). *Consultoría de IA para empresas en Barcelona*. Recuperado el 10 de noviembre de 2026, de https://www.aihard.es/es/servicios
- Cañete, J. (2026, 17 de marzo). *NPU de nueva generación: el hardware que mueve IA en 2026*. Jacar. https://jacar.es/npu-nueva-generacion-2026/
- Capital & Compute. (2026, 16 de septiembre). *GitHub Student Pack 2026: What it is actually worth*. https://capitalandcompute.net/blog/github-student-developer-pack-2026/
- Equipo Editorial blog COOLMOD. (2026, 15 de septiembre). *Por qué ha subido el precio de la RAM y qué implica para quienes quieren comprar un PC*. Blog COOLMOD. https://www.coolmod.com/blog/categorias/componentes/por-que-ha-subido-el-precio-de-la-ram-y-que-implica-para-quienes-quieren-comprar-un-pc/
- Fila, R. (2026, 8 de junio). *Supabase free tier limits 2026*. Automation Atlas. https://automationatlas.io/answers/supabase-free-tier-limits-2026/
- González, G. (2025, 30 de mayo). *Línea ENISA para jóvenes emprendedores*. Legálitas. https://www.legalitas.com/actualidad/enisa-jovenes-emprendedores
- Holded. (s. f.). *Cuánto cuesta crear una empresa en España*. Recuperado el 10 de noviembre de 2026, de https://www.holded.com/es/herramientas/calculadoras-coste-crear-empresa
- Kleinbaum, T. (2026, 8 de noviembre). *SK Hynix triplica ingresos y Samsung bate récord: la RAM subirá hasta un 15 % este invierno*. Tendencias en la Red. https://www.netz-trends.de/es/sk-hynix-samsung-dram-sube-precio-invierno-2026/
- Laravel. (s. f.-a). *Database: Getting started* (Versión 13.x). Recuperado el 3 de noviembre de 2026, de https://laravel.com/docs/13.x/database
- Laravel. (s. f.-b). *Laravel Sail* (Versión 13.x). Recuperado el 3 de noviembre de 2026, de https://laravel.com/docs/13.x/sail
- Laravel. (s. f.-c). *Plans and pricing*. Laravel Cloud. Recuperado el 3 de noviembre de 2026, de https://laravel.com/cloud/docs/pricing
- PcComponentes. (s. f.). *PCs para IA local: portátiles, mini PC y sobremesa*. Recuperado el 10 de noviembre de 2026, de https://www.pccomponentes.com/categorias/ordenadores/ia-local
- PcComponentes. (2026, 18 de septiembre). *AI Computing Solutions Lead* [Oferta de empleo]. https://jobs.pccomponentes.com/jobs/8402926-ai-computing-solutions-lead
- Reglamento (UE) 2016/679 del Parlamento Europeo y del Consejo, de 27 de abril de 2016, relativo a la protección de las personas físicas en lo que respecta al tratamiento de datos personales y a la libre circulación de estos datos y por el que se deroga la Directiva 95/46/CE (Reglamento general de protección de datos). (2016). *Diario Oficial de la Unión Europea*, L 119, 1-88. https://eur-lex.europa.eu/eli/reg/2016/679/oj
- Stripe. (s. f.). *Sandboxes*. Recuperado el 3 de noviembre de 2026, de https://docs.stripe.com/sandboxes
- Supabase. (2026, 3 de septiembre). *Use Supabase with Laravel*. https://supabase.com/docs/guides/getting-started/quickstarts/laravel
- 3dpoder. (2026, 7 de noviembre). *Team Group avisa: la escasez de memoria DDR5 se agrava hasta 2027*. Foro3D. https://foro3d.com/2026/noviembre/team-group-avisa-la-escasez-de-memoria-ddr5-se-agrava-hasta-2027.html
- Vercel. (2026, 14 de septiembre). *Vercel Hobby plan*. https://vercel.com/docs/plans/hobby
- Wevelsiep, T. (2026, 12 de octubre). *Open LLM licences for commercial use: Apache 2.0, MIT, Llama, Qwen, Mistral*. WZ-IT. https://wz-it.com/en/knowledge/ki/open-llm-licenses-commercial-use/
