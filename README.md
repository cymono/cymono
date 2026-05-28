# 🍳 Wikitchen

### Sistema de planificación alimentaria personal · RAG + PKM + LLM

---

> **¿Llega a casa cansado y termina comiendo cualquier cosa?**
> Wikitchen es un sistema simple que resuelve exactamente eso.

---

## ¿Qué es?

Wikitchen es un **wiki personal de cocina** que funciona como memoria externa para las decisiones alimentarias. Combina tres herramientas:

- 📚 **PKM (Obsidian)** — una carpeta de archivos de texto que conecta el inventario con las recetas
- 🤖 **LLM (Claude Cowork)** — se le consulta "¿qué como hoy?" y responde en base al inventario disponible
- 🔍 **RAG** — el modelo no inventa ingredientes; trabaja únicamente con lo que el usuario registró

El resultado: en menos de 2 minutos se tiene claro qué cocinar, con lo disponible en casa, en 15 minutos o menos.

---

## ¿Por qué funciona?

Al llegar cansados, la corteza prefrontal ya presenta agotamiento funcional. No es falta de voluntad: es neurociencia. El problema no es saber qué comer — es que **decidir consume energía que ya no se tiene**.

Wikitchen elimina la decisión. El usuario solo consulta; el sistema responde.

---

## La estructura es minimalista

```
Wikitchen/
│
├── inventario.md       ← Todo lo disponible en casa
├── objetivos.md        ← Metas nutricionales personales
├── plan-semanal.md     ← Plan de comidas de la semana
├── index.md            ← Índice central
├── log.md              ← Historial de cambios
│
└── recetas/
    ├── arroz-con-huevo-y-verduras.md
    ├── poroto-negro-express.md
    └── ...
```

Cada receta incluye: tiempo de preparación, ingredientes, pasos y proteínas estimadas.

---

## Cómo replicarlo

**Se necesita:**
- [Obsidian](https://obsidian.md) (gratuito) — para visualizar y navegar los archivos
- [Claude Cowork](https://claude.ai) — el modelo de lenguaje con acceso a la carpeta
- Esta estructura de archivos

**El flujo:**

1. Se abre Claude Cowork con la carpeta del proyecto como contexto
2. Se consulta: *"Tengo 15 minutos y quiero algo con proteína, ¿qué preparo?"*
3. Claude Cowork lee el inventario y genera una receta con los pasos detallados

**Tiempo de configuración inicial: ~30 minutos.**

---

## Objetivos nutricionales base

- ✅ Mínimo 20–25 g de proteína por comida
- ✅ Alta fibra
- ✅ Alimentos reales, sin ultraprocesados
- ✅ Máximo 15 minutos de preparación para la cena

---

## Ejemplo real

> **Consulta:** *"Estoy cansado, tengo arroz cocido, huevos y brócoli congelado"*
>
> **Wikitchen responde:** Arroz salteado con huevo y brócoli · 12 min · ~22g proteína · Alta fibra

---

## El concepto en una línea

**Menos fricción → mejores decisiones → mejor alimentación.**

---

*Presentado en el Congreso Medicina del Futuro Presente · Mayo 2026*
*Dr. Simón Sabattín · Médico · Redgesam / Redsalud*
