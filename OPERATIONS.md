# OPERATIONS.md

**Versión:** 0.5 (diseño de 0b, GATE A, en borrador: §9; nada ejecutado) · **Creado:** 2026-10-05
En 0a solo se **recogen hechos** sobre proveedor y operación. El procedimiento completo (SOP) se diseña y prueba en 0b. Todo valor no confirmado es `UNKNOWN`.

## 1. Flujo previsto (como lo describe Michael; sin stock propio)

```
cliente compra (Shopify + Wompi)
  → Vibrabien obtiene/prepara producto mediante proveedor
  → Vibrabien organiza despacho
  → cliente recibe
```

Cada paso por diseñar en 0b: TO DESIGN.

## 2. Ficha del proveedor

**Proveedor (hecho confirmado por Michael, 2026-10-06): SexoSentido / SexoSentido Mayoristas.** El proveedor **también vende al consumidor final a través de `sexosentido.co`** (riesgo `SUPPLIER-RETAIL CHANNEL CONFLICT`, ver `METRICS.md` §4). No se infiere todavía: razón social exacta, relación jurídica entre dominios, exclusividad, prioridad de inventario, condiciones para revendedores ni política de precios (todo UNKNOWN). **Pistas de los catálogos (consistentes con lo confirmado):** los catálogos de Fara Toys y de Winyi llevan en el pie la dirección www.sexosentidomayoristas.com (y, en algunas páginas de Fara, www.sexosentido.co). El catálogo "MUY SECRETO 2025_MAYOR" (lencería, abril 2025) declara como autor "Sexosentido Cartagena" y lleva la misma dirección web y un usuario público "@SEXOSENTIDOCOL". El catálogo Erotic V°1-2024 (la marca de los geles) no trae datos del distribuidor. Nombre, contacto y ubicación: UNKNOWN. Los tres catálogos no indican IVA, mínimos, vigencia, despacho ni garantía (ver `METRICS.md` §3.1).

**Cómo usar esta lista en la llamada:** no inventar ni suponer respuestas; lo que el proveedor no sepa o no quiera decir se registra como `UNKNOWN`. Pedir por escrito (correo o el medio que el proveedor use habitualmente) al menos costos, tiempos, factura y política de agotados. Las preguntas están ordenadas por prioridad: si la llamada se acorta, se cubren en este orden. **Estas preguntas son el GATE B de 0b** (ver `PROJECT.md` §4.1): la llamada no bloquea el cierre de 0a, pero sin las respuestas mínimas no se ejecuta el simulacro. Preguntas adicionales por el hecho confirmado: ¿exclusividad?, ¿prioridad de inventario?, ¿condiciones para revendedores?, ¿política de precios?

**Prioridad 1 — decide el margen y la capacidad de cumplir**

| Pregunta | Respuesta |
|---|---|
| ¿Cuánto tarda desde que se pide hasta tener el producto disponible para despacho? ¿Qué horarios tiene (corte del día, fines de semana)? | UNKNOWN |
| ¿Cómo se confirma la disponibilidad real de un producto antes de prometerlo? | UNKNOWN |
| **Costo de los 5 productos de la muestra D14 (§2.1)** y si los precios son estables o pueden cambiar sin aviso | UNKNOWN |
| ¿Mínimo de compra? ¿Forma de pago (por pedido, crédito, adelantado)? | UNKNOWN |
| ¿Entrega factura? ¿A nombre de quién? | UNKNOWN |
| ¿Puede despachar directo al cliente final? ¿Con empaque neutro? | UNKNOWN |

**Prioridad 2 — disponibilidad (por el stock virtual de Shopify)**

| Pregunta | Respuesta |
|---|---|
| ¿Con qué frecuencia cambian sus existencias? | UNKNOWN |
| ¿Qué productos suelen agotarse? | UNKNOWN |
| ¿Cuánto tarda en reponer un agotado? | UNKNOWN |
| ¿Puede avisar antes de un agotado? ¿Cómo? | UNKNOWN |
| ¿Tiene catálogo o listado de disponibilidad actualizado? ¿En qué formato y cada cuánto se actualiza? | UNKNOWN |

**Prioridad 3 — calidad y relación comercial**

| Pregunta | Respuesta |
|---|---|
| ¿Política de defectos, devoluciones y garantía? | UNKNOWN |
| ¿Materiales y seguridad del producto? ¿Autenticidad (originales, marca)? | UNKNOWN |
| ¿Vende también al público o a otras tiendas / marketplaces? ¿A qué precio? | **Sí: hecho confirmado por Michael (2026-10-06), el proveedor también vende al consumidor final a través de `sexosentido.co`.** Razón social exacta, relación jurídica entre dominios, exclusividad, prioridad de inventario, condiciones para revendedores y política de precios: UNKNOWN. Observado en `sexosentido.co`: (1.344 productos, vendedor "Sexo Sentido") vende al público los mismos SKU, con los mismos códigos que el catálogo (1522, 11105, 13353, 13047, 13354, 10376). ChatGPT reporta además otros vendedores del Gel Exótico y del Super Huevo (Lollipop Medellín, Nudite, Paradisex, Erotismo.co), sin relación demostrada con el mayorista. Precios y comparación en `METRICS.md` §3.3. Preguntas pendientes para el proveedor: exclusividad, prioridad de inventario, condiciones para revendedores y política de precios. |
| ¿Permite usar sus fotos? | UNKNOWN |
| ¿Hay un segundo proveedor de respaldo? | UNKNOWN |

### 2.1 Muestra D14 (fijada el 2026-10-05, antes de conocer costos)

Todos los productos existen en el catálogo público vivo. No son "producto estrella": son una muestra para estudiar economía unitaria. Regla y excepción: ver `METRICS.md` §3. Muestra aceptada por ambas IAs y **congelada**: no se cambia tras recibir costos. Al pedir costos se usa siempre el **handle exacto y el precio exacto** (importa en los duplicados).

| # | Nivel | Producto (handle) | Precio |
|---|---|---|---|
| 1 | Bajo | Gel Exótico (`gel-exotico-1`) | 18.000 |
| 2 | Medio | Dildo Doble Twin Fork Purple (`dildo-doble-twin-fork-purple`) | 79.900 |
| 3 | Medio/alto | Masajeador ava (`masajeador-ava`) | 129.900 |
| 4 | Alto | Bala Vibradora Winyi Brandy Silicona Premium (`bala-vibradora-winyi-brandy-silicona-premium`, la de 219.900) | 219.900 |
| 5 | Masculino (opcional) | Super huevo masturbador (`huevo-masturbador-super`) | 48.000 |
| — | Extra informativo | Succionador Honey (`succionador-honey`): pedir su costo es gratis y no sesga la muestra | 240.000 |

**Costos de catálogo y matches de la muestra:** ver `METRICS.md` §3.1 (`CATALOG_COST_2024`/`CATALOG_COST_2025`, no confirmados). Hallazgos que cambian las preguntas:
- Gel Exótico: 18.000 = 37 ml, 41.000 = 250 ml, 61.000 = 500 ml y sachet 5.000: es el mismo producto en distintas presentaciones (el catálogo Erotic además trae una de 20 ml a 15.000, que la tienda no vende).
- La "Bala Brandy" de 179.900 corresponde por foto y precio a **Winyi Crystal**, no a Brandy.
- "Masajeador ava" es el de Fara (Cod 11105); Winyi tiene otro con el mismo nombre.

**Preguntas al proveedor derivadas:** ¿los precios de catálogo 2024/2025 siguen vigentes? ¿incluyen IVA? ¿mínimos y descuentos? ¿ref. y empaque reales de "BIG DOUBLE" (Cod 10376)? ¿existe la presentación de 20 ml del Gel Exótico? ¿qué colores de Honey hay?

## 3. Logística — incógnitas (se resuelven en 0b)

| Tema | Estado |
|---|---|
| **Configuración de envío actual en Shopify (hechos, captura del 2026-10-05):** 1 perfil general (aplica a los productos que no estén en otros perfiles; los nuevos se añaden por defecto) · 1 de 1 sucursal · ubicación de procesamiento configurada en Barranquilla, Colombia · **1 zona doméstica (Colombia) con 2 tarifas: $14.951 COP para pedidos de $0 a $162.599 COP; gratis desde $162.600 COP** · fechas estimadas de entrega desactivadas · entrega local desactivada · retiro en tienda desactivado · sin cuenta de transportadora conectada. Si las tarifas son correctas: se evalúa en 0b. | RECIBIDO (configuración actual) |
| Recogida del producto y almacenamiento temporal | UNKNOWN |
| Empaque discreto (diseño, costo) | UNKNOWN |
| Mensajería en Barranquilla (quién, costo, tiempo) | UNKNOWN |
| Envíos al resto de Colombia (transportadora, costo, tiempo) | UNKNOWN |
| Plazo prometido por zona | UNKNOWN (no se publica hasta verificar) |
| Costo de envío al cliente / umbral de envío gratis | Configuración actual en Shopify: $14.951 COP hasta $162.599 COP; gratis desde $162.600 COP (sin evaluar). Costo real de envío: UNKNOWN |
| Pago contra entrega (Wompi no lo cubre; ¿alternativa?) | UNKNOWN |
| Política de cambios y devoluciones (revisar retracto en venta a distancia con contador/abogado) | En Shopify hay una política de devoluciones y reembolsos **publicada** (contenido no revisado); no hay reglas de devolución/cancelación predeterminadas. Política operativa: UNKNOWN |
| Entrega fallida / paquete perdido / dañado | UNKNOWN |
| Hora de corte para despacho | UNKNOWN |
| **Canal de atención al cliente y comunicación postventa.** WhatsApp Business: el texto oficial vigente lo prohíbe para la categoría "Adult products and services" y **no distingue atención de venta** (ver `BRAND_AND_AUDIENCE.md` §3.2); Vibrabien lo tiene enlazado desde la web. | UNKNOWN — decidir en 0b |
| **Inventario en Shopify — modelo actual:** inventario virtual/sentinel (~10.000 por producto, algunos 100.000; política `deny`), configurado deliberadamente por Michael para evitar productos agotados. No son unidades físicas de Vibrabien. Se compra al proveedor después del pedido. **Disponibilidad en Shopify representada mediante stock virtual alto; no sincronizada con stock físico del proveedor.** Riesgo: Shopify = disponible mientras el proveedor está temporalmente agotado. Hoy los 124 productos publicados figuran como disponibles en el catálogo público. | Hecho confirmado. Proceso de confirmación de disponibilidad: TO DESIGN — 0b |
| Actualización masiva de los 124 productos el 2026-10-05 ~17:51 (autor y causa) | UNKNOWN |
| Producto con inventario 0 reportado (¿intencional?) | UNKNOWN |
| ¿El tema muestra cantidades de inventario al público? | UNKNOWN |
| Privacidad: cómo se guardan direcciones y compras de clientes; qué ven los mensajeros | UNKNOWN |

## 4. Simulacro (0b — diseño en §9.7 y §9.8; NO se ejecuta hasta el GATE B)

- **A:** pedido → proveedor → Michael → cliente en Barranquilla.
- **B:** pedido → proveedor → Michael → otra ciudad.

Medir: hora del pedido · hora de compra al proveedor · disponibilidad · tiempo hasta recibir el producto · empaque y su costo · tiempo y costo de mensajería · tiempo total · problemas · margen final.

## 5. Modelos de inventario (hipótesis; sin decisión)

- **A:** 100 % bajo pedido.
- **B:** stock mínimo de 1-3 productos de mayor rotación.
- **C:** híbrido.

No se compra stock "para sentir que el negocio está más preparado". Se decide con costo, margen, rotación, disponibilidad, tiempo del proveedor, volumen mínimo y producto estrella conocidos.

## 6. Procedimiento de cumplimiento de un pedido (SOP)

**Diseño manual en borrador (GATE A, 2026-10-06; NO ejecutado):** ver §9.1 a §9.6 (flujo, estados, excepciones, confirmación de stock, ficha económica y modelo temporal). Se ejecuta solo después del GATE B.

## 7. Wompi: registro histórico — DEFERRED / NON-BLOCKING

> Por decisión de Michael (DEC-020), Wompi es técnicamente funcional y **no bloqueante para el trabajo actual**; la investigación de elegibilidad, panel, tarifas y reglamentos queda diferida. Esta sección se conserva como registro histórico. **Recuperar el acceso al panel no es condición para continuar el trabajo actual.**

### 7.1 Qué convendría saber si se reabre el tema (diferido)

Michael **no tiene acceso al panel de Wompi** (hecho; no se asume problema legal ni de propiedad). Si en el futuro se reabre el tema y antes de escalar con clientes reales, convendría saber:

- quién administra la cuenta y quién es el titular o autorizado;
- cómo puede Vibrabien consultar transacciones;
- cómo se hacen los reembolsos;
- quién recibe los fondos;
- cómo se gestionan los contracargos (el modelo Gateway/Agregador cambia quién los gestiona; el de Vibrabien es UNKNOWN);
- cómo se recupera o delega el acceso.

### 7.2 Borrador de consulta (NO ENVIADA / DEFERRED)

Debe enviarla el titular, el representante legal o un contacto autorizado que pueda autenticarse ante Wompi. No se pide a Wompi que revele datos de usuarios autorizados a quien no pueda autenticarse. **La descripción de la actividad debe ser completa y veraz: no se omite ni se suaviza la naturaleza del catálogo.** Entre corchetes, los datos que debe completar quien envíe.

> **Asunto:** Consulta sobre elegibilidad de actividad comercial y condiciones de la cuenta — [Razón social] — NIT [NIT]
>
> Buen día, equipo de Wompi:
>
> Somos [Razón social], titular del comercio [nombre del comercio / identificador en Wompi], que opera la tienda en línea vibrabien.co: comercio electrónico de productos para adultos de bienestar íntimo (incluye juguetes íntimos, lubricantes y accesorios), con ventas a nivel nacional.
>
> Revisamos el Reglamento de Comercios V4-2026. En la sección 14.8 no encontramos nuestra actividad entre las actividades restringidas, pero esa misma sección incorpora las restricciones de los reglamentos de las entidades financieras, las franquicias, las redes y otras entidades del sistema de pagos. Por eso solicitamos, por escrito:
>
> 1. **Elegibilidad:** ¿nuestra actividad está permitida en Wompi, incluidos los reglamentos de las entidades adquirentes (Bancolombia S.A. y AKUA Colombia Acquiring S.A.) y de las franquicias aplicables a nuestro modelo de registro? Si hay restricciones o condiciones (por ejemplo, sobre imágenes o descripciones de producto), ¿cuáles son?
> 2. **Clasificación:** ¿qué actividad económica figura declarada en el registro de nuestra cuenta y cómo se clasifica nuestro comercio internamente, incluido el riesgo de fraude?
> 3. **Modelo de registro:** ¿nuestra cuenta opera bajo el modelo Gateway o Agregador? ¿Quién gestiona los contracargos?
> 4. **Retenciones y reserva:** ¿hay hoy retenciones o fondo de reserva aplicados o previstos en nuestra cuenta? ¿Qué criterios los determinan y cómo se nos notificaría?
> 5. **Suspensión:** ¿existe aviso o revisión previa antes de una desactivación o suspensión?
> 6. **Tarifas** vigentes por método de pago y el **nombre que ve el comprador** en su extracto.
> 7. **Administración:** ¿cuál es el procedimiento para verificar la titularidad de la cuenta, recuperar el acceso al panel, crear o delegar usuarios autorizados, consultar operaciones y gestionar reembolsos y contracargos?
>
> Agradecemos una respuesta escrita que podamos conservar.
>
> Atentamente,
> [Nombre], [cargo], [correo], [teléfono]

## 8. Verificaciones de solo lectura pendientes (Michael)

- **Google & YouTube (tarea paralela, no bloqueante):** en Shopify → Canales de venta → Google & YouTube → Merchant Center / Productos, capturar **solo lectura**: si Merchant Center está conectado; cuántos productos están sincronizados; cuántos aprobados, desaprobados o pendientes; si aparece algún aviso de contenido para adultos, el atributo `adult` o una configuración `adult` de cuenta; y los países o mercados configurados. **No cambiar nada ni iniciar campañas.**
- **Proveedor:** llamada usando §2 y pedir el costo exacto de la muestra fijada (§2.1), con handle y precio exactos.
- **Actualización masiva del 2026-10-05:** ¿hizo Michael cambios masivos en los productos hoy?

## 9. Diseño de 0b — arquitectura operativa manual (GATE A) — NO EJECUTADO

**Estado:** diseño v0.1, 2026-10-06. Pregunta central: ¿puede Vibrabien recibir un pedido y cumplirlo correctamente, de forma repetible, discreta y económicamente entendible? **No se ejecuta nada** (ni pedidos, ni compras, ni simulacro, ni cambios en Shopify, precios, envíos o inventario, ni se quita el botón de WhatsApp, ni se publican promesas). El GATE B sigue cerrado. Todo UNKNOWN sigue siendo UNKNOWN: los valores marcados "objetivo de prueba" son metas para medir, no promesas ni supuestos. Lo que requiere criterio fiscal o legal se marca `REQUIRES POLICY / LEGAL REVIEW`.

**Actores:** **OP** = operador (Michael o quien él designe; quién más: UNKNOWN) · **MIC** = Michael como decisor · **PROV** = SexoSentido / SexoSentido Mayoristas · **TRANS** = mensajero o transportadora (UNKNOWN) · **CLI** = cliente.

### 9.1 Flujo happy path (de "Shopify registra el pedido" a "cliente recibe y confirma")

| # | Paso | Actor | Entra con | Sale con (se registra) | Si falla |
|---|---|---|---|---|---|
| 1 | Pedido recibido | Shopify → OP | Pedido creado | `order_id`, hora **T0**, líneas, dirección | Incompleto o duplicado → EXCEPCIÓN |
| 2 | Verificar pago | OP | Pedido "pagado" en Shopify | Pago verificado por la vía identificada (condición del GATE C); hora T0p | No verificable → EXCEPCIÓN `PAGO_NO_VERIFICABLE` |
| 3 | Registrar origen | OP | Pedido | `source_type` (`OPERATIVE`/`DEMAND`) y `source`; fila en `EXPERIMENT_LOG.md` | Origen desconocido: `other`; no bloquea |
| 4 | Identificar SKU/variante | OP | Líneas del pedido | `handle`, variante, precio, **código del proveedor** (tabla de equivalencias), cantidad | Sin código verificado → EXCEPCIÓN `SKU_SIN_REFERENCIA` (no se compra) |
| 5 | Confirmar disponibilidad real | OP → PROV | Mensaje por código (§9.4) | Respuesta y hora **T1** | Agotado o sin respuesta → EXCEPCIÓN |
| 6 | Confirmar costo vigente | OP → PROV | Mismo mensaje | `supplier_cost_current`, vigencia | Cambió → EXCEPCIÓN `COSTO_CAMBIO` |
| 7 | Decidir si se cumple | OP (MIC si hay excepción) | Datos de 5 y 6 | Decisión registrada: GO / HOLD / CANCEL | — |
| 8 | Comprar o reservar | OP → PROV | GO | `supplier_order_ref`, monto, forma de pago, factura sí/no | Rechazo o mínimo → EXCEPCIÓN |
| 9 | **Rama A:** recibir el producto · **Rama B:** despacho directo (solo si el proveedor lo confirma) | PROV / OP | Compra hecha | A: `inbound_cost`, hora **T2** (producto en manos del OP). B: el proveedor informa despacho | No llega en el plazo → EXCEPCIÓN |
| 10 | Inspección física (solo Rama A) | OP | Producto recibido | Lista: SKU correcto, cantidad, íntegro/sellado, coincide con la ficha (color, accesorios), foto | No coincide o está dañado → EXCEPCIÓN |
| 11 | Empaque discreto (solo Rama A) | OP | Producto aprobado | Exterior neutro sin mención del contenido; nombre de remitente (UNKNOWN); `packaging_cost`; hora **T3** | Faltan insumos → EXCEPCIÓN |
| 12 | Generar o coordinar el envío | OP → TRANS | Paquete listo | Operador elegido por zona, guía, `shipping_cost`, hora **T4** (entrega a TRANS) | No recoge o cuesta más → EXCEPCIÓN |
| 13 | Entrega | TRANS | Entrega a TRANS | Tracking, hora **T5** | Falla o pérdida → EXCEPCIÓN |
| 14 | Confirmación | CLI / OP | Entrega reportada | Confirmación de recepción por un canal permitido (UNKNOWN) o prueba de entrega | Sin confirmación → cerrar con prueba de entrega después de un plazo (`REQUIRES POLICY / LEGAL REVIEW`) |
| 15 | Cierre económico | OP | Pedido entregado | Ficha completa (§9.5) y margen | Datos faltantes → margen `INCOMPLETE` |

**Rama B (despacho directo):** queda como rama hasta que el proveedor responda. Si existe, salta los pasos 10 y 11 (se pierde la inspección y el empaque propio). Esa renuncia es una decisión de MIC, no un supuesto.
**Regla derivada del paso 4:** solo se cumplen pedidos de productos con código del proveedor verificado. Hoy la verificación cubre la muestra y un grupo de productos; **~20 productos de la tienda no cruzaron con ningún catálogo** (`METRICS.md` §3.2). Esto es un riesgo del GATE C.

### 9.2 Estados mínimos del pedido (siete, no once)

| Estado | Significa | Se entra si | Se sale si | Responsable |
|---|---|---|---|---|
| `NUEVO` | Shopify registró el pedido; pago sin verificar | Pedido creado | Pago verificado → `POR_CONFIRMAR`; no verificable → `EXCEPCION` | OP |
| `POR_CONFIRMAR` | Pago verificado; consultando stock y costo | Pago verificado | Proveedor confirma y MIC/OP decide GO → `EN_PREPARACION`; agotado o costo inaceptable → `EXCEPCION` | OP (PROV responde) |
| `EN_PREPARACION` | Compra hecha; producto en camino al OP, en inspección, empaque o a la espera de guía | Compra o reserva hecha | Entrega a TRANS → `DESPACHADO`; falla → `EXCEPCION` | OP |
| `DESPACHADO` | En poder de TRANS | Entrega a TRANS (T4) | Entrega verificada → `ENTREGADO`; falla → `EXCEPCION` | OP / TRANS |
| `ENTREGADO` | El cliente recibió; falta cerrar la economía | Entrega verificada (T5) | Ficha cerrada → `CERRADO` | OP |
| `EXCEPCION` | Algo se salió del flujo; **no es un paso lineal sino una marca**: guarda `estado_previo`, `tipo`, `decisor`, hora | Cualquier falla de §9.3 | Se resuelve y vuelve a `estado_previo`, o pasa a `CERRADO` | MIC |
| `CERRADO` con `resultado` | Pedido terminado | Ficha cerrada | — | OP |

`resultado` de `CERRADO`: `ENTREGADO_OK` · `CANCELADO` · `REEMBOLSADO`.
**Por qué no más estados:** no hay `PAYMENT_CONFIRMED` (es una puerta dentro de `NUEVO`) ni `READY_TO_SHIP` (es un tramo de `EN_PREPARACION`). **Dónde se lleva:** una fila por pedido en una hoja manual con los campos de §9.5; sin herramientas nuevas.

### 9.3 Matriz de excepciones (decisiones lógicas, no políticas)

| # | Excepción | Cómo se detecta | Opciones lógicas | Decide | Registrar | Marca |
|---|---|---|---|---|---|---|
| 1 | Proveedor sin stock | Respuesta "agotado" o sin respuesta | Esperar reposición (si hay fecha confiable y el cliente acepta); ofrecer un equivalente exacto con consentimiento; cancelar y reembolsar | MIC | Hora, fecha de reposición, SKU | `REQUIRES POLICY / LEGAL REVIEW` (cancelación, reembolso, consentimiento) |
| 2 | El costo cambió | `supplier_cost_current` ≠ costo registrado | Recalcular margen; GO si MIC acepta; si el margen sería negativo, HOLD y MIC decide | MIC | Costo nuevo, vigencia | Si cancela: `REQUIRES POLICY / LEGAL REVIEW` |
| 3 | Producto recibido no coincide | Inspección (SKU, color, accesorios) | No enviar; pedir cambio o crédito al proveedor; si no hay equivalente, como #1 | OP → MIC | Foto, descripción | Depende de la garantía del proveedor (GATE B) |
| 4 | Empaque dañado | Inspección | Si el producto está íntegro, reempacar; si no, rechazar y reclamar | OP | Foto | — |
| 5 | Pedido de varios productos y falta uno | Consulta de stock por línea | Envío parcial (con costo adicional), esperar, cancelar la línea | MIC | Líneas y tiempos | `REQUIRES POLICY / LEGAL REVIEW` (parcial, reembolso parcial, costo) |
| 6 | Dirección parece incorrecta | Validación al registrar (ciudad, barrio, teléfono) | Contactar al cliente por un canal permitido antes de despachar; no despachar hasta confirmar | OP | Dato corregido, hora | `REQUIRES POLICY / LEGAL REVIEW` (tratamiento de datos personales) |
| 7 | El envío cuesta más de lo esperado | Cotización > costo esperado | Absorber (queda como `shipping_subsidy`), cambiar de operador | MIC | Cotizaciones | Cobrar la diferencia al cliente: `REQUIRES POLICY / LEGAL REVIEW` |
| 8 | TRANS no recoge | Sin recogida en la ventana acordada | Reintentar, otro operador, llevar el paquete a un punto | OP | Horas | — |
| 9 | Entrega fallida | Tracking "no entregado" | Contactar al cliente, reprogramar, devolución a origen; registrar el costo extra | OP | Intentos, costo | Reenvío o cobro: `REQUIRES POLICY / LEGAL REVIEW` |
| 10 | Paquete perdido | Sin movimiento o fuera de plazo | Reclamo a TRANS; reponer con nueva compra o reembolsar | MIC | Guía, reclamo | `REQUIRES POLICY / LEGAL REVIEW` (responsabilidad, seguro) |
| 11 | Cliente pide cancelar | Solicitud del cliente | Antes de comprar al proveedor: cancelar y reembolsar; después: opciones según estado | MIC | Hora de la solicitud, estado | `REQUIRES POLICY / LEGAL REVIEW` (retracto en venta a distancia) |
| 12 | Cliente pide cambio | Solicitud | Evaluar caso | MIC | Motivo | `REQUIRES POLICY / LEGAL REVIEW` (higiene, garantía) |
| 13 | Cliente pide devolución | Solicitud | Evaluar caso; requiere una vía identificada para reembolsar | MIC | Motivo | `REQUIRES POLICY / LEGAL REVIEW` (retracto, garantía, higiene) |
| 14 | Pago en Shopify no verificable | No se confirma el cobro por la vía identificada | No comprar al proveedor; esperar verificación; si no se confirma, cancelar | MIC | Evidencia | Depende de la condición del GATE C sobre pagos y reembolsos |
| 15 | La publicación tiene información incorrecta | Inspección o reclamo | Detener el cumplimiento de ese SKU; contactar al cliente; corrección **agrupada** (no cambios individuales) | MIC | Discrepancia | `REQUIRES POLICY / LEGAL REVIEW` (claims e información al consumidor) |
| 16 | Proveedor sin respuesta | Vence el tiempo de §9.4 | Escalar, no comprar, no prometer | MIC | Horas, canal | — |

### 9.4 Confirmación de stock (manual)

- **Cuándo:** el mismo día hábil, **después de verificar el pago y antes de comprar**; no se consulta al publicar. Estado: `POR_CONFIRMAR`.
- **Cómo se identifica el producto:** mensaje de plantilla con marca, **código/ref/SKU**, nombre del catálogo, variante o color, cantidad y `order_id` interno. Nunca solo por nombre: "Ava" y "Crystal" existen en dos marcas distintas con productos diferentes. Para duplicados de la tienda se usa siempre el handle y el precio exactos.
- **Canal:** el que el proveedor indique en el GATE B. **No se asume WhatsApp Business:** la política de esa plataforma prohíbe comprar, vender o promover productos para adultos, y comprarle al proveedor podría caer ahí (`REQUIRES POLICY / LEGAL REVIEW`). Alternativas: llamada o correo.
- **Cuánto se espera:** tres tiempos. **W1** = respuesta esperada; **W2** = reintento por un segundo contacto; **W3** = pasa a `EXCEPCION` `SIN_RESPUESTA`. Sus valores se fijan después del GATE B con lo que el proveedor declare; para el simulacro, **objetivo de prueba: respuesta el mismo día hábil**.
- **Qué se registra:** `stock_query_at`, `stock_response_at`, quién respondió, `availability_status` (`DISPONIBLE` / `AGOTADO` / `CONDICIONAL` con fecha / `SIN_RESPUESTA`), cantidad confirmada, fecha de reposición, `supplier_cost_current`, vigencia, canal y notas.
- **Sin respuesta:** reintento en W2; en W3 pasa a `EXCEPCION`; no se compra y no se promete.
- **Agotado:** `EXCEPCION` con las opciones de la fila 1 de §9.3. Se anota el SKU en una lista manual de **SKU con riesgo de agotado**; ajustar la disponibilidad en Shopify es una decisión posterior de Michael, no de este diseño.
- **Métricas:** tiempo de respuesta, % de confirmaciones, % de agotados.

### 9.5 Ficha económica por pedido

Una fila por pedido; `NULL` = no medido todavía (no se rellena con supuestos).

| Campo | Fuente | Regla |
|---|---|---|
| `order_id`, fecha, `source_type`, `source` | Shopify / registro | — |
| Líneas: `handle`, código del proveedor, cantidad | Shopify / tabla de equivalencias | — |
| `sale_price` | Shopify | Precio del producto, sin envío |
| `shipping_charged_to_customer` | Shopify | 14.951 hasta 162.599; gratis desde 162.600 (configuración actual) |
| `supplier_cost_current` | PROV | Costo vigente; se compara con el costo de catálogo (`cost_delta`) |
| `shopify_transaction_fee` | Shopify | **Observado**; se contrasta con la estimación del 2 %. La base del 2 % (con o sin envío): UNKNOWN |
| `payment_processing_fee` | Wompi | **`NULL`**: diferido por DEC-020; sin panel no hay forma de observarlo |
| `inbound_cost` | OP | Costo de llevar el producto del proveedor a Vibrabien; `0` o `NULL` según la rama |
| `packaging_cost` | OP | Insumos medidos |
| `shipping_cost` | TRANS | Cotizado y real |
| `shipping_subsidy` | Calculado | `max(shipping_cost − shipping_charged_to_customer, 0)` |
| `returns_cost` | OP | `NULL` salvo que haya devolución |
| `tax_treatment`, `invoice` | Fiscal | UNKNOWN / `REQUIRES POLICY / LEGAL REVIEW` |
| `T0`…`T5` | OP | Hora de cada hito (§9.6) |
| `operator_minutes` | OP | Minutos del operador por pedido; se mide pero no se costea |

**Márgenes (nombres explícitos; ninguno es utilidad neta):**
- `PRE_FULFILLMENT_MARGIN_EX_WOMPI = sale_price − supplier_cost_current − shopify_transaction_fee` (ya usado en `METRICS.md`).
- `FULFILLMENT_MARGIN_EX_WOMPI = sale_price − supplier_cost_current − shopify_transaction_fee − packaging_cost − inbound_cost − shipping_subsidy − returns_cost`. **Es el resultado principal esperado de 0b**, porque Wompi seguirá en `NULL`.
- `contribution_margin` = lo anterior menos `payment_processing_fee`. **Solo se calcula si ningún campo requerido es `NULL`**; si no, `margin_status = INCOMPLETE` y se reporta el margen parcial con su nombre.
- El excedente de envío (`max(shipping_charged − shipping_cost, 0)`) se anota aparte y no entra en el margen, igual que en la fórmula vigente.
- **Cambio propuesto a `METRICS.md`:** la fórmula de contribución no incluye `inbound_cost`; propongo añadirlo.

**Qué UNKNOWN convierte el simulacro en dato:** `supplier_cost_current`, la base real del cargo de Shopify, `packaging_cost`, `inbound_cost`, `shipping_cost` (local y nacional), tiempos de cada tramo, tiempo del operador. **No los convierte:** Wompi, impuestos y devoluciones.

### 9.6 Modelo temporal para la promesa (calcula la promesa; no la fija)

`ORDER_TIME (T0)` → `PAGO VERIFICADO (T0p)` → `PROVEEDOR CONFIRMA (T1)` → `PRODUCTO LISTO (T2)` → `EMPACADO (T3)` → `ENTREGA A TRANS (T4)` → `ENTREGADO (T5)`.

| Tramo | Duración | Notas |
|---|---|---|
| Verificación | T0p − T0 | Depende del método de verificación del pago |
| Confirmación | T1 − T0p | Tiempo de respuesta del proveedor; incluye esperas fuera de horario |
| Abastecimiento | T2 − T1 | Plazo proveedor → Vibrabien (o despacho directo); su ubicación: UNKNOWN |
| Preparación | T3 − T2 | Inspección y empaque |
| Espera de recogida | T4 − T3 | Programar al operador |
| Tránsito | T5 − T4 | **Cambia por zona** |

- Se registran las horas reales y de ahí se derivan días calendario y hábiles.
- **Barranquilla frente al resto de Colombia:** cambian el tránsito (mensajería local frente a transportadora nacional) y la espera de recogida; el abastecimiento puede cambiar si el proveedor no está en Barranquilla (UNKNOWN).
- **Regla de construcción de la promesa (el valor lo decide Michael):** `promesa(zona) ≥` peor tiempo observado en cada tramo + un margen que Michael fije. Con n pequeño no se publica nada: la promesa pública se decide **después** del simulacro. Las fechas estimadas de entrega de Shopify siguen desactivadas hasta entonces.
- Se anota el efecto del horario de corte del proveedor.

### 9.7 SIMULACRO A — Barranquilla (solo diseño)

**Condiciones comunes a A y B (pre-registro):** antes de empezar se escriben los valores esperados (plazo del proveedor, tránsito del operador, costo) y el presupuesto de tiempo, para no juzgar después. Un comprador de confianza (Michael u otra persona) compra **como cliente normal por la tienda**, con pago real, una unidad, sin promociones. Se registra como `OPERATIVE`. La factura y el tratamiento fiscal de estas compras: `REQUIRES POLICY / LEGAL REVIEW`. **Requisito previo: GATE B cumplido.**

| Elemento | Diseño |
|---|---|
| **Producto** | **Masajeador Ava** de Fara (`masajeador-ava`; Cod 11105 · Ref SHD-S082; precio 129.900; costo de catálogo 2025: 69.900, no vigente) |
| **Por qué** | Costos doblemente verificados; EXACT SAME SKU en el competidor y en el catálogo; según el cruce heurístico de `METRICS.md` §3.2, la mayoría de los productos de la tienda cruza con el catálogo de Fara; ticket medio por debajo del umbral de envío gratis (el cliente paga 14.951); caja pequeña y con marca, lo que prueba el empaque discreto; costo de efectivo moderado |
| **Alternativa de bajo costo** | Super Huevo de Winyi, si el efectivo en riesgo es una preocupación |
| **Inicio** | `T0` = hora en que se realiza el pedido en la tienda, con dirección de entrega en Barranquilla |
| **Pasos** | Los 15 pasos de §9.1, con cronómetro en cada hito |
| **Cronómetro** | `T0`, `T0p`, `T1`, `T2`, `T3`, `T4`, `T5` y los minutos del operador por paso |
| **Datos a registrar** | Canal y hora de la consulta; respuesta y quién respondió; disponibilidad; costo vigente y vigencia; `supplier_order_ref` y forma de pago; método de recepción; resultado de la inspección con fotos; materiales de empaque; operador y guía; confirmación de entrega; cualquier anomalía |
| **Costos a registrar** | `supplier_cost_current`, `inbound_cost`, `packaging_cost`, `shipping_cost` (y todas las cotizaciones), `shopify_transaction_fee` observado, `payment_processing_fee` = `NULL` |
| **PASS** | (1) todos los hitos y costos registrados, salvo los declarados UNKNOWN (Wompi, impuestos, devoluciones); (2) el stock se confirmó con el método definido; (3) entregado en la dirección correcta, con el SKU correcto e íntegro; (4) el exterior no revela el contenido (verificado con foto); (5) el tiempo total cabe en el presupuesto fijado antes, o la desviación está explicada; (6) `FULFILLMENT_MARGIN_EX_WOMPI` calculado con insumos reales y ≥ 0; (7) sin incidente de datos personales |
| **FAIL** | No entregado o perdido sin vía de recuperación; producto equivocado o dañado sin resolución; el empaque revela el contenido; el proveedor no puede confirmar disponibilidad con el método; `FULFILLMENT_MARGIN_EX_WOMPI` < 0; pedido sin trazabilidad |
| **Obliga a rediseñar** | Plazo del proveedor incompatible con cualquier promesa; costo de transporte mayor que el margen; recogida local que no funciona; empaque original que delata el contenido; respuesta del proveedor fuera de horario sistemática |

### 9.8 SIMULACRO B — otra ciudad de Colombia (solo diseño)

| Elemento | Diseño |
|---|---|
| **Ciudad** | La decide Michael. Criterios: destinatario de confianza y destino típico. Referencia: Bogotá es la ciudad con más sesiones fuera de Barranquilla en Shopify Analytics (40), pero no es una prueba de demanda |
| **Producto** | **Super Huevo de Winyi** (`huevo-masturbador-super`; WY0632 · SKU 13047; precio 48.000; costo de catálogo 2025: 24.900, no vigente) |
| **Por qué** | Cubre la segunda marca (Winyi); costo doblemente verificado y n=3 de precio en el benchmark; mínimo efectivo en riesgo; caja pequeña y ligera, que mide el costo de envío nacional sobre un producto barato (el cliente paga 14.951 sobre 48.000) |
| **Extensión opcional** | La Brandy (219.900) probaría el tramo de envío gratis, pero su costo de efectivo (112.900) es mayor. Como el costo de envío se mide igual con cualquier producto, esa extensión es contable y no urgente |
| **Inicio, pasos, cronómetro** | Igual que A, con dirección en la otra ciudad |
| **Datos adicionales** | Operador nacional y servicio elegidos; recogida; seguro o declaración de valor; datos del remitente en la guía; tiempo por tramo; comparación local frente a nacional |
| **Costos** | Los de A, más cualquier recargo por zona |
| **PASS** | Los mismos criterios que A; además, el tránsito nacional queda medido y cabe en el presupuesto fijado antes |
| **FAIL** | Los mismos criterios que A; además, la guía o la factura visible expone el contenido |
| **Obliga a rediseñar** | Costo nacional mayor que el margen del producto; tránsito sin trazabilidad; el operador nacional no recoge; daños en tránsito; remitente que revela la categoría |

### 9.9 Criterios de 0b (PASS / PASS WITH CONDITIONS / FAIL / PENDING)

| Dimensión | PASS | PASS WITH CONDITIONS | FAIL | PENDING |
|---|---|---|---|---|
| **Disponibilidad** | El proveedor confirma por el método definido dentro del objetivo en A y B | Confirma, pero fuera del objetivo o por un canal informal | No confirma, o confirma y no entrega | Sin simulacro |
| **Tiempo** | T0→T5 medido en ambas zonas y dentro del presupuesto previo | Medido, pero fuera del presupuesto: la promesa será más larga | No entregado, o un tramo no se puede medir | Sin simulacro |
| **Costo** | `supplier_cost_current`, `inbound_cost`, `packaging_cost` y `shipping_cost` medidos con fuente | Algún componente estimado | Algún componente no se puede obtener | Sin dato |
| **Discreción** | El exterior no identifica el contenido en ninguna zona | Mejorable, sin revelar | Revela el contenido | Sin simulacro |
| **Integridad** | SKU correcto, íntegro y coincide con la ficha | Diferencia menor con resolución | Equivocado o dañado sin resolución | Sin simulacro |
| **Trazabilidad** | `order_id` ↔ pedido al proveedor ↔ guía, con todos los hitos | Falta algún hito no crítico | No se puede reconstruir el pedido | Sin simulacro |
| **Excepciones** | Cada fila de §9.3 tiene responsable y decisión lógica, y se ensayó al menos stock y sin respuesta en papel | Quedan `REQUIRES POLICY / LEGAL REVIEW` pendientes | Una excepción crítica sin responsable | No ensayadas |
| **Margen** | `FULFILLMENT_MARGIN_EX_WOMPI` ≥ 0 en A y B, y componentes restantes conocidos | Positivo, con Wompi, impuestos o devoluciones UNKNOWN | Negativo | Sin cálculo |

**Regla global (propuesta):**
- **PASS:** todas las dimensiones en PASS. **Expectativa realista:** Margen no pasa de `PASS WITH CONDITIONS` mientras Wompi y los impuestos sigan UNKNOWN (DEC-020).
- **PASS WITH CONDITIONS:** ninguna en FAIL y los dos simulacros ejecutados. Las condiciones quedan escritas; el alcance puede limitarse a ciertos productos o zonas.
- **FAIL:** FAIL en Disponibilidad, Integridad, Discreción o Trazabilidad, o margen negativo en ambos simulacros. Implica rediseñar el modelo; no es un fallo del baseline.
- **PENDING:** falta un simulacro o un dato clave.
- No se fija un margen mínimo: el único umbral es el signo (≥ 0).

### 9.10 Preguntas mínimas al proveedor para abrir el GATE B

**MUST KNOW BEFORE SIMULATION (siete preguntas; la llamada se reduce a esto):**

| # | Pregunta | Para qué |
|---|---|---|
| M1 | ¿Por qué canal y con quién confirmo la disponibilidad de un producto por código, en qué horario, y en cuánto tiempo suele responder? ¿A quién escalo si no responden? | Método de confirmación de stock, horario y corte |
| M2 | ¿Cuál es el costo **vigente** del Ava (11105) y del Super Huevo (13047), hasta cuándo es válido y **incluye IVA**? | Costo vigente de los productos del simulacro; sin saber si incluye IVA no se interpreta el margen |
| M3 | ¿Hay mínimo de compra? ¿Puedo comprar una sola unidad? | El simulacro es de una unidad |
| M4 | ¿Cómo y cuándo se paga (antes de entregar, contra entrega, crédito)? | Pago al proveedor |
| M5 | ¿Cómo llega el producto a Vibrabien (recogida, mensajería, entrega), quién lo paga y cuánto tarda desde "comprado" hasta "listo"? | Plazo proveedor → Vibrabien y `inbound_cost` |
| M6 | ¿Puede despachar directo al cliente final con empaque neutro? Si sí, ¿a qué costo? | Decide la Rama A o B |
| M7 | Si llega dañado o equivocado: ¿lo cambian o lo reembolsan, y en qué plazo? | Garantía básica; el simulacro compra con dinero real |

**USEFUL BUT NOT BLOCKING:** frecuencia de cambio de existencias · productos que suelen agotarse · tiempo de reposición · aviso previo de agotados · listado de disponibilidad actualizado · estabilidad de precios · costo vigente del resto de la muestra (Gel Exótico, Twin Fork, Brandy, Honey) · vigencia de los catálogos 2024/2025 · si facturan cada compra y a nombre de quién (condición del GATE C) · exclusividad, prioridad de inventario, condiciones para revendedores y política de precios · materiales y autenticidad · fotos · segundo proveedor.

**Dónde difiere esta lista del GATE B tal como está escrito:** el GATE B pide "costo vigente de la muestra". Para ejecutar el simulacro bastan los dos productos del simulacro (M2); el resto es útil para la economía, pero no bloquea. Las demás condiciones del GATE B quedan cubiertas por M1 a M7. **Esto debe aceptarlo Michael antes de aplicarlo.**
