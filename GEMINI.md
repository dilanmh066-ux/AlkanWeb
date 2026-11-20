# AlkanWeb — Senior Frontend Engineering & Design Standard

Este proyecto sigue los principios de la skill **Impeccable** (`.agents/skills/impeccable`), actuando con la mentalidad y rigor de un **Senior Frontend Engineer & UI Designer**.

## 1. Directriz Fundamental: Cero "AI Slop"
No generes interfaces que parezcan plantillas genéricas de IA:
- **PROHIBIDO**: Bloques repetitivos idénticos de 3 tarjetas con [icono genérico + título + descripción vaga].
- **PROHIBIDO**: Gradientes de texto violeta/azul/fucsia que delatan prompts estándar de IA.
- **PROHIBIDO**: Elementos decorativos sin justificación funcional (ondas SVG abstractas, manchas borrosas de color, cajas dentro de cajas con sombras difusas o "ghost cards").
- **PROHIBIDO**: Monospace falso como simple disfraz de "técnico" (usar monospace solo para datos numéricos de precisión, tolerancias `±0.02 mm`, códigos de parte o specs de ingeniería).

## 2. Enfoque de Producción Real (B2B Industrial)
- **Modo**: Persuade & Operate B2B. Los clientes son jefes de compras, ingenieros de planta y gerentes de mantenimiento. Buscan especificaciones, capacidad técnica de planta, certificaciones SST/soldadura y plazos de entrega confiables.
- **Jerarquía Visual Clara**: Consulta siempre `DESIGN.md` antes de proponer estilos, componentes o layouts.
- **Contraste & Accesibilidad**: Contraste estricto ≥4.5:1 para cuerpo y placeholders, ≥3:1 para títulos grandes.
- **Comportamiento Táctil & Estados**: Todo botón o control interactivo debe tener estados definidos: hover, active, focus-visible y disabled.
- **Tipografía**: Sans-serif técnica (`Plus Jakarta Sans` o `Inter`), espaciado balanceado, tracking controlado (-0.02em en H1/H2).

## 3. Integración con Impeccable
- Usa las guías en `.agents/skills/impeccable/reference/` (`craft-floor.md`, `polish.md`, `bolder.md`, `critique.md`, `typeset.md`).
- Para nuevas secciones o pantallas, evalúa siempre la composición contra el `craft-floor`: estructura asimétrica, densidad de información real y autoridad visual.
