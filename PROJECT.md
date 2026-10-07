# PROJECT.md — VIBI Marketing OS

**Versión:** 0.2 · **Creado:** 2026-10-05 · **Estado:** Fase 0a COMPLETADA — PASS WITH CONDITIONS (DEC-021, 2026-10-06); 0b no iniciada
**Dueño y decisor final:** Michael · **Colaboradores:** Claude, ChatGPT (Codex solo ante problemas técnicos concretos)

> Documento corto a propósito. Si crece, algo está mal.

## 1. Qué es

**Vibrabien** (vibrabien.co) es una tienda Shopify colombiana de bienestar íntimo. Mercado inicial: Barranquilla; vende a toda Colombia. Instagram: `@vibrabien_col`.

**VIBI Marketing OS** es el nombre de la *visión*: un sistema que aprende qué funciona para Vibrabien. La v0.1 es deliberadamente mínima:

> **v0.1 = experimentos manuales + documentación + medición.**

No hay integraciones operativas, automatizaciones ni agentes. Las integraciones nativas exclusivamente de medición podrán aprobarse en 0a.1. Nada de lo demás se construye hasta que exista un proceso manual estable.

## 2. Objetivo actual

Dos objetivos separados (no mezclar):

| Objetivo | Definición | Estado |
|---|---|---|
| **OPERATIONAL GOAL** | 10 pedidos **cumplidos correctamente**: entregados en el plazo prometido, producto intacto, empaque discreto, cliente confirma recepción, sin reembolso ni queja. | No iniciado |
| **DEMAND GOAL** | Primeras ventas de personas ajenas a la red directa de Michael, por un canal identificable. Sin número obligatorio hasta conocer el tráfico actual. | No iniciado |

Cada venta se etiqueta `OPERATIVE` o `DEMAND` (ver `EXPERIMENT_LOG.md`).

## 3. Principios

1. **Diseñar primero, automatizar después.**
2. **No escalar demanda antes de poder cumplirla con margen positivo.**
3. **Cada experimento debe decir qué pregunta intenta responder.**
4. **Medir antes de optimizar.** Sin significancia estadística con volúmenes pequeños: experimentos cualitativos y señales.
5. **Ausencia de prohibición encontrada ≠ autorización.**
6. **Vibrabien diseñará creatividad para el canal, no creatividad para evadir la moderación del canal.**
7. **Las referencias de competidores se usan para identificar patrones y principios, nunca para copiar activos.**
8. **Nada pasa a "hecho" sin fuente.** Lo no comprobado se marca `UNKNOWN`, `PENDING` o `NOT VERIFIED`.
9. **Todo gasto se justifica por separado.** No hay presupuesto fijo.
10. **Aprobación humana antes de cualquier acción pública importante. No hay publicación automática.**

## 4. Fases

| Fase | Pregunta que responde | Estado |
|---|---|---|
| **0a — Baseline** | ¿Dónde estamos realmente? (solo lectura) | **COMPLETADA — PASS WITH CONDITIONS** (DEC-021, 2026-10-06) |
| **0a.1 — Medición** | ¿Podemos medir? GA4 vía integración oficial de Shopify, solo analítica | No iniciada; según la definición existente, puede prepararse en paralelo cuando corresponda, sin retrasar el diseño operativo |
| **0b — Promesa y operación** | ¿Podemos cumplir lo que prometemos? Incluye simulacro real | **NO INICIADA** (no aprobada automáticamente; ver gates en §4.1) |
| **1 — Público y oferta** | ¿A quién vender primero y con qué oferta? | No iniciada |
| **2 — Experimentos orgánicos** | ¿Qué contenido o canal genera atención cualificada? Puede empezar parcialmente tras 0a (sin contenido comercial de producto hasta Fase 1) | No iniciada |
| **3 — Primeras ventas** | ¿Se cumplen 10 pedidos correctamente? | No iniciada |
| **4 — Canal frío / inversión** | ¿Hay un canal frío rentable? Solo si 0b y 3 salieron bien | No iniciada |
| **5 — Automatización** | ¿Qué tarea estable, medible, de bajo riesgo y reversible merece automatizarse? | No iniciada |

### 4.1 Gates de 0b (DEC-021)

0a = PASS WITH CONDITIONS **no significa** negocio listo para escalar, operación validada, margen final confirmado ni primeros clientes autorizados.

| Gate | Qué habilita | Condición | Estado |
|---|---|---|---|
| **A** | Inicio del **diseño** de 0b: flujo operativo, SOP, promesa, escenarios de envío y estructura del simulacro, sin tocar Shopify | — | **ABIERTO** |
| **B** | **Ejecutar el simulacro** | Conocer como mínimo: costo vigente de la muestra; disponibilidad real; método para confirmar stock; tiempo proveedor → Vibrabien; horario y corte; mínimo de compra; método de pago; posibilidad de despacho directo; empaque neutro o directo si existe; política básica de defectos y garantía. Si no está claro, no se ejecuta el simulacro. | No cumplido (falta la llamada al proveedor) |
| **C** | Una **venta comercial real** | Gate B, más: logística real y costo; plazo prometido; proceso cuando un SKU no está disponible; canal de atención permitido; decisión sobre el botón de WhatsApp Business; facturación y tratamiento fiscal suficientemente definidos; corrección de claims y productos críticos (Brandy/Crystal, Gel Exótico, Twin Fork); política operativa de devoluciones y cambios, junto con una vía identificada para verificar que un pago fue recibido y ejecutar un reembolso si fuera necesario (por la persona actualmente autorizada o el procedimiento disponible; no exige acceso personal de Michael al panel); medición suficiente para identificar el origen de la venta. Wompi no se exige (DEC-020). | No cumplido |

Medición y Merchant Center no bloquean el diseño de 0b. La anomalía de medición se resuelve antes de experimentos serios de adquisición o demanda. Merchant Center es paralelo y no bloqueante.

Contenido orgánico en paralelo: puede **educar y construir marca**. No puede prometer entrega, disponibilidad, tiempos, descuentos ni condiciones logísticas no verificadas, ni incluir urgencia artificial.

## 5. Límites (lo que NO se hace en esta etapa)

- No agentes, workflows, n8n, integraciones operativas ni código de producción (excepción: integraciones nativas de solo medición en 0a.1).
- No cambios en Shopify sin decisión explícita de Michael (0a fue de solo lectura; el diseño de 0b tampoco toca Shopify).
- No pauta ni promociones.
- No WhatsApp Business como canal comercial (la política fue verificada por ambas IAs: prohíbe la categoría "Adult products and services"; ver `DECISIONS.md` DEC-005). La decisión sobre el botón que hoy existe en la web es condición del GATE C.
- No TikTok ni Google Ads en el registro de políticas hasta que se vayan a usar.
- No decisiones de stock hasta tener datos de proveedor y margen.

## 6. Colaboración

- División por **fortalezas, no por permisos**. Michael decide.
- **Opiniones independientes** (cada IA sin ver la conclusión de la otra) cuando una decisión tenga alto impacto o alto costo de reversión: gasto relevante, contratos, proveedor, checkout, pasarela, claims de producto, decisiones legales, automatizaciones públicas, datos de clientes, pricing importante, compra significativa de stock, arquitectura difícil de revertir. No se usa para textos, captions o ajustes menores.
- Un documento nuevo debe justificar su existencia. Los seis actuales: `PROJECT`, `BRAND_AND_AUDIENCE`, `EXPERIMENT_LOG`, `METRICS`, `DECISIONS`, `OPERATIONS`.
- No compartir credenciales, llaves ni datos personales de clientes en chats ni documentos.

## 7. Estado

0a completada con condiciones (`DECISIONS.md` DEC-021). Estado final de D1-D16 en `METRICS.md` §1.2; condiciones que pasan a 0b en `DECISIONS.md`; ficha del proveedor (GATE B) en `OPERATIONS.md` §2. **Proveedor confirmado por Michael: SexoSentido / SexoSentido Mayoristas, que también vende al consumidor final en `sexosentido.co`** (riesgo `SUPPLIER-RETAIL CHANNEL CONFLICT`, no es FAIL). La propuesta de valor es de Fase 1.
