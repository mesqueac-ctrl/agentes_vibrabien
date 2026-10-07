# EXPERIMENT_LOG.md

**Versión:** 0.1 (plantilla vacía) · **Creado:** 2026-10-05 · **Entradas hasta la fecha:** 0

Núcleo del sistema de aprendizaje. Ciclo: `EXPERIMENTO → OBSERVACIÓN → APRENDIZAJE DOCUMENTADO → NUEVA HIPÓTESIS`.
Sin significancia estadística con volúmenes pequeños: se registran señales y observaciones cualitativas, no "ganadores".

## Modelo: tres registros separados, relacionados por ID

Una venta puede existir sin experimento. Un experimento puede existir sin ventas. La operación puede terminar días después. **Una entrega fallida no es un experimento de marketing fallido.**

```
EXPERIMENT (experiment_id)
      ▲ nullable
SALE (order_id, experiment_id?)  ──  OPERATION (order_id)
```

(Es un modelo conceptual. No hay base de datos ni automatización.)

### 1. EXPERIMENT — `EXP-001`, `EXP-002`, …

| Campo | Contenido |
|---|---|
| experiment_id | EXP-### |
| Fecha inicio / fin | |
| **Pregunta que intenta responder** | Obligatorio. Sin pregunta, no hay experimento. |
| Hipótesis | "Si hacemos X para Y por el canal Z, esperamos W." |
| Acción | Qué se hizo exactamente |
| Canal | Ej.: Instagram orgánico |
| Público | |
| Costo (COP) | Dinero y horas |
| Resultado cuantitativo | Alcance, visitas al perfil, clics al sitio, mensajes recibidos, guardados, compartidos, visitas a tienda, carritos, pedidos (solo los que existan) |
| Observaciones cualitativas | Preguntas recibidas, comentarios, objeciones |
| Aprendizaje | Una o dos líneas |
| Decisión | `REPETIR` / `MODIFICAR` / `DESCARTAR` |
| Verificación de política | ¿Se revisó contra `BRAND_AND_AUDIENCE.md` §3-4? |

### 2. SALE — una fila por pedido

| Campo | Contenido |
|---|---|
| order_id | ID del pedido en Shopify |
| Fecha | |
| experiment_id | Nullable |
| **source_type** | Finalidad de la venta, no quién es el comprador. `OPERATIVE`: pedido deliberadamente buscado o reclutado para probar la operación, el fulfillment, el pago o la experiencia. `DEMAND`: pedido que ocurre por demanda comercial auténtica, sin reclutar al comprador específicamente para una prueba operacional. **No se clasifica automáticamente por quién es la persona.** |
| **source** | Origen del pedido: `friend` · `referral` · `instagram` · `creator` · `organic_search` · `other`. Combinaciones válidas, por ejemplo: `DEMAND` + `referral`; `OPERATIVE` + `friend`. (Nota: `whatsapp` no figura como fuente comercial; ver `DECISIONS.md` DEC-005.) |
| Valor del pedido (COP) | |
| Notas | |

### 3. OPERATION — una fila por pedido

| Campo | Contenido |
|---|---|
| order_id | |
| promised_at | Fecha/hora prometida |
| delivered_at | Fecha/hora real |
| fulfillment_result | `OK` / `LATE` / `DAMAGED` / `FAILED` / `PENDING` |
| issues | Qué pasó |
| Reembolso/queja | sí/no |

Un pedido cuenta para el OPERATIONAL GOAL solo si cumple la definición de `PROJECT.md` §2.

## Registros

*(vacío — se llena a partir de la Fase 2/3)*

### Experimentos
| ID | Pregunta | Canal | Decisión |
|---|---|---|---|
| — | — | — | — |

### Ventas
| order_id | experiment_id | source_type | source |
|---|---|---|---|
| — | — | — | — |

### Operación
| order_id | promised_at | delivered_at | fulfillment_result |
|---|---|---|---|
| — | — | — | — |
