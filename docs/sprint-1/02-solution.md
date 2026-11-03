## 2. Propuesta de solución

La IA de tu empresa, montada a medida y sin salir de tu oficina.

### 2.1 Qué es la solución

**AIComp** vende ordenadores para ejecutar IA dentro de la propia empresa, montados de serie o personalizados. Llegan con modelos abiertos ya instalados (Llama, Qwen, Gemma, Mistral) y adaptados a los documentos del cliente, y se completan con servicios de instalación, personalización y mantenimiento.

Lo que construimos nosotros es la plataforma web de AIComp: la tienda online, un configurador que recomienda el equipo según el caso de uso (no según las piezas) y un área de cliente para seguir pedidos y gestionar los servicios contratados.

### 2.2 Ventajas e inconvenientes

| ✅ Ventajas                                                                                                                                                                               | ⚠️ Inconvenientes                                                                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Los datos no salen de la oficina.** Es lo que pide el mercado: el 91 % de los responsables de TI prefiere infraestructura propia, privada o híbrida para IA con datos sensibles (Cloudian, 2026). | **Hardware caro y volátil.** La RTX PRO 6000 pasó de 7.628 € a 17.003 € en 12 meses (GPU PRIX, s. f.) y la memoria subió un 40–70 % en 2025 (Omdia, como se citó en Robinson, 2026): riesgo para el margen y el stock                         |
| **Pago único en lugar de suscripción.** Para 50 usuarios, un equipo de 5.000–8.000 € (Batz, 2026) frente a 10.800 $ al año de Microsoft 365 Copilot Business (eesel AI, 2026).                               | **Competidor grande.** PcComponentes (825 M€ de ventas en 2025) vende IA local para empresas desde octubre de 2026 (Andrés, 2026).                                                                       |
| **Lista para usar.** El cliente no necesita ingenieros de IA; la falta de conocimiento es el primer freno de las empresas europeas para usar IA (Eurostat, 2025, como se citó en Markeviciute, 2026).                                    | **No sustituye a la nube en todo.** Un modelo local no se integra con Office como Copilot, y los modelos más grandes exigen servidores de 80.000 € o más (estimación propia del pitch) |
| **Ingresos recurrentes.** Instalación, personalización y mantenimiento estabilizan un margen de hardware frágil                                                                  | **Los servicios escalan peor que la tienda.** Dependen de personas; AIHARD, por ejemplo, solo va a domicilio en la zona de Barcelona (AIHARD, s. f.).                                                      |

### 2.3 Justificación

| Criterio                                     | Por qué AIComp lo cumple                                                                                                                                                                                             |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coste para el cliente**              | Hay un equipo para cada tamaño, de 550–1.840 € para un autónomo (VORLUX AI, s. f.) a 5.000–8.000 € para 50 usuarios: del orden de un año de suscripción en la nube, pagado una sola vez.                                        |
| **Privacidad de los datos**            | Los datos se procesan en la oficina del cliente, lo que facilita cumplir el RGPD y el AI Act, cuyas obligaciones de transparencia aplican desde el 2 de agosto de 2026 (Baladi et al., 2026).                                               |
| **Complejidad técnica para nosotros** | Construimos la web, no los equipos: tienda, configurador y área de cliente con el stack que propone el profesor (React, Laravel y Tailwind). La pieza más compleja es el configurador.                              |
| **Escalabilidad**                      | Una sola web y un catálogo por niveles, del mini PC al servidor multi-GPU. Se vende online en toda España, no solo en una zona como los integradores pequeños.                                                     |
| **Encaje con el mercado**              | Ocupa el hueco entre la tienda que solo vende hardware y la consultoría local. La adopción aún es baja (21,1 % de las empresas con 10 o más empleados en 2025; Europa Press, 2025) y la entrada de PcComponentes confirma la demanda. |

### 2.4 Por qué no otras vías

Descartamos la nube privada porque el cliente seguiría pagando cada mes y dependiendo de un tercero, y el renting de equipos porque, con precios de GPU tan volátiles, el riesgo del hardware recaería en AIComp.

### Referencias

- AIHARD. (s. f.). *Infraestructura de IA local para empresas*. Recuperado el 3 de noviembre de 2026, de https://www.aihard.es/es
- Andrés, R. (2026, 13 de octubre). *PcComponentes ha encontrado una forma de exprimir el auge de la IA sin necesidad de apostarlo todo al hardware*. Xataka. https://www.xataka.com/robotica-e-ia/uno-mayores-distribuidores-hardware-espana-ha-tenido-idea-para-seguir-creciendo-convertirse-dell
- Baladi, A., Gesing, K., Harrison, J., Lukic, V., Spano, R., Oberacker, Y. y Thonke, V. A. (2026, 27 de mayo). *EU AI Act omnibus agreement: Postponed high-risk deadlines and other key changes*. Gibson Dunn. https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/
- Batz, M. (2026, 16 de octubre). *NVIDIA DGX Spark price in October 2026*. pi3g. https://pi3g.com/nvidia-dgx-spark-price/
- Cloudian. (2026, 3 de marzo). *Enterprise survey finds 93% are repatriating AI workloads or evaluating a move away from public cloud* [Nota de prensa]. https://cloudian.com/press/enterprise-repatriating-ai-workloads/
- eesel AI. (2026, 7 de mayo). *Copilot pricing 2026: Business, Enterprise plans compared*. https://www.eesel.ai/blog/copilot-pricing
- Europa Press. (2025, 22 de octubre). *Economía.- El 21,1% de empresas en España de 10 o más empleados usó la IA en el primer trimestre del año, según el INE*. Bolsamanía. https://www.bolsamania.com/noticias/empresas/economia--el-211-de-empresas-en-espana-de-10-o-mas-empleados-uso-la-ia-en-el-primer-trimestre-del-ano-segun-el-ine--21080387.html
- GPU PRIX. (s. f.). *RTX PRO 6000 Blackwell price in Spain: History, deals & specs*. Recuperado el 18 de octubre de 2026, de https://gpuprix.com/spain/gpus/rtx-pro-6000-blackwell
- Markeviciute, E. (2026, 25 de mayo). *Por qué las empresas europeas todavía no aprovechan las herramientas de IA*. Euronews. https://es.euronews.com/next/2026/05/25/por-que-las-empresas-europeas-no-usan-herramientas-de-ia
- Robinson, D. (2026, 12 de enero). *PC shipments set to hit the buffers as AI guzzles memory*. The Register. https://www.theregister.com/2026/01/12/memory_shortages_price_hikes/
- VORLUX AI. (s. f.). *IA local: qué hardware y qué modelo, medido*. Recuperado el 3 de noviembre de 2026, de https://vorluxai.com/
