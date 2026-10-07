# METRICS.md

**Versión:** 1.0 (cierre de 0a: PASS WITH CONDITIONS, DEC-021; proveedor confirmado) · **Creado:** 2026-10-05
Ningún valor de este documento se inventa: todo es `UNKNOWN` hasta que llegue la fuente. Los valores marcados *(derivado)* son aritmética sobre datos recibidos, no datos de Shopify.

## 1. Datos de 0a — estado de recolección

| ID | Dato | Fuente | Estado |
|---|---|---|---|
| D1 | Fecha de lanzamiento de la tienda y plan de Shopify | Michael / Shopify | **CONFIRMADO** — lanzamiento ~marzo 2026; plan **Basic**, facturación anual, **264 USD/año** (captura de Shopify) |
| D2 | Embudo: sesiones → carrito → checkout → compra (desde lanzamiento hasta 90 días) | Shopify | RECIBIDO — rango 1 ene–5 oct 2026 (incluye ~2 meses previos al lanzamiento); serie mensual PENDING |
| D3 | Sesiones por fuente, dispositivo y ubicación | Shopify | RECIBIDO (cifras aproximadas, redondeadas por Shopify) |
| D4 | Pedidos: total, de prueba, reales, cancelados, reembolsados (solo conteos) | Shopify / Michael | PARCIAL — total 3, pruebas 3, reales 0; reembolsos de prueba: 0 según Michael (el dinero permanece en Wompi); **cancelaciones UNKNOWN** |
| D5 | Fechas aproximadas de visitas y pruebas propias de Michael | Michael | PARCIAL — los 3 pedidos son de Michael, hechos entrando a vibrabien.co como cliente normal (sitio → producto/carrito → checkout → Wompi → pago); **fechas PENDING**; origen de su tráfico en el informe: UNKNOWN |
| D6 | Catálogo exportado (precios, costo por artículo, seguimiento de inventario) | Shopify | PARCIAL — catálogo público vivo leído por Claude (124 productos; §2.1); el CSV reportado era un **export parcial de 50 productos**; costos e inventario por producto siguen sin verificar |
| D7 | Canales de venta y apps instalados y activos | Shopify | PARCIAL — canales y apps visibles conocidos; Google & YouTube parcialmente caracterizado (§2.2); **Merchant Center / catálogo / campañas / Google Shopping: UNKNOWN**; función de las 4 apps y de Headless y Point of Sale: UNKNOWN |
| D8 | Zonas/tarifas de envío vigentes; métodos de pago de Wompi activos | Shopify | **RECIBIDO para la configuración actual** — Wompi activo, PayPal inactivo, cargo de 2 %; 1 zona (Colombia) con 2 tarifas; demás hechos de entrega registrados (§2.2). La comisión propia de Wompi sigue en D13. |
| D9 | Píxeles/integraciones activas, qué datos de clientes envían, configuración de privacidad | Shopify | PARCIAL/RECIBIDO — píxeles identificados y configuración de privacidad capturada (§2.2); **falta saber qué datos exactos envía GTM** y detalles relevantes |
| D10 | Tienda pública, páginas de políticas, analítica instalada | Shopify | PARCIAL — políticas publicadas identificadas (contenido **no revisado**); analítica: ver D9; tienda pública / contraseña / dominio: UNKNOWN |
| D11 | Instagram: tipo de cuenta, enlace/botones, etiquetado de productos, métricas de 30 días | Instagram / Michael | PARCIAL — seguidores: 59; "2 vistas" reportadas por Instagram en el último mes (tipo exacto de métrica pendiente de confirmar); el resto (alcance, visitas al perfil, toques en el enlace, mejor contenido, tipo de cuenta, funciones comerciales) OPEN |
| D12 | Rastro de WhatsApp: enlaces/botones, cuenta/catálogo de WhatsApp Business, apps instaladas | Michael / observación de la web pública | PARCIAL — **cuenta WhatsApp Business CONFIRMADA** (Michael); **botón flotante y enlace del pie de página CONFIRMADOS** (observados, §2.4); catálogo, enlace/botón en Instagram y conversaciones originadas desde la web: UNKNOWN |
| D13 | Wompi: comisión, nombre en el extracto, avisos de cuenta, actividad declarada al registrarse | Wompi / Michael | **DEFERRED / NON-BLOCKING** (DEC-020, decisión de Michael). Wompi es técnicamente funcional: activo en Shopify, 3 compras por el flujo normal, cobros funcionaron y el dinero llegó a Wompi (según Michael; no reembolsado). Michael no tiene acceso al panel. **UNKNOWN:** panel, transacciones verificadas, montos exactos, comisión, actividad/categoría declarada, avisos, nombre en el extracto, autorización de la categoría. **No equivale a ACEPTADO CONFIRMADO.** |
| D14 | Proveedor: costo de la muestra y respuestas de llamada (ver `OPERATIONS.md` §2) | Proveedor / catálogos | **PARCIAL** — costos de catálogo (`CATALOG_COST_2024` / `CATALOG_COST_2025`) y match verificado por imagen para los 5 productos de la muestra y el extra (§3.1); **no son costos vigentes confirmados**; respuestas del proveedor PENDING |
| D15 | Precios de 2-3 competidores para la muestra | IAs | **PARCIAL / SUFICIENTE PARA 0a** — benchmark del 2026-10-06 en §3.3, reconciliado con ChatGPT: Super Huevo n=3; Gel Exótico 37 ml n=5 (2 EXACT SAME SKU + 3 SAME PRODUCT / HIGH, estos reportados por ChatGPT); Twin Fork, Ava, Brandy y Crystal con comparación limitada (n=1); Honey sin comparación; no se exigen 3 vendedores exactos por producto |
| D16 | Estado fiscal y si el precio de venta incluye IVA | Michael | PARCIAL — **empresa** (Michael); facturación UNKNOWN; tratamiento del IVA UNKNOWN |

**Reglas de lectura:** separar siempre pedidos de prueba y tráfico propio de los reales. Con pocas visitas, el tráfico propio y bots pueden dominar: registrarlo como limitación, no ocultarlo. Datos insuficientes = *brecha de medición*, no fallo.

### 1.1 Cierre del Día 1 — COMPLETADO CON PENDIENTES — APROBADO

Un baseline puede contener `UNKNOWN`, `OPEN`, `BLOCKED` y `PENDING VERIFICATION`. No se exige que todos los D-items estén confirmados.

| Grupo | D-items |
|---|---|
| Confirmado / recibido | D1 · D2 · D3 · D8 (configuración actual) |
| Parcial | D4 · D5 · D6 · D7 · D9 · D10 · D11 · D12 · D16 |
| **DEFERRED / NON-BLOCKING** (DEC-020) | D13 (Wompi) |
| No iniciados por diseño (Día 2+) | D14 (proveedor) · D15 (precios de competidores) |

**OPEN / BLOCKED que pasan a días posteriores (nada se resuelve en el Día 1):**
- **D13:** DEFERRED / NON-BLOCKING (DEC-020). Comisión, panel, transacciones verificadas, categoría declarada, avisos y extracto: UNKNOWN. No es prerrequisito del trabajo actual.
- **D6:** CSV actual (verificación independiente de los 50 productos).
- **D9:** confirmación de GA4 (evidencia parcial por etiqueta `G-`); qué recibe GTM.
- **D11:** tipo exacto de la métrica de "2 vistas"; alcance, visitas al perfil, toques en el enlace, tipo de cuenta.
- **D12:** catálogo de WhatsApp; enlace en Instagram; conversaciones originadas desde la web.
- **D16:** facturación; tratamiento del IVA.
- **D4/D5:** cancelaciones; fechas de las pruebas. **D2/D3:** serie mensual.
- **D7/D9:** Headless, POS, los 2 mercados de Google, Merchant Center/catálogo/campañas, Council Bluffs, función de las apps instaladas, Mercado Pago en Pagos, estado de Facebook & Instagram y Shop.
- **D6/D10:** producto con inventario 0, si el tema muestra cantidades, contenido jurídico de las políticas.
- **Anomalía del embudo** (3 pedidos vs. 0 completados), conflicto WhatsApp–DEC-005 y REVIEW de Network Intelligence: abiertos.

**Dato indispensable para el veredicto de 0a:** no se identifica ninguno nuevo sin día previsto. **Prerrequisito del Día 2 (cumplido):** fijar la muestra de productos de D14 **antes** de ver costos. *(Histórico: el 2026-10-05 se había añadido como prerrequisito identificar al administrador de Wompi; DEC-020 lo retira del camino crítico.)*

### 1.2 Estado final de D1-D16 al cierre de 0a (DEC-021, 2026-10-06)

| D | Estado final | Qué queda abierto |
|---|---|---|
| D1 | **CONFIRMADO** | — (plan Basic anual, 264 USD/año; lanzamiento ~marzo 2026) |
| D2 | RECIBIDO | Serie mensual; anomalía "0 pagos completados" vs. 3 pedidos (medición/atribución) |
| D3 | RECIBIDO (aproximado) | ~59 % de las sesiones desde Council Bluffs sin explicar |
| D4 | PARCIAL | Cancelaciones UNKNOWN |
| D5 | PARCIAL | Fechas de las pruebas y visitas propias |
| D6 | PARCIAL | Catálogo vivo de 124 productos verificado; el CSV era un export parcial de 50; costo por artículo vacío en Shopify; inventario virtual |
| D7 | PARCIAL | Merchant Center, sincronización de catálogo y campañas UNKNOWN; función de Headless, POS y apps UNKNOWN |
| D8 | RECIBIDO (configuración actual) | La comisión de Wompi está en D13 |
| D9 | PARCIAL / RECIBIDO | GA4 UNKNOWN; qué datos envía GTM; REVIEW de Network Intelligence |
| D10 | PARCIAL | Políticas publicadas, contenido sin revisar; contraseña y dominio UNKNOWN |
| D11 | PARCIAL | 59 seguidores; "2 vistas" con métrica por confirmar; resto OPEN |
| D12 | PARCIAL | WhatsApp Business confirmado; catálogo de WhatsApp, enlace en Instagram y conversaciones UNKNOWN; decisión del botón en GATE C |
| D13 | **DEFERRED / NON-BLOCKING** (DEC-020) | Comisión, panel, categoría declarada y demás: UNKNOWN |
| D14 | PARCIAL | Costos de catálogo 2024/2025 (no vigentes), matches verificados; costos vigentes y respuestas del proveedor son GATE B |
| D15 | **PARCIAL / SUFICIENTE PARA 0a** | Comparación limitada para varios SKU; Honey sin comparación |
| D16 | PARCIAL | Empresa; facturación e IVA UNKNOWN (GATE C) |

Ningún D-item bloquea el cierre de 0a. Los UNKNOWN se conservan.

## 2. Baseline de tienda

**Fuente:** Shopify Analytics (captura de Michael), recibida 2026-10-05. **Periodo mostrado: 1 ene – 5 oct 2026.** Lanzamiento aproximado de la tienda: marzo 2026 (Michael). Plan: Basic, facturación anual. Las cifras de Shopify vienen redondeadas ("1,4 mil", "1,1 mil").

| Métrica | Valor |
|---|---|
| Sesiones totales | 1.866 |
| Sesiones (excluyendo tráfico propio / no humano) | UNKNOWN (no separable con los datos actuales; ver ubicación) |
| Añadidos al carrito | 56 (3 %) |
| Llegaron a checkout | 29 (1,55 %) |
| Completaron pago **en el embudo de Shopify** | 0 — **anomalía de medición/atribución pendiente (§2.2); no es evidencia de que el checkout falle** |
| Pedidos registrados en Shopify | 3 — los 3 son pruebas de Michael con su propio dinero, hechas como cliente normal; el cobro quedó acreditado en la cuenta de Wompi (confirmado por Michael; verificación con el panel de Wompi: D13, diferido) |
| Pedidos comerciales reales | 0 (confirmado por Michael) |
| Reembolsados | 0 (pedidos de prueba; según Michael el dinero permanece en Wompi) |
| Cancelados | UNKNOWN |
| Tasa de conversión comercial | 0 compras reales / 1.866 sesiones; **no interpretable** hasta separar tráfico propio y no humano |

**Fuente de tráfico (referentes visibles):**

| Referente / ubicación | Sesiones |
|---|---|
| Directo / Council Bluffs | ~1.100 |
| Directo / Barranquilla | 365 |
| Google / Barranquilla | 65 |
| Directo / Bogotá | 19 |
| Google / Bogotá | 18 |
| Instagram (social) | 23 |
| Facebook (social) | 1 |
| Resto no listado | UNKNOWN |

**Dispositivo:**

| Dispositivo | Sesiones |
|---|---|
| Escritorio | ~1,4 mil (≈1.455 *(derivado: 1.866 − 410 − 1)*) |
| Móvil | 410 |
| Otro | 1 |

**Ubicación (aproximada):**

| Ciudad | Sesiones |
|---|---|
| Council Bluffs, Iowa (EE. UU.) | ~1,1 mil |
| Barranquilla | 450 |
| Bogotá | 40 |
| Medellín | 26 |
| Cartagena | 16 |
| Otras ubicaciones | UNKNOWN (≈234 *(derivado: 1.866 − 1.632 listadas con Council Bluffs en 1.100)*) |

**Páginas de aterrizaje visibles:**

| Página | Sesiones |
|---|---|
| Homepage | 1.652 |
| `/products/succionador-honey` | 22 |
| `/collections/dildos` | 20 |
| `/collections/all` | 18 |
| `/collections/vibradores` | 16 |
| `/collections/para-mujeres` | 16 |
| `/collections/para-hombres` | 9 |

Instagram (30 días): alcance UNKNOWN · visitas al perfil UNKNOWN · toques en el enlace UNKNOWN · publicaciones UNKNOWN · **seguidores 59** (Michael).

### 2.1 Catálogo (D6)

**Hechos reportados por ChatGPT sobre un export parcial** (corresponden a 50 productos, no al catálogo completo; ver "Catálogo público vivo" más abajo; **Claude no ha verificado los datos de inventario y costo**): 113 filas de exportación · 50 productos únicos · 50 activos · 50 publicados · precio mínimo 5.000 COP · mediana 50.000 COP · máximo 289.900 COP · `Cost per item` completado en 0 de 50 · seguimiento de inventario de Shopify activo en los 50 · política de inventario `deny` en los 50 · 49 con inventario positivo (cantidades predominantes cercanas a 10.000; algunos 100.000) · 1 con inventario 0.

**Modelo actual, confirmado por Michael:** inventario virtual/sentinel en Shopify respaldado por disponibilidad esperada del proveedor. Las cantidades cercanas a 10.000 (algunas 100.000) se configuraron **deliberadamente** para que los productos no aparezcan agotados. Vibrabien no posee físicamente esas unidades, no mantiene stock propio relevante y compra/obtiene el producto del proveedor después del pedido; el proveedor normalmente dispone de grandes cantidades.

**Disponibilidad en Shopify representada mediante stock virtual alto; no sincronizada con stock físico del proveedor.** Riesgo que permanece: Shopify = disponible mientras el proveedor está temporalmente agotado. Se resuelve en 0b con el diseño del proceso de confirmación de disponibilidad (ver `OPERATIONS.md` §2-§3). No se cambian las cantidades en Shopify.

Pendiente de aclarar: el producto con inventario 0 reportado (hoy los 124 productos publicados figuran como disponibles; el endpoint público no expone cantidades) y si el tema muestra cantidades al público (UNKNOWN).

**Catálogo público vivo (Claude, 2026-10-05, lectura solo lectura del endpoint público `vibrabien.co/products.json`, el mismo que ve cualquier visitante):**
- **124 productos publicados.** Precio mínimo por producto: 5.000 · P10 17.900 · P25 35.000 · **mediana 75.000** · P75 129.900 · P90 219.900 · máximo 480.000 COP.
- Distribución: ≤20.000: 17 · 20.001–50.000: 34 · 50.001–100.000: 31 · 100.001–200.000: 28 · >200.000: 14.
- 124/124 con imágenes y descripción. Los 124 figuran como disponibles (`available`); el endpoint no expone cantidades de inventario.
- Productos por colección: dildos 31 · vibradores 40 · para-mujeres 67 · para-hombres 14.
- Creación (productos vigentes): 78 en abril 2026, 13 en mayo, 1 en julio, 32 en agosto; el más antiguo, 16-abr-2026 (Michael sitúa el lanzamiento ~marzo; productos anteriores pudieron eliminarse).
- **Los 124 productos tienen `updated_at` = 2026-10-05 ~17:51:** actualización masiva el mismo día. Autor y causa: UNKNOWN (pendiente preguntar a Michael si hizo cambios masivos hoy, p. ej., de inventario).
- Duplicados de título confirmados en el catálogo vivo: Bala Vibradora Winyi Brandy Silicona Premium (`…-1` a 179.900 y la otra a 219.900) · Gel Exótico (`gel-exotico-1` a 18.000 y `gel-exotico` a 41.000; además "Gel Exótico Sachet" a 5.000 y "Gel Exótico Erotic Care" a 61.000) · Cuellera sado (`…-1` a 45.000 y otra a 85.000). Siguen en REVIEW (pueden ser presentaciones distintas).

**Explicación de la discrepancia con los hechos reportados (confianza alta por coincidencia exacta):** los 50 primeros productos del catálogo vivo, en el orden del endpoint, tienen mínimo 5.000, mediana 50.000 y máximo 289.900 COP, idénticos a los valores reportados del CSV, y los duplicados de Gel Exótico y Winyi están entre ellos. El CSV inspeccionado fue, casi con seguridad, un **export parcial de 50 productos** y no el catálogo. La cifra "50 productos" no describe el catálogo. **Reconciliado con ChatGPT:** revisó de nuevo su archivo (113 filas, 50 handles únicos), corrige su conclusión ("el archivo recibido contenía 50 productos", no "Vibrabien tiene 50 productos") y acepta la evidencia del endpoint. Estado: **catálogo vivo, 124 productos — CLAUDE VERIFIED; CSV, 50 productos — verificado por ChatGPT.** Causa del export parcial: UNKNOWN y sin importancia ahora. El export de julio visible en `Downloads` (`products_export_1.csv`, 24-jul-2026; 93 productos, `Cost per item` vacío en 93 de 93) es anterior.

**Posibles títulos duplicados (REVIEW — no asumir error; pueden ser presentaciones distintas):**

| Título | Precios | Origen del dato |
|---|---|---|
| Bala Vibradora Winyi Brandy Silicona Premium | 179.900 y 219.900 | Michael / ChatGPT (no está en el export de julio) |
| Gel Exótico | 18.000 y 41.000 | Michael / ChatGPT; el export de julio muestra además "Gel Exótico Sachet" (5.000) y "Gel Exótico Erotic Care" (61.000) con handles distintos |

Medición instalada: **hay al menos dos integraciones/píxeles de medición activos** (Google & YouTube y GTM - Eventos y Compras; ver §2.2). GA4, Search Console y Meta Pixel: no confirmados por las capturas → UNKNOWN. Si falta GA4: registrar `GAP: GA4 missing` y decidir `0a.1`.

### 2.2 Configuración de Shopify (Día 1, segundo bloque)

**Anomalía de medición / atribución (PENDIENTE):** Shopify Analytics muestra "completaron el pago: 0" aunque existen 3 pedidos hechos por el flujo normal de la tienda (sitio → producto/carrito → checkout → Wompi → pago, con el cobro acreditado en Wompi según Michael). **Se registra como anomalía de medición/atribución, no como fallo del checkout.** Causa: UNKNOWN. **Sigue abierta.** Retorno a la página de confirmación/gracias tras pagar en Wompi: UNKNOWN (Michael no lo recuerda). Pendiente: ver si los 3 pedidos tienen fuente/atribución en Shopify. Contexto: existen al menos dos integraciones de medición activas (§2.2, D9).

**D1 — Plan:** Basic · facturación anual · 264 USD/año (captura de Shopify). Costo fijo: queda fuera del margen de contribución y cuenta en el punto de equilibrio.

**D7 — Canales de venta (estado visible actual, captura de Shopify):**

| Canal / app | Estado visible |
|---|---|
| Tienda online | Instalado |
| Google & YouTube | Instalado desde el 4 de mayo · conexión ACTIVA · píxel CONECTADO · datos Optimizado · extensiones activas 0 · funciones activas 0 (detalle abajo) |
| Headless | Instalado — uso UNKNOWN (Michael no sabe si se usa) |
| Point of Sale | Instalado — uso UNKNOWN (Michael no sabe si se usa) |
| Shop | No aparece en esa pantalla |
| Facebook & Instagram | No aparece en esa pantalla |

Solo se registra el estado visible actual; **no se asume que Shop o Facebook & Instagram nunca estuvieron instalados.**

**D7 — Apps instaladas (Shopify → Apps):** Flow · Messaging · Mercado Pago Tarjetas CO · Translate & Adapt. Solo se registra que están **INSTALADAS**. No se asume que Mercado Pago funcione como método de pago, que Messaging sea WhatsApp, que ninguna genere tráfico ni que alguna deba eliminarse. Función exacta: pendiente cuando sea relevante.

**Google & YouTube — caracterización actual (captura del canal):**
- Conexión del canal: ACTIVA · píxel: CONECTADO · medición Web y Servidor · acceso a datos: Optimizado.
- 2 mercados visibles (cuáles: UNKNOWN) · extensiones activas: 0 · funciones activas: 0.
- Permisos/accesos visibles sobre pedidos, productos, informes/estadísticas, clientes y descuentos y otros datos.
- **UNKNOWN:** si Merchant Center tiene catálogo sincronizado; qué productos, si alguno, están publicados en superficies de Google; si existen campañas; si Google Shopping está activo. No se investiga Google Ads.

**D8 — Pagos (captura de Shopify → Pagos):**

| Elemento | Estado |
|---|---|
| Wompi | **ACTIVO** |
| PayPal | INACTIVO |
| Cargo de Shopify por proveedores externos | **2 %** — la pantalla muestra: "Se aplica un cargo de 2% a los pagos procesados a través de proveedores externos." → `shopify_transaction_fee` = 2 % para el flujo actual vía Wompi |
| Comisión propia de Wompi | UNKNOWN (no se suma al 2 % hasta conocer la tarifa real) |

**D8 — Envíos (captura del Perfil general de envío).** *Corrige el registro anterior de "2 zonas": hay **1 zona doméstica (Colombia), con 2 tarifas**.*

| Zona | Tarifa | Condición | Precio al cliente |
|---|---|---|---|
| Domestic — Colombia | Estándar | Pedidos de $0 a $162.599 COP | $14.951 COP |
| Domestic — Colombia | Estándar | Pedidos desde $162.600 COP | GRATIS |

Otros hechos: el perfil general aplica a los productos que no estén en otros perfiles; los productos nuevos se añaden por defecto; 1 de 1 sucursal; **ubicación de procesamiento configurada en Barranquilla, Colombia** (la dirección exacta no se registra) · fechas estimadas de entrega: desactivadas · entrega local: desactivada · retiro en tienda: desactivado · sin cuenta de transportadora conectada. **No se evalúa si las tarifas son correctas: eso pertenece a 0b.**

**D9 — Eventos del cliente / píxeles (Shopify → Eventos del cliente):**

| Integración | Estado | Datos |
|---|---|---|
| Google & YouTube | Servidor + Web | Optimizado |
| GTM - Eventos y Compras | Web | UNKNOWN (qué servicios externos recibe; si hay duplicación) |

**Hay al menos dos integraciones/píxeles de medición activos.** No se asume qué recibe GTM ni si hay duplicación. No se modifica ni desactiva nada.

**D9 — Privacidad del cliente (Shopify → Privacidad del cliente):** política de privacidad publicada · banner de cookies automatizado (Shopify indica que no es obligatorio en las regiones donde la tienda vende actualmente) · página de exclusión del uso compartido de datos automatizada y activa para California, Colorado y otros estados indicados por Shopify · **Shopify Network Intelligence: ACTIVADO** · configuración de marketing por email/SMS presente · configuración de doble suscripción presente · ubicación del almacenamiento mostrada por Shopify: Estados Unidos. **No se determina si cumple o incumple la normativa colombiana** (revisión posterior).

> **REVIEW:** Shopify Network Intelligence está activo y la propia interfaz indica uso combinado de datos de clientes para productos, segmentación de anuncios y personalización. Revisar implicaciones de privacidad para una tienda de bienestar íntimo. No se desactiva en 0a.

**D10 — Políticas (Shopify → Políticas):** reglas de devolución/cancelación predeterminadas: no hay reglas establecidas. Políticas escritas **PUBLICADAS:** devoluciones y reembolsos · privacidad · términos del servicio · envío · información de contacto · aviso legal. **Solo se registra que están publicadas; su contenido no se ha revisado** (no se afirma que sea correcto, suficiente ni adaptado a Vibrabien).

### 2.4 Cuarto bloque del Día 1 (respuestas de Michael y observación de la web pública)

**D13 — Wompi. Estado histórico registrado durante el Día 1: BLOCKED / EXTERNAL ACCESS REQUIRED. Estado vigente: DEFERRED / NON-BLOCKING por DEC-020.** Michael confirma que **no tiene acceso al panel de Wompi**. Lo que sabemos por Michael: los 3 pedidos de prueba fueron pagados, el dinero quedó en Wompi y no fue reembolsado. **UNKNOWN:** transacciones verificadas en panel, montos exactos en Wompi, comisión de Wompi, actividad/categoría declarada, avisos, nombre en el extracto. Se resolverá después mediante la persona que administre Wompi, recuperación de acceso o consulta directa a Wompi. El cruce "3 cobros en Wompi vs. 3 pedidos en Shopify" sigue sin verificar (solo palabra de Michael).

**D11 — Instagram:** seguidores **59**. Instagram muestra **2 "vistas" en el último mes**: *2 vistas reportadas por Instagram en el último mes; tipo exacto de métrica pendiente de confirmar.* No se convierte en alcance, visitas al perfil ni impresiones. Interpretación permitida: la actividad/distribución observada es extremadamente baja. Alcance, visitas al perfil, toques en el enlace, mejor contenido, tipo de cuenta y funciones comerciales: OPEN.
*Meta declarada por Michael:* llegar a 1.000 seguidores para darse a conocer. Se registra como deseo declarado; **no está adoptada como objetivo de negocio** (los seguidores son una métrica intermedia, ver `PROJECT.md` §3 principio 4 y §2) y se discute en Fase 1/2.

**D16 — Fiscal:** **empresa** (Michael). Facturación: UNKNOWN. Tratamiento del IVA: UNKNOWN. Tipo societario: UNKNOWN (no necesario ahora).

**D12 — WhatsApp.** Michael confirma que el número enlazado desde vibrabien.co usa **WhatsApp Business** (cuenta Business: CONFIRMADA; botón web y enlace del pie de página: CONFIRMADOS). **Observación directa de la página de inicio de vibrabien.co (Claude, solo lectura, sin hacer clic en los enlaces; 2026-10-05):**

| Elemento | Observado |
|---|---|
| Botón flotante "Contáctanos por WhatsApp" | Presente en la página de inicio (posición fija). Enlace `wa.me/` hacia un número colombiano (+57…), con mensaje predefinido: "Hola quiero información sobre sus productos". |
| Enlace de texto "WhatsApp: +57 …" | Presente (pie de página). Mismo número. |
| Otras páginas | No revisadas |
| Número | Visible públicamente; no se registra completo en este documento |

UNKNOWN: si hay catálogo de WhatsApp, si hay enlace o botón de WhatsApp en Instagram, cuántas conversaciones se han originado desde la web, y si una app de Shopify inyecta el botón o está en el tema. En la lista de apps de Shopify no aparece ninguna app de WhatsApp evidente (Messaging no se asume que lo sea).
**Conflicto con DEC-005:** la web actualmente dirige consultas comerciales a una cuenta WhatsApp Business confirmada, mientras que DEC-005 retira WhatsApp Business como canal comercial por prudencia. En 0a **no se elimina ni se modifica nada** (solo lectura); queda para decisión de Michael. Pendiente: cuántas conversaciones de WhatsApp ha recibido originadas en el sitio (señal de demanda que Shopify Analytics no mide).

**D9 — Etiquetas observadas en la página pública** (código fuente de la home, solo lectura): GTM `GTM-MTX3DCGF` · etiqueta Google `G-DWSS4HHK0V` (formato típico de un ID de medición de GA4) · etiqueta Google Ads `AW-18142264463` · etiqueta Google `GT-WF83CWBD`. Enlaces en la web a la cuenta de Instagram `@vibrabien_col` y a una página de Facebook. **GA4 permanece UNKNOWN según la regla vigente:** estas etiquetas son evidencia técnica parcial; la confirmación requiere ver la propiedad en GA4 o en la configuración de Shopify/Google. La presencia de una etiqueta de Google Ads **no establece** que existan campañas (UNKNOWN; no se investiga Google Ads).

**Observación incidental (no es auditoría):** el título de la página de inicio es "Sex Shop Online y Juguetes Íntimos en Colombia | VibraBien".

### 2.3 Mapa de exposición actual (parcial)

Lo que ya existe y podría chocar con una política. **Solo registro de hechos; no se investiga ni se modifica nada en 0a.**

| Elemento | Estado | Pendiente |
|---|---|---|
| **WhatsApp** | **Cuenta WhatsApp Business confirmada**, enlazada desde la web: botón flotante con mensaje predefinido y enlace de texto con número (§2.4). Catálogo, enlace en Instagram y conversaciones desde la web: UNKNOWN | Conflicto con DEC-005 → decisión de Michael; no se elimina en 0a |
| **Etiquetas Google en la web** | GTM, etiqueta G- (formato GA4), etiqueta AW- (Google Ads) y GT- observadas en el código público | GA4 UNKNOWN; campañas UNKNOWN |
| Enlaces sociales en la web | Instagram `@vibrabien_col` y una página de Facebook | Estado de la página de Facebook: UNKNOWN |
| **Google & YouTube** | Instalado desde el 4 de mayo; conexión ACTIVA; píxel CONECTADO; medición Web/Servidor; datos Optimizado; 2 mercados; 0 extensiones y 0 funciones activas; permisos visibles sobre pedidos, productos, informes, clientes y descuentos | Merchant Center / catálogo sincronizado / productos en superficies de Google / campañas / Google Shopping: UNKNOWN. No auditoría completa de Google Ads. **Captura de solo lectura de alta prioridad pendiente** (Merchant Center conectado, productos sincronizados, approved/disapproved/pending, configuración `adult`, mercados): ver `OPERATIONS.md` §8. |
| Medición (Eventos del cliente) | Google & YouTube (Servidor + Web) y GTM - Eventos y Compras (Web) activos | Qué recibe GTM y si hay duplicación |
| **Shopify Network Intelligence** | ACTIVADO; la interfaz indica uso combinado de datos de clientes (productos, segmentación de anuncios, personalización) | REVIEW de privacidad para bienestar íntimo; no se desactiva en 0a |
| Apps instaladas (Flow, Messaging, Mercado Pago Tarjetas CO, Translate & Adapt) | Instaladas; función exacta UNKNOWN | Aclarar cuando sea relevante |
| Facebook & Instagram (canal de Shopify) | No visible en la captura | Confirmar estado actual |
| Shop | No visible en la captura | Confirmar estado actual |
| Headless, Point of Sale | Instalados; función UNKNOWN | Aclarar si se usan |
| Pasarela | Wompi activo (categoría no confirmada); PayPal inactivo | Investigación/consulta diferida por DEC-020 (no se envía) |

## 3. Economía unitaria (preliminar en 0a; se valida en 0b)

**Sin umbral universal de PASS/FAIL.** Se calcula y se reporta; el objetivo de CAC se define después.

**PRELIMINAR:** el tratamiento fiscal puede modificar estos cálculos. No se asume IVA ni tasa fiscal; no se resuelve contabilidad en 0a.

Componentes:

```
sale_price
supplier_cost
payment_processing_fee       = comisión Wompi + IVA de la comisión (si aplica)
shopify_transaction_fee      = 2 % (flujo actual vía Wompi, según Shopify)
packaging_cost
shipping_cost
shipping_charged_to_customer
shipping_subsidy             = max(shipping_cost − shipping_charged_to_customer, 0)
expected_variable_returns
tax_treatment                = UNKNOWN / consultar contador
```

Fórmulas:

```
CONTRIBUTION_MARGIN_COP     = sale_price − supplier_cost − payment_processing_fee
                              − shopify_transaction_fee − packaging_cost
                              − shipping_subsidy − expected_variable_returns
CONTRIBUTION_MARGIN_PERCENT = CONTRIBUTION_MARGIN_COP / sale_price
BREAK_EVEN_CAC              = CONTRIBUTION_MARGIN_COP
TARGET_CAC                  = (a definir) por debajo del break-even para dejar utilidad
```

Estado de los componentes: comisión de Wompi UNKNOWN · IVA de la comisión UNKNOWN (solo si aplica) · `shopify_transaction_fee` = 2 % para el flujo actual vía Wompi (pantalla de Pagos de Shopify, plan Basic); **no se suma a la comisión de Wompi hasta conocer la tarifa real de Wompi** · `tax_treatment` UNKNOWN, incluido si `sale_price` ya incluye impuestos. Costos fijos (suscripción Shopify, apps) quedan fuera del margen de contribución pero cuentan en el punto de equilibrio.

`shipping_charged_to_customer` (configuración actual en Shopify, no evaluada): $14.951 COP para pedidos de $0 a $162.599 COP; gratis desde $162.600 COP. `shipping_cost` real: UNKNOWN (0b).

**Muestra D14 FIJADA el 2026-10-05, antes de recibir costos del proveedor** (no son "producto estrella"; todos existen en el catálogo público vivo). Regla: anclas por percentil del catálogo (P10 17.900 · P25 35.000 · P50 75.000 · P75 129.900 · P90 219.900); medio = más cercano a la mediana dentro de las colecciones dildos y vibradores; medio/alto = más cercano a P75; alto = más cercano a P90; masculino = más cercano a la mediana de la colección para-hombres (48.000); empates: primero en el orden del catálogo. **Excepción deliberada:** el producto de ticket bajo es Gel Exótico (18.000, ≈P10; resuelve el REVIEW de duplicados), no "Esposas peluche" (17.900), que sería el más cercano por regla pura. **Muestra aceptada por ambas IAs y congelada: no se cambia tras recibir costos.** Al pedir costos al proveedor se usan siempre el handle exacto y el precio exacto (importa en los duplicados). Antes del simulacro, `shipping_subsidy`, `packaging` y `expected_variable_returns` son **estimaciones** y se reportan en tres escenarios.

| Producto (ticket) | sale_price | supplier_cost | payment_processing_fee | shopify_transaction_fee | packaging_cost | shipping_cost (bajo / medio / alto) | shipping_charged_to_customer | shipping_subsidy | expected_variable_returns | Margen COP (3 esc.) | Margen % (3 esc.) |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1. Bajo — Gel Exótico (`gel-exotico-1`) | 18.000 | 8.700 (`CATALOG_COST_2024`, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 14.951 (pedido de 1 unidad) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| 2. Medio — Dildo Doble Twin Fork Purple (`dildo-doble-twin-fork-purple`) | 79.900 | 39.900 (`CATALOG_COST_2025`, match PROBABLE, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 14.951 (1 unidad) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| 3. Medio/alto — Masajeador ava (`masajeador-ava`) | 129.900 | 69.900 (`CATALOG_COST_2025`, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 14.951 (1 unidad) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| 4. Alto — Bala Vibradora Winyi Brandy Silicona Premium (`bala-vibradora-winyi-brandy-silicona-premium`, versión de 219.900) | 219.900 | 112.900 (`CATALOG_COST_2025`, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 0 (gratis, ≥162.600) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| 5. Masculino (opcional) — Super huevo masturbador (`huevo-masturbador-super`) | 48.000 | 24.900 (`CATALOG_COST_2025`, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 14.951 (1 unidad) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |
| Extra informativo (no cuenta como muestra): Succionador Honey (`succionador-honey`), el único producto con aterrizajes propios en Shopify Analytics (22) | 240.000 | 129.900 (`CATALOG_COST_2025`, §3.1) | UNKNOWN | 2 % | UNKNOWN | UNKNOWN | 0 (gratis, ≥162.600) | UNKNOWN | UNKNOWN | UNKNOWN | UNKNOWN |

### 3.1 D14 — costos de catálogo y margen pre-fulfillment EX-WOMPI (Día 2)

**Etiquetas de costo (ninguna es `CURRENT_SUPPLIER_COST_CONFIRMED`):**
- `CATALOG_COST_2025`: Winyi (portada "CATÁLOGO 2025"; PDF creado el 5-may-2025; el título interno del archivo dice "catalogo winyi 2023") y Fara Toys ("CATALOGO FARATOYS 2025"; PDF creado el 26-may-2025).
- `CATALOG_COST_2024`: **Erotic** ("CATÁLOGO DE PRODUCTOS V°1-2024"; 80 páginas; PDF creado el 7-jun-2024). **Procedencia (verificada el 2026-10-06):** el primer catálogo que se adjuntó a Claude fue `Precios-MAYORISTAS-Catálogo-Erotic_2024 (1) (1).pdf` (SHA-256 `2FC8AF82…618CC`; idéntico, por hash, a una copia anterior `…(1).pdf` de la misma carpeta). El brief de Michael/ChatGPT nombraba en cambio "CATALOGO MUY SECRETO 2025_MAYOR", que es **otro archivo**. La afirmación anterior de este documento ("Michael lo nombró MUY SECRETO…, pero es de 2024") era una **inferencia no comprobada y errónea**: Claude asumió que ambos nombres eran el mismo archivo.
- **"MUY SECRETO 2025_MAYOR"** (`CATALOGO MUY SECRETO 2025_MAYOR (1).pdf`, 42 páginas, creado el 16-abr-2025, autor "Sexosentido Cartagena"; portada "CATÁLOGO ABRIL 2025, EDICIÓN N.º 03, MAYORISTAS / EMPRENDEDORES"): lencería (páginas 2-29), disfraces (30-38) y una página índice de juguetes sin precios (39-40). Claude lo abrió por primera vez el 2026-10-06: **no contiene Gel Exótico ni ninguno de los productos de la muestra**. Esa etiqueta no se usa para ningún costo de este documento.
- **ChatGPT y Claude analizaron conjuntos de archivos distintos para el primer catálogo.** ChatGPT no recibió el archivo Erotic y por eso no pudo encontrar Gel Exótico en sus tres PDFs.
- Ningún catálogo indica IVA, mínimos de compra, vigencia, despacho ni garantía.
- "Pág." es la página del PDF (en Erotic, el número impreso difiere).

**Fórmula (NO es margen de contribución final ni utilidad neta):**
`PRE_FULFILLMENT_MARGIN_EX_WOMPI = sale_price − catalog_cost − shopify_transaction_fee`, con `shopify_transaction_fee` = 2 % de `sale_price`. `PRE_FULFILLMENT_MARGIN_EX_WOMPI_PERCENT` = margen / `sale_price`.
**UNKNOWN (no se asumen en cero):** comisión de Wompi, empaque, envío real, devoluciones, impuestos.

| # | Producto de Vibrabien | Catálogo · pág. | Nombre del proveedor | Código · ref · SKU | Costo catálogo | Sugerido detal | `sale_price` | Match | Fee Shopify 2 % | `PRE_FULFILLMENT_MARGIN_EX_WOMPI` | % |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | Gel Exótico (`gel-exotico-1`) | Erotic · 11 | Gel Exótico, lubricante a base de agua, 37 ml | REF.1522 | 8.700 (2024) | 18.000 | 18.000 | **EXACT MATCH** (nombre, marca Erotic Care, presentación 37 ml, foto de la caja idéntica, sugerido). **`CLAUDE VERIFIED`: fuente = archivo Erotic V°1-2024 adjunto a Claude; ChatGPT no recibió ese archivo y no pudo verificarlo.** | 360 | **8.940** | **49,7 %** |
| 2 | Dildo Doble Twin Fork Purple (`dildo-doble-twin-fork-purple`) | Fara · 37 | BIG DOUBLE | Cod 10376 · Ref CN-711916421 | 39.900 (2025) | 79.900 | 79.900 | **SAME PRODUCT / HIGH CONFIDENCE** (reevaluado el 2026-10-06; antes PROBABLE): PVC natural, púrpura, 20 cm Ø3,6, doble cabeza con ventosa, sugerido exacto; ChatGPT reporta una ficha pública de Mercado Libre con marca Chisa-novelties y modelo CN-711916421 (el mismo ref. del catálogo), y la foto de la tienda muestra un empaque Hi-Rubber/CHISA. El nombre "Twin Fork" no está en el catálogo y el cliente podría recibir el empaque de Fara ("Big Double"), distinto al de la foto. **No se usa EXACT: falta una prueba inequívoca.** | 1.598 | **38.402** | **48,1 %** |
| 3 | Masajeador ava (`masajeador-ava`) | Fara · 22 | MASAJEADOR AVA | Cod 11105 · Ref SHD-S082 | 69.900 (2025) | 129.900 | 129.900 | **EXACT MATCH** (foto de la tienda idéntica: "AVA massager" con caja FARA; sugerido exacto). **Winyi también tiene un "Masajeador Ava" distinto (WY0551, 264.900): no es este.** | 2.598 | **57.402** | **44,2 %** |
| 4 | Bala Vibradora Winyi Brandy Silicona Premium, versión 219.900 (`bala-vibradora-winyi-brandy-silicona-premium`) | Winyi · 9 | SMART BULLET BRANDY | WY0713 · SKU 13353 | 112.900 (2025) | 219.900 | 219.900 | **EXACT MATCH** (nombre, marca, foto idéntica, sugerido) | 4.398 | **102.602** | **46,7 %** |
| 5 | Super huevo masturbador (`huevo-masturbador-super`) | Winyi · 27 | HUEVO MASTURBADOR SUPER | WY0632 · SKU 13047 | 24.900 (2025) | 48.000 | 48.000 | **EXACT MATCH** (foto idéntica con caja Winyi "Super Masturbator Egg", sugerido exacto) | 960 | **22.140** | **46,1 %** |
| Extra | Succionador Honey (`succionador-honey`) | Winyi · 13 y 41 | HONEY (13: versión purple) | WY0528PURPLE / WY0528 · SKU 11805 | 129.900 (2025) | 239.900 | 240.000 | **EXACT MATCH** (nombre, marca, foto idéntica; la tienda redondea +100 sobre el sugerido) | 4.800 | **105.300** | **43,9 %** |

**Estado de verificación de la tabla (reconciliado con ChatGPT):**
- `DOUBLE VERIFIED` (costo y sugerido, de forma independiente): Twin Fork (39.900 → 79.900), Ava de Fara (69.900 → 129.900), Brandy de Winyi (112.900 → 219.900), Super huevo (24.900 → 48.000), Honey (129.900 → 239.900) y Crystal WY0714 (89.900 → 179.900). Los cálculos de `PRE_FULFILLMENT_MARGIN_EX_WOMPI` de esas filas fueron revisados por ChatGPT y son correctos. En el Twin Fork, los números son doble verificados; la **identidad** del producto se reevaluó a `SAME PRODUCT / HIGH CONFIDENCE` el 2026-10-06 (ver la tabla de arriba); no se eleva a EXACT.
- `CLAUDE VERIFIED` solamente: **Gel Exótico 37 ml** (costo 8.700, sugerido 18.000, REF.1522). Procedencia de la fuente: resuelta (archivo Erotic V°1-2024 adjunto a Claude), pero ChatGPT no tuvo ese archivo. Para doble verificación, Michael tendría que entregárselo. Mientras tanto, el margen de la fila 1 (8.940; 49,7 %) no se presenta como doble verificado.

**Otro caso derivado de los catálogos:** el listado duplicado "Bala Vibradora Winyi Brandy…" a 179.900 (`…-1`) **no es Brandy**: su foto y su precio corresponden a **CRYSTAL de Winyi** (p. 10, WY0714, SKU 13354, costo 89.900, sugerido 179.900). Con los mismos criterios: 179.900 − 89.900 − 3.598 = 86.402 (48,0 %). No se modifica nada en Shopify.

**Posibles errores de contenido detectados (REVIEW, sin modificar nada):**
- *Gel Exótico:* la ficha de Vibrabien promete "aroma seductor" y "esencia exótica", pero el catálogo Erotic lo describe como "transparente, inodoro", "no contiene sabor" y "sensación neutra". Es un posible claim sin respaldo; confirmar con el proveedor.
- *Twin Fork Purple:* la foto de la tienda muestra un empaque de otra marca (Hi-Rubber/CHISA); el catálogo lo lista como "BIG DOUBLE". El cliente podría recibir un empaque distinto.
- *Duplicados de título:* "Bala Winyi Brandy" (la de 179.900 es Crystal), "Gel Exótico" (cuatro presentaciones del mismo producto), "Cuellera sado" (45.000 y 85.000, dos artículos distintos en Fara p. 50 y 51).
- *Nombres de handle distintos del título:* `anillo-vibrador-doble-con-control-remoto-bunny` se titula "…Andy…"; `succionador-dual-bloom` se titula "…Quinn…"; `plug-anal-vibrador-doble-bulbo-con-control-remoto` se titula "…Henry…".
- *Mismo nombre, productos distintos en dos marcas:* "Ava" (Fara y Winyi) y "Crystal" (Fara p. 4, 80.000, es el "Vibrador crystal" de la tienda; Winyi p. 10, 179.900).
- *Precio por debajo del sugerido:* "Plug Anal Doble Bulbo Winyi Henry" se vende a 190.900 y el sugerido de Winyi (WY0684) es 209.900 (costo de catálogo 106.900).

**Lectura:** los costos de catálogo equivalen a ~49–59 % del sugerido y la tienda cobra exactamente el sugerido, de modo que el margen pre-fulfillment ex-Wompi de los productos verificados es 44–50 % del precio. **Esto no es utilidad:** quedan por restar Wompi, empaque, envío real, devoluciones e impuestos, todos UNKNOWN. En el producto de 18.000, el cliente paga 14.951 de envío y el costo real de envío es UNKNOWN.

**Requiere confirmación del proveedor:** vigencia de los precios 2024/2025 frente a hoy; si incluyen IVA; mínimos y descuentos; ref. y empaque real de "BIG DOUBLE"; presentación y disponibilidad del Gel Exótico de 37 ml (REF.1522) y si existe la de 20 ml ($15.000), que la tienda no vende; si el Brandy de 179.900 es en realidad Crystal; colores disponibles de Honey.

### 3.2 Cruce del catálogo de Vibrabien con los tres catálogos (HEURÍSTICO / EXPLORATORIO)

Cruce automático de los 124 productos publicados (nombre distintivo + precio exacto en la misma zona del catálogo, más lectura estructurada de Winyi). **No está verificado producto por producto salvo la muestra.**
**Contabilidad de los 124 (suma exacta):** 91 + 7 + 2 + 24 = 124. Antes se habían escrito cifras aproximadas ("~91 + 7 + ~25 = ~123") que omitían 2 casos y redondeaban el último grupo; no había un producto perdido.
- **91** coinciden por nombre distintivo y precio exacto en la misma zona de un catálogo de Fara o Erotic (cruce automático; puede haber falsos positivos). Los conteos por catálogo en el cálculo (Fara 100, Erotic 23) cuentan páginas con coincidencia y se solapan, no productos.
- **7** coinciden con Winyi en la lectura estructurada: Brandy 219.900, Marcia, Andy, Quinn y Super con precio exacto; Honey y Joanna con +100 de redondeo.
- **2** son casos Winyi con hallazgo propio: Henry (nombre coincide, pero se vende a 190.900 y el sugerido es 209.900) y la "Bala Brandy" de 179.900 (que corresponde a Crystal).
- **24** no cruzaron automáticamente: jaula de castidad, set de duchas anales, bolas anales con anillo, masajeador corporal multifunción, vibrador neón Fara multicolor, Twin Fork, huevo vibrador Chrome Silver, vibrador Banana, Gel Exótico (18.000, 41.000 y 61.000), Hot Gel, Ice Gel Silver (fresa y herbarium), Ice Gel frío-caliente, Erotic Ice Gel, Hogtie, Vagina Deep Pleasure, anillo masajeador protástico, funda premium, Estimulante Rosa, Lovense Lush, Vibrador Meave y Wistone Tongue (480.000). De estos, **4 se resolvieron luego a mano** (los tres Gel Exótico por la ficha de Erotic, y el Twin Fork por especificación); **20 siguen sin resolver**. Que no hayan cruzado no demuestra que no estén en un catálogo: varios tienen el nombre solo en la imagen.
- Ningún producto cruzó con más de un catálogo.
- **Esto no es inventario reconciliado:** es una exploración sin verificación producto por producto, salvo la muestra.
- Relación costo/sugerido (mediana, cálculo aproximado): Winyi 0,59 · Fara 0,50 · Erotic 0,46.

### 3.3 D15 — Benchmark de precios frente a vendedores en Colombia (2026-10-06)

**Qué es y qué no es:** una fotografía descriptiva. No decide precios, descuentos ni margen objetivo, no copia a nadie y no declara productos estrella. No se contactó a ningún competidor ni se copió copy o fotos.

**Método y límites (importantes):**
- Fuentes con precio público y consultable: `sexosentido.co` (catálogo público por `products.json`, 1.344 productos, actualizado el 2026-10-06), Addi Marketplace (tienda "Vibra Lab") y, solo como contexto de categoría, Éxito y Farmatodo.
- **Mercado Libre no fue utilizable para consultar precios en la sesión de Claude porque solicitó inicio de sesión** (no se eludió ni se usaron cuentas). ChatGPT sí pudo ver una ficha pública sin iniciar sesión: es una diferencia de acceso y de herramienta, no una afirmación general sobre el marketplace. Con el buscador de Claude no aparecieron otros revendedores con estos SKU (TiendaCereza, Alcarrito y Venuscali no los traen). Falabella y Rappi no se exploraron de forma sistemática.
- **Reconciliación con ChatGPT (2026-10-06):** ChatGPT encontró vendedores adicionales (Lollipop Medellín, Nudite, Paradisex, Erotismo.co) y una ficha pública de Mercado Libre. Esos datos están marcados *(ChatGPT)* = **reportados por ChatGPT, no verificados por Claude**; las URL se incorporarán desde su reporte.
- **Estado de la evidencia:** Super Huevo tiene n = 3 precios; Gel Exótico 37 ml tiene n = 5 (2 con SKU exacto y 3 como mismo producto con alta confianza); el resto tiene comparación limitada (n = 0 o 1). No se exigen 3 vendedores exactos por producto para seguir.
- **Dato clave:** SexoSentido.co **vende al público los mismos SKU**, con el mismo código del catálogo. **Hecho confirmado por Michael (2026-10-06): SexoSentido / SexoSentido Mayoristas es el proveedor de Vibrabien, y el proveedor también vende al consumidor final a través de `sexosentido.co`.** No se infiere: razón social exacta, relación jurídica entre los dominios, exclusividad, prioridad de inventario, condiciones para revendedores ni política de precios (todo UNKNOWN). Los precios de SexoSentido se leen, por tanto, como el canal minorista del propio proveedor (ver riesgo `SUPPLIER-RETAIL CHANNEL CONFLICT` en §4).
- "Precio normal" = precio actual publicado. SexoSentido muestra además un **precio tachado** (por ejemplo, 262.800 frente a 212.900) que se registra como ancla de referencia, no como precio de mercado: no se sabe si es temporal. En varios productos el tachado equivale a precio ÷ 0,7, lo que sugiere un ancla automática.
- Banda descriptiva (no regla): ±5 % = `NEAR MARKET MEDIAN`; por debajo de −5 % = `BELOW`; por encima de +5 % = `ABOVE`.
- Envío: no capturado en SexoSentido (`UNKNOWN`). Addi muestra "entregas de 1 a 3 días hábiles", sin costo visible. Vibrabien cobra 14.951 hasta 162.599 y es gratis desde 162.600.

**Observaciones por producto (competidores):**

| Producto de la muestra | Tienda | Tipo de match | SKU / ref | Precio actual | Precio tachado | Disponibilidad |
|---|---|---|---|---|---|---|
| Gel Exótico 37 ml | SexoSentido | EXACT SAME SKU | 1522 | 19.900 | — | disponible |
| Gel Exótico 37 ml | Lollipop Medellín *(ChatGPT)* | EXACT SAME SKU (SKU 1522 visible) | 1522 | 19.000 | — | UNKNOWN |
| Gel Exótico 37 ml | Nudite *(ChatGPT)* | SAME PRODUCT / HIGH CONFIDENCE (nombre y presentación 37 ml; sin SKU visible en la evidencia) | — | 17.000 | — | UNKNOWN |
| Gel Exótico 37 ml | Paradisex *(ChatGPT)* | SAME PRODUCT / HIGH CONFIDENCE (ídem) | — | 20.000 | — | UNKNOWN |
| Gel Exótico 37 ml | Erotismo.co *(ChatGPT)* | SAME PRODUCT / HIGH CONFIDENCE (ídem) | — | 25.000 | — | UNKNOWN |
| Twin Fork (BIG DOUBLE) | SexoSentido | SAME PRODUCT / HIGH CONFIDENCE (SKU 10376 = Fara "BIG DOUBLE", ref. CN-711916421) | 10376 | 79.900 | — | disponible |
| Twin Fork (CN-711916421) | Mercado Libre Colombia, ficha pública vista por ChatGPT *(ChatGPT)* | Refuerza la identidad: marca Chisa-novelties, modelo CN-711916421, doble, PVC, ventosa, ~19,5 cm | CN-711916421 | **no disponible; sin precio utilizable: no entra al benchmark** | — | no disponible |
| Masajeador Ava (Fara) | SexoSentido | EXACT SAME SKU | 11105 | 128.900 | 178.800 | disponible |
| Winyi Brandy WY0713 | SexoSentido | EXACT SAME SKU | 13353 | 212.900 | 262.800 | disponible |
| Super Huevo Winyi WY0632 | SexoSentido | EXACT SAME SKU | 13047 | 48.900 | 98.800 | disponible |
| Super Huevo Winyi WY0632 | Lollipop Medellín *(ChatGPT)* | EXACT SAME MODEL / SKU (modelo WY0632 explícito en la ficha) | WY0632 | 49.800 | — | UNKNOWN |
| Super Huevo Winyi | Addi · Vibra Lab | SAME PRODUCT / HIGH CONFIDENCE (nombre, marca e imagen idénticos; sin SKU visible) | — | 59.900 | — | en stock |
| Honey WY0528 (SKU 11805) | SexoSentido | **NOT COMPARABLE**: su "Vibrador Honey 10 Funciones" (SKU 11655, 198.730) es otro SKU. No se encontró el SKU 11805 en ningún vendedor | — | — | — | — |
| Extra: Winyi Crystal WY0714 (el listado de Vibrabien "Brandy" a 179.900) | SexoSentido | EXACT SAME SKU | 13354 | 162.900 | 224.800 | disponible |

Otras presentaciones del Gel Exótico en SexoSentido (mismo producto, otros tamaños): sachet 5 ml 5.900 (SKU 8865) · 20 ml 17.900 (1216) · 250 ml 44.900 (9082) · 500 ml 54.900 (8774).
URLs: `https://www.sexosentido.co/products/` + handle (por ejemplo `lubricante-neutro-intimo-gel-exotico-37-ml-sexo-sentido-tienda-erotica`, `vibrador-fara-toys-premium-ava-massager-sexo-sentido-tienda-erotica`, `winyi-brandy-bala-vibradora`, `winyi-super-huevo-masturbador-wy0632-sexo-sentido-tienda-erotica`, `dildo-realista-big-doble-sexo-sentido-tienda-erotica`, `winyi-crystal-punto-g`) y `https://marketplace.addi.com/producto/394498`.

**Posición de Vibrabien (descriptiva; n entre 0 y 5; no es una regla de precios):**

| Producto | n | Mín. | Mediana | Máx. | Vibrabien | Dif. vs mediana | % | Banda |
|---|---|---|---|---|---|---|---|---|
| Gel Exótico 37 ml | 5 (2 EXACT SAME SKU + 3 SAME PRODUCT / HIGH) | 17.000 | 19.900 | 25.000 | 18.000 | −1.900 | −9,5 % | BELOW. Solo con SKU exacto (n=2: 19.000 y 19.900): mediana 19.450, −1.450 (−7,5 %), también BELOW. Vibrabien queda por debajo del centro; solo Nudite (17.000) está por debajo |
| Twin Fork | 1 (SexoSentido; la ficha de Mercado Libre no tiene precio utilizable) | 79.900 | 79.900 | 79.900 | 79.900 | 0 | 0 % | NEAR (n=1) |
| Ava | 1 | 128.900 | 128.900 | 128.900 | 129.900 | +1.000 | +0,8 % | NEAR (n=1) |
| Brandy WY0713 | 1 | 212.900 | 212.900 | 212.900 | 219.900 | +7.000 | +3,3 % | NEAR (n=1) |
| Super Huevo | 3 (SexoSentido 48.900, Lollipop 49.800, Vibra Lab 59.900) | 48.900 | 49.800 | 59.900 | 48.000 | −1.800 | −3,6 % | **NEAR MARKET MEDIAN** (antes figuraba BELOW con n=2). SexoSentido es el canal minorista del propio proveedor (confirmado por Michael), así que solo 2 de los 3 vendedores son ajenos a él; **sin SexoSentido (n=2)**: mediana 54.850, −6.850 (−12,5 %), BELOW. Contra el mínimo observado: −900 (−1,8 %) |
| Honey | 0 | — | — | — | 240.000 | — | — | sin comparación |
| Extra: Crystal (listado "Brandy" 179.900) | 1 | 162.900 | 162.900 | 162.900 | 179.900 | +17.000 | +10,4 % | ABOVE (n=1) |

Gel Exótico, otras presentaciones (n=1, SexoSentido): 250 ml 41.000 frente a 44.900 (−8,7 %) · 500 ml 61.000 frente a 54.900 (**+11,1 %**) · sachet 5.000 frente a 5.900 (−15,3 %).

**Contexto de categoría (COMPARABLE BUT NOT SAME: otra marca y fórmula; no entra en las estadísticas):** gel lubricante Elixir. Sachet de 5 ml en Éxito: 4.897 (antes 5.900). Elixir de 500 ml en Farmatodo: 50.915 (antes 59.900). Elixir "Cum piel sensible" de 250 ml: 49.900, agotado, vendido por Pleasure. Uno de esos listados de farmacia muestra un registro INVIMA (por ejemplo "2024DM-0029636"). **REVIEW REGULATORIO:** que otros vendedores muestren registros no demuestra por sí solo qué requisito exacto aplica a cada producto de Vibrabien; el estado sanitario de sus lubricantes es `UNKNOWN`, no es asesoría legal y **no se resuelve dentro de D15**.

**Patrones observados (n pequeño; no concluyentes):**
1. **El proveedor compite al por menor con los mismos SKU.** Sobre 12 SKU revisados, frente al sugerido del catálogo: Ava, Fancy, Super Huevo y Big Doble caen dentro de ±3 %; Brandy −3,2 %; Gel 500 ml −10,0 %, Crystal −9,4 % y Stargaze −14,6 %; y los geles pequeños quedan por encima (+9,5 % a +19 %, de poco valor absoluto). Muchos llevan precios tachados altos. Vibrabien cobra casi exactamente el sugerido, así que en los productos de ticket alto queda en la misma banda que el proveedor.
2. **Entre los vendedores que parecen independientes del proveedor, los precios se dispersan alrededor del sugerido y no lo copian de forma uniforme.** Gel 37 ml frente al sugerido de 18.000: Nudite 17.000 (−5,6 %), Lollipop 19.000 (+5,6 %), Paradisex 20.000 (+11,1 %), Erotismo.co 25.000 (+38,9 %) *(ChatGPT)*. Super Huevo frente a 48.000: Lollipop 49.800 (+3,8 %) *(ChatGPT)* y Vibra Lab 59.900 (+24,8 %). El sugerido queda cerca del centro o algo por debajo de lo observado; no hay evidencia de un precio único de mercado. (Corrige una afirmación anterior de este documento: sí aparecieron revendedores ajenos a SexoSentido para el Gel Exótico.)
3. **Por debajo del sugerido hay precedentes en el propio proveedor:** Brandy −3,2 %, Crystal −9,4 %, Stargaze −14,6 %, Gel 500 ml −10,0 %. No es "permanente": solo se observó una fecha.
4. **El envío cambia materialmente los productos baratos.** El Gel de 37 ml (18.000) más 14.951 de envío son 32.951, el 83 % más que el producto; el envío del competidor no se capturó. Con la tarifa cobrada como sustituto ilustrativo del costo real (que es `UNKNOWN`), el envío equivaldría al 167 % del margen EX-WOMPI del gel (8.940) y al 15 % del de la Brandy (102.602). Es una hipótesis para 0b, no un dato.
5. **En un solo pedido, los productos baratos tienen mala economía:** el margen EX-WOMPI del gel (8.940) es el que primero absorben Wompi, empaque, envío y devoluciones. Los caros (≥162.600 con envío gratis) tienen margen para absorber más, aunque no se mide.
6. **Donde competir por precio parece más difícil:** (a) lubricantes y geles, de bajo ticket y con competidores de farmacia y supermercado que publican ofertas (Éxito, Farmatodo); (b) cualquier SKU de marca que también venda el propio proveedor en su tienda, con tachados que hacen parecer un descuento cualquier precio cercano.

**Comparación limitada o no comparable:** Honey (sin vendedor del SKU: NOT COMPARABLE); Twin Fork, Ava, Brandy y Crystal (un solo precio, de SexoSentido). Los precios de Mercado Libre no se usaron en la sesión de Claude y la ficha vista por ChatGPT no tiene precio utilizable. Para 0a no se necesitan 3 vendedores exactos por producto.

**Conclusión permitida (no recomienda cambios de precio, no declara productos estrella):**
- Vibrabien está cerca del rango observable en varios SKU.
- No hay evidencia de una ventaja o desventaja general de precio.
- Competir exclusivamente por precio es riesgoso.
- El proveedor también vende al detal los mismos SKU (confirmado por Michael); la relación jurídica y las condiciones para revendedores siguen UNKNOWN.
- La logística y el CAC probablemente importarán más que pequeños movimientos de precio (hipótesis, no medida).
- Los precios tachados de SexoSentido son anclas de referencia: no se tratan como precio normal de mercado ni se afirma que se cobraran antes.

## 4. Riesgos financieros (registro)

> Por decisión de Michael (DEC-020), los riesgos de Wompi siguen registrados pero **no forman parte del camino crítico actual**.

| Riesgo | Detalle | Estado |
|---|---|---|
| Retención de ingresos por Wompi | Reglamento V4-2026, cláusula 6.7: retención hasta 180 días calendario por alertas de fraude o contracargos; también ante solicitud de reversión, índice de fraude superior a 2,5 % (o el que defina Wompi) o actividades restringidas/ilícitas | VERIFICADO por Claude (nivel A, 2026-10-05) |
| Fondo de reserva | Cláusula 6.8: hasta 15 % de los ingresos, a discreción de Wompi, para actividad de alto riesgo de fraude o transaccionalidad mensual superior a USD 50.000; desembolso hasta 90 días después. Si Wompi clasificaría a Vibrabien como "alto riesgo": UNKNOWN | VERIFICADO por Claude (nivel A); aplicación a Vibrabien UNKNOWN |
| Suspensión o cancelación discrecional por Wompi | Cláusulas 15, 14.4 y 2.2.14: pueden cancelar, desactivar o suspender "en cualquier momento, a nuestra discreción"; suspensión inmediata sin notificación previa si detectan actividades ilícitas o restringidas | VERIFICADO por Claude (nivel A) |
| Categoría no confirmada en Wompi | Funcionamiento técnico confirmado: 3 compras de prueba por el flujo normal, cobro acreditado en la cuenta de Wompi (según Michael; verificación con el panel pendiente, D13). Autorización estable de la categoría **NO confirmada** | PENDING (consulta escrita) → **DEFERRED / NON-BLOCKING** (DEC-020) |
| Contracargos | En productos íntimos algunos clientes disputan el cobro; el nombre en el extracto puede mitigarlo | UNKNOWN |
| Margen negativo o insuficiente | Depende de costos reales (proveedor, envío, comisiones, devoluciones) | UNKNOWN |
| Dependencia de una sola pasarela | Wompi activo; PayPal aparece en Shopify pero inactivo; app "Mercado Pago Tarjetas CO" instalada (si funciona como método de pago: UNKNOWN) | Reconocido |
| Acceso al panel de Wompi | Michael (empresa) no tiene acceso al panel; los fondos de las 3 pruebas están en Wompi. Quién administra la cuenta: UNKNOWN | DEFERRED / NON-BLOCKING (DEC-020; D13) |
| Situación fiscal / IVA / facturación | Empresa (Michael); facturación e IVA UNKNOWN | UNKNOWN (consultar contador); condición de GATE C |
| **SUPPLIER-RETAIL CHANNEL CONFLICT** | Vibrabien compra al mismo ecosistema/proveedor (SexoSentido / SexoSentido Mayoristas) que también vende los mismos SKU al detal en `sexosentido.co` (hecho confirmado por Michael). Interpretación: reduce la posibilidad de construir una ventaja sostenible basada únicamente en precio o en acceso al catálogo. UNKNOWN: razón social, relación jurídica entre dominios, exclusividad, prioridad de inventario, condiciones para revendedores, política de precios. **No es FAIL.** La propuesta de valor se decide en Fase 1. | Registrado (DEC-021) |

## 5. Métricas de seguimiento previstas (Fase 2+, no medir aún)

Visitas únicas a tienda desde Instagram · conversaciones iniciadas (por un canal permitido) · carritos iniciados · pedidos · una métrica cualitativa semanal (preguntas más repetidas). Se definen formalmente cuando exista baseline.
