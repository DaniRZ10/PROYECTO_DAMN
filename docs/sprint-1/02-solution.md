## 2\. Propuesta de solución

La IA de tu empresa, montada a medida y sin salir de tu oficina.

### 2.1 Qué es la solución

**AIComp** vende ordenadores para ejecutar IA dentro de la propia empresa, montados de serie o personalizados. Llegan con modelos abiertos ya instalados (Llama, Qwen, Gemma, Mistral) y adaptados a los documentos del cliente, y se completan con servicios de instalación, personalización y mantenimiento.

Lo que construimos nosotros es la plataforma web de AIComp: la tienda online, un configurador que recomienda el equipo según el caso de uso (no según las piezas) y un área de cliente para seguir pedidos y gestionar los servicios contratados.

### 2.2 Ventajas e inconvenientes

| ✅ Ventajas                                                                                                                                                                               | ⚠️ Inconvenientes                                                                                                                                                                              |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Los datos no salen de la oficina.** Es lo que pide el mercado: el 91 % de los responsables de TI prefiere infraestructura propia, privada o híbrida para IA con datos sensibles. | **Hardware caro y volátil.** La RTX PRO 6000 pasó de 7.628 € a 17.003 € en 12 meses y la memoria subió un 40–70 % en 2025: riesgo para el margen y el stock                         |
| **Pago único en lugar de suscripción.** Para 50 usuarios, un equipo de 5.000–8.000 € frente a 10.800 $ al año de Microsoft 365 Copilot Business.                               | **Competidor grande.** PcComponentes (825 M€ de ventas en 2025) vende IA local para empresas desde octubre de 2026.                                                                       |
| **Lista para usar.** El cliente no necesita ingenieros de IA; la falta de conocimiento es el primer freno de las empresas europeas para usar IA.                                    | **No sustituye a la nube en todo.** Un modelo local no se integra con Office como Copilot, y los modelos más grandes exigen servidores de 80.000 € o más (estimación propia del pitch) |
| **Ingresos recurrentes.** Instalación, personalización y mantenimiento estabilizan un margen de hardware frágil                                                                  | **Los servicios escalan peor que la tienda.** Dependen de personas; AIHARD, por ejemplo, solo va a domicilio en la zona de Barcelona.                                                      |

### 2.3 Justificación

| Criterio                                     | Por qué AIComp lo cumple                                                                                                                                                                                             |
| -------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Coste para el cliente**              | Hay un equipo para cada tamaño, de 550–1.840 € para un autónomo a 5.000–8.000 € para 50 usuarios: del orden de un año de suscripción en la nube, pagado una sola vez.                                        |
| **Privacidad de los datos**            | Los datos se procesan en la oficina del cliente, lo que facilita cumplir el RGPD y el AI Act, cuyas obligaciones de transparencia aplican desde el 2 de agosto de 2026.                                               |
| **Complejidad técnica para nosotros** | Construimos la web, no los equipos: tienda, configurador y área de cliente con el stack que propone el profesor (React, Laravel y Tailwind). La pieza más compleja es el configurador.                              |
| **Escalabilidad**                      | Una sola web y un catálogo por niveles, del mini PC al servidor multi-GPU. Se vende online en toda España, no solo en una zona como los integradores pequeños.                                                     |
| **Encaje con el mercado**              | Ocupa el hueco entre la tienda que solo vende hardware y la consultoría local. La adopción aún es baja (21,1 % de las empresas con 10 o más empleados en 2025) y la entrada de PcComponentes confirma la demanda. |

### 2.4 Por qué no otras vías

Descartamos la nube privada porque el cliente seguiría pagando cada mes y dependiendo de un tercero, y el renting de equipos porque, con precios de GPU tan volátiles, el riesgo del hardware recaería en AIComp.

### Fuentes

**Cloudian**: https://cloudian.com/press/enterprise-repatriating-ai-workloads/
**GPUPrix**: https://gpuprix.com/spain/gpus/rtx-pro-6000-blackwell
**Omdia, vía The Register**: https://www.theregister.com/on-prem/2026/01/12/pc-shipments-set-to-hit-the-buffers-as-ai-guzzles-memory/5151409
**eesel**: precios de Copilot: https://www.eesel.ai/blog/copilot-pricing
**pi3g**: precios de DGX Spark: https://pi3g.com/nvidia-dgx-spark-price/
**Xataka**: https://www.xataka.com/robotica-e-ia/uno-mayores-distribuidores-hardware-espana-ha-tenido-idea-para-seguir-creciendo-convertirse-dell
**Eurostat, vía Euronews**: https://es.euronews.com/2026/05/25/por-que-las-empresas-europeas-no-usan-herramientas-de-ia
**AIHARD**: https://www.aihard.es/es
**VORLUX AI**: https://vorluxai.com/
**Gibson Dunn**: https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/
**INE, vía Bolsamanía**: https://www.bolsamania.com/noticias/empresas/economia--el-211-de-empresas-en-espana-de-10-o-mas-empleados-uso-la-ia-en-el-primer-trimestre-del-ano-segun-el-ine--21080387.html
