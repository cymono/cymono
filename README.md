# 🍳 Wikitchen

### Sistema de planificación alimentaria personal · RAG + PKM + LLM

---

> **¿Llega a casa cansado después de una jornada extensa y termina comiendo cualquier cosa?**
> Wikitchen es un sistema simple que resuelve exactamente eso.

---

## ¿Qué es?

Wikitchen es un **wiki personal de cocina** que funciona como memoria externa para las decisiones alimentarias del día. Combina tres herramientas:

- 📚 **PKM (Obsidian)** — una carpeta de archivos de texto interconectados que organiza el inventario, las recetas y el plan semanal
- 🤖 **LLM (Claude Cowork)** — se le consulta qué preparar y responde considerando únicamente los ingredientes disponibles
- 🔍 **RAG** — el modelo no inventa ni sugiere ingredientes que no estén registrados; trabaja exclusivamente con el contexto que el usuario le entrega

El resultado: en menos de 2 minutos se tiene claro qué cocinar, con lo disponible en casa, en 15 minutos o menos.

---

## ¿Por qué funciona? La base neurocientífica

Los profesionales de la salud enfrentan jornadas extensas con privación parcial de sueño y carga cognitiva acumulada. Este contexto activa mecanismos fisiológicos concretos que afectan directamente la decisión alimentaria:

**1. Sistema orexinérgico activado**
La privación de sueño y el estrés crónico aumentan la actividad del sistema orexinérgico, incrementando el apetito y elevando la preferencia por alimentos de alta palatabilidad (ricos en grasa, azúcar o sal). Esto no es una preferencia arbitraria: es una respuesta adaptativa del sistema nervioso ante el déficit energético percibido.

**2. Agotamiento de la corteza prefrontal**
La corteza prefrontal —responsable del control ejecutivo, la planificación y la inhibición de impulsos— muestra agotamiento funcional progresivo durante jornadas de trabajo prolongadas. Al llegar a casa, esta región tiene menor capacidad de regular las decisiones alimentarias frente a la señal de recompensa inmediata que ofrecen los ultraprocesados.

**3. La brecha entre lo planificado y lo elegido**
La diferencia entre lo que se planifica comer en la mañana y lo que se elige al llegar cansado no refleja falta de voluntad. Refleja que **decidir tiene un costo cognitivo**, y al final del día ese costo ya fue pagado varias veces. El sistema límbico toma el control cuando la prefrontal está agotada.

**La solución no es más fuerza de voluntad — es menos decisiones.**

Wikitchen elimina la fricción de decidir. El usuario solo consulta; el sistema responde con una receta concreta, ejecutable, con lo que ya tiene en casa.

> *Referencias: Greer SM et al., Nature Communications 2013 · Krause AJ et al., Nature Reviews Neuroscience 2017 · Satterfield BC et al., Progress in Brain Research*

---

## La estructura es minimalista

```
Wikitchen/
│
├── inventario.md       ← Todo lo disponible en despensa, refrigerador y congelador
├── objetivos.md        ← Metas nutricionales personales
├── plan-semanal.md     ← Plan de comidas de la semana
├── index.md            ← Índice central con links a todo
├── log.md              ← Historial de cambios
│
└── recetas/
    ├── arroz-con-huevo-y-verduras.md
    ├── poroto-negro-express.md
    ├── crema-brocoli-arvejas.md
    └── ...
```

Cada receta incluye: tiempo de preparación, ingredientes, pasos y estimación proteica.

---

## El inventario va más allá de los alimentos

Una de las ventajas del sistema es que el inventario puede incluir **todo lo que está disponible en la cocina**: ingredientes, especias, condimentos, utensilios e implementos. Esto permite que Claude Cowork genere recetas completamente ajustadas a la realidad del usuario — no solo a lo que tiene para comer, sino también a **cómo puede cocinarlo**.

### Ejemplo real — Mi inventario con mis alimentos. 

#### 🥩 Proteínas y legumbres
| Producto | Estado |
|----------|--------|
| Lentejas | Seco |
| Garbanzos | Seco |
| Porotos negros | En conserva |
| Porotos blancos | En conserva |
| Atún | En conserva |
| Carne de soya | Seco |
| Pollo | Congelado |
| Carne molida | Congelada |
| Huevos | Refrigerador |

#### 🥦 Verduras y frutas
| Producto | Estado |
|----------|--------|
| Acelga, lechuga, zanahorias | Refrigerador |
| Pepino, pimentón, tomate | Refrigerador |
| Papa, ají verde, limones | Refrigerador |
| Arvejas | Congeladas |
| Brócoli | Congelado |
| Zapallo | Congelado |

#### 🌶️ Especias y condimentos
| Producto |
|----------|
| Merquén, orégano, albahaca deshidratada |
| Ajo en polvo, jengibre molido, ajicolor |
| Glutamato monosódico, sal |
| Salsa de tomate, tahini, aceto balsámico |
| Vinagre de vino blanco, vinagre de manzana |

#### 🍳 Utensilios e implementos
| Utensilio | Uso principal |
|-----------|--------------|
| Easy Soup | Sopas, cremas y guisos en minutos |
| Olla a presión Thomas PC 40 | Legumbres, batch cooking, carnes |

Con este contexto completo, Claude Cowork puede responder consultas como: *"Tengo 15 minutos, quiero algo con proteína y solo puedo usar el Easy Soup"* — y generar una receta ejecutable al instante.

---

## Cómo replicarlo

**Se necesita:**
- [Obsidian](https://obsidian.md) (gratuito) — para visualizar y navegar los archivos
- [Claude Cowork](https://claude.ai) — con acceso a la carpeta del proyecto
- Esta estructura de archivos, adaptada al inventario propio

**El flujo:**

1. Se registra el inventario personal en `inventario.md` — alimentos, especias, utensilios
2. Se abre Claude Cowork con la carpeta del proyecto como contexto
3. Se consulta: *"Tengo 15 minutos y quiero algo con proteína, ¿qué preparo?"*
4. Claude Cowork cruza inventario + objetivos nutricionales + tiempo disponible y genera la receta con pasos detallados

**Tiempo de configuración inicial: aproximadamente 30 minutos.**

---

## Objetivos nutricionales base

- ✅ Mínimo 20–25 g de proteína por comida
- ✅ Alta fibra
- ✅ Alimentos reales, sin ultraprocesados
- ✅ Máximo 15 minutos de preparación para la cena

---

## Ejemplo de interacción real

> **Consulta:** *"Llegué cansado. Tengo arroz cocido, huevos y brócoli congelado. Máximo 12 minutos."*
>
> **Wikitchen responde:**
> **Arroz salteado con huevo y brócoli** · 12 min · ~22 g proteína · Alta fibra
> 1. Calentar el arroz (2 min en microondas o sartén)
> 2. Saltear brócoli congelado con aceite y ajo en polvo (4 min)
> 3. Agregar 2 huevos batidos, revolver hasta cuajar (3 min)
> 4. Condimentar con salsa de tomate, merquén y glutamato monosódico

---

## El concepto en una línea

**Menos fricción en la decisión → mejores elecciones alimentarias → mejor salud.**

---

*Presentado en el Congreso Medicina del Futuro Presente · Mayo 2026*
*Dr. Simón Sabattín · Médico · Redgesam / Redsalud*
