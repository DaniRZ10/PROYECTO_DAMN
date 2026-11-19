## 3. Criterios de calidad

Este bloque fija **cuándo se da por terminado cada objetivo grande del MVP** y con qué se comprueba. Los objetivos son **épicas**, no historias de usuario ni tareas: agrupan los módulos definidos en el Sprint 2 ([módulos de la plataforma](../sprint-2/01-modules.md)) y se miden con indicadores que cualquiera del equipo puede verificar. El diseño que acompaña a estas épicas está en [arquitectura y flujos](01-architecture.md) y en los [wireframes](02-wireframes.md).

Cada indicador es **un número, un sí/no o una prueba**. Ninguno depende de una opinión.

### 3.1 Definition of Done general

Lo que cumple **toda** épica antes de darse por terminada. Se suma a la Definition of Done por issue del contrato del equipo, no la sustituye.

1. **Issues cerradas en regla.** Todas las issues de la épica cumplen sus criterios de aceptación y su PR ha sido aprobada y fusionada en `develop` por el Scrum Master, con la tarjeta en Done.
2. **Desplegada y funcionando** en los entornos del proyecto: frontend en Cloudflare Pages, API en Laravel Cloud y datos en PostgreSQL (Supabase).
3. **Flujo completo sin errores.** El camino principal de la épica se recorre de principio a fin sin errores en la consola del navegador ni respuestas 5xx de la API.
4. **Usable de 360 px a escritorio**, sin desbordamiento horizontal.
5. **Permisos comprobados con los tres roles** (visitante, cliente y administrador): ninguna pantalla ni *endpoint* de la épica responde a un rol que no le corresponde.
6. **Lighthouse de 90 o más** en rendimiento y en accesibilidad en las pantallas principales de la épica. La banda 90–100 es la que Lighthouse considera buena (Chrome for Developers, 2019); extenderla también a accesibilidad es decisión nuestra (estimación propia).
7. **Reproducible en local** por cualquiera del equipo (XAMPP y PostgreSQL), con los datos de ejemplo cargados por un *seeder*.
8. **Documentada.** README actualizado y, si la épica toca la API, sus *endpoints* y los estados que maneja descritos.

### 3.2 Las épicas del MVP

Los 11 módulos que entran en el MVP se agrupan en cinco épicas. Cada módulo pertenece a **una sola** épica, para que no haya objetivos que se den por terminados dos veces ni módulos sin dueño.

| Épica | Módulos que agrupa (numeración del Sprint 2) |
| --- | --- |
| **E1 Escaparate por sector y catálogo** | 1 Páginas públicas y contenido por sector · 2 Catálogo de equipos |
| **E2 Configurador por sector y caso de uso** | 3 Configurador |
| **E3 Compra: alta de cliente, presupuesto y pedido** | 4 Cuentas y acceso · 5 Carrito, presupuesto y pedido · 6 Servicios y cuota de mantenimiento · 9 Pago (simulado) · 10 Avisos por correo (simulado) |
| **E4 Área de cliente y servicios contratados** | 7 Área de cliente |
| **E5 Administración: catálogo, reglas y pedidos** | 8 Panel de administración · 11 Logística y plazos (simulado) |

**Por qué este reparto.** Se mantiene la propuesta de partida de cinco épicas, con tres precisiones:

- **Los módulos simulados no son épicas propias.** El pago y los avisos por correo solo existen dentro de la compra, así que su Definition of Done se comprueba en E3. La logística es el estado y el plazo que mueve el administrador, así que va en E5; que el plazo se vea en la ficha se comprueba en E1.
- **Los servicios y la cuota (módulo 6) se contratan durante la compra**, de modo que su Definition of Done va en E3; que el cliente los consulte después se comprueba en E4.
- **Los módulos 12 a 15 quedan fuera del MVP** y no tienen épica: no se construyen, luego no procede darlos por terminados.

### 3.3 Definition of Done e indicadores por épica

| Épica | Objetivo | Definition of Done | Indicadores medibles |
| --- | --- | --- | --- |
| **E1 Escaparate por sector y catálogo** | Que una pyme reconozca su caso en la web y llegue al configurador con su sector ya marcado. | Portada, páginas de los tres sectores, "cómo funciona" y contacto publicadas; catálogo con listado y ficha, con datos de ejemplo; cada ficha muestra plazo de entrega estimado y no unidades en stock. | · Las 4 entradas del configurador (despachos, gestorías, clínicas y "otro") lo abren con el sector preseleccionado: sí/no en las 4.<br>· Un visitante llega de la página de sector al presupuesto en **4 pasos como máximo**.<br>· El **100 %** de las fichas muestra plazo de entrega estimado y **ninguna** muestra stock. |
| **E2 Configurador por sector y caso de uso** | Que cualquier combinación de respuestas devuelva un presupuesto explicable, con equipo, puesta en marcha y cuota. | El cuestionario pregunta solo sector, número de usuarios y uso; las reglas y los precios se resuelven en la API; devuelve equipo, puesta en marcha, cuota y la explicación de por qué ese equipo. | · El **100 %** de las combinaciones de sector y tramo de usuarios devuelve un equipo del catálogo.<br>· El equipo devuelto es el más económico que cumple las reglas: prueba automatizada sobre todos los tramos.<br>· Ninguna regla ni precio se resuelve en el frontend: sí/no, comprobado en la respuesta de la API.<br>· Toda recomendación lleva su explicación: **100 %** de las respuestas. |
| **E3 Compra: alta de cliente, presupuesto y pedido** | Que un visitante se registre y convierta su presupuesto en un pedido registrado y pendiente de pago. | Registro y acceso de la empresa; el presupuesto se guarda, pasa al carrito y se convierte en pedido; la puesta en marcha y la cuota se contratan junto al equipo; el pedido nace pendiente de pago; los avisos salen contra Mailpit. | · Sin sesión se crean **0** pedidos y **0** presupuestos guardados: prueba sobre la API.<br>· Todo pedido confirmado nace en estado "recibido" y pago "pendiente de pago": sí/no.<br>· El **100 %** de los registros y de los pedidos confirmados genera su correo en Mailpit.<br>· Los importes del presupuesto llegan al pedido **sin variación**: prueba comparando importes. |
| **E4 Área de cliente y servicios contratados** | Que el cliente consulte en todo momento sus presupuestos, pedidos, estados y servicios contratados. | El área muestra presupuestos guardados, pedidos con su estado y servicios contratados, y solo los de la empresa que ha accedido. | · Un cliente ve el **100 %** de sus pedidos y **0** de otra empresa: prueba con dos empresas.<br>· Un cambio de estado hecho por el administrador se ve al recargar: sí/no.<br>· Pedir por la API un pedido ajeno devuelve **403** en el **100 %** de los intentos. |
| **E5 Administración: catálogo, reglas y pedidos** | Que un administrador mantenga el catálogo y las reglas y mueva los pedidos sin tocar código. | Alta, edición y baja del catálogo; mantenimiento de las reglas del configurador y de los servicios y cuotas; gestión de los pedidos, sus cuatro estados y el paso a pagado. | · Crear, editar y dar de baja un equipo sin desplegar código: sí/no.<br>· Cambiar una regla altera la recomendación en la siguiente ejecución del configurador, sin desplegar: prueba manual.<br>· Los **4** estados del pedido (recibido, en montaje, enviado, entregado) y el paso a "pagado" se manejan desde el panel: sí/no.<br>· Una sesión de cliente recibe **403** en el **100 %** de los *endpoints* del panel. |

### Referencias

- Chrome for Developers. (2019, 19 de septiembre). *Lighthouse performance scoring*. https://developer.chrome.com/docs/lighthouse/performance/performance-scoring
