# DESIGN.md — AlkanWeb Visual System & Token Architecture (Oficial)

## 1. Visual World & Corporate Philosophy
- **Identity**: B2B Metalmecánica Pesada, Mecanizado CNC, Soldadura Homologada y Montajes Industriales (**Taller Industrial Alkan S.A.S.** — Fundada en 1974, Guadalajara de Buga).
- **Aesthetic**: *Technical Precision Dark Mode B2B*. Sobrio, de alta ingeniería, con autoridad técnica. Cero "AI slop", cero gradientes genéricos de plantilla púrpura/azul, cero tarjetas repetitivas idénticas.
- **Tone**: Fiabilidad industrial pesada, tolerancias milimétricas ($\pm 0.02\text{ mm}$), seguridad de planta (SST y alturas) y relaciones contractuales de alto valor B2B.

---

## 2. Color Palette & Surface Tokens (Oficial Alkan)
- **Background Base**: `#0B111A` (Profundidad acero carbón/slate ultra-oscuro oficial)
- **Surface Elevation 1 (Navbar, Stats)**: `#101924`
- **Surface Elevation 2 (Paneles & Bento Grid)**: `#142130` con borde sutil de 1px en `#1E2D40`
- **Primary CTA Button**: `#235832` (Verde bosque corporativo profundo oficial del logo) con hover en `#2E6F40` y texto blanco puro `#FFFFFF`.
- **Corporate Accent / Highlights**: `#3A834E` / `#48A15F` (Verde corporativo elegante y de alto contraste medido > 4.5:1; **PROHIBIDO verde neón/esmeralda estridente**).
- **Primary Text**: `#FFFFFF` (Títulos e hitos principales).
- **Body Text**: `#CBD5E1` (Slate-300 de alta legibilidad técnica; medida estricta 65–75 caracteres por línea).
- **Secondary Text / Muted**: `#94A3B8` (Slate-400).
- **Borders & Dividers**: `1px solid #1E2D40`.

---

## 3. Typography Rules
- **Font Family**: Sans-serif geométrica técnica (`Plus Jakarta Sans`, `Inter`).
- **Headings**:
  - H1: 44px - 56px, `font-bold` o `font-extrabold`, tracking `-0.02em`.
  - H2: 32px - 40px, `font-bold`, tracking `-0.02em`.
  - H3: 20px - 24px, `font-semibold`.
- **Body**: 15px - 16px, line-height `1.6`, measure `65-75ch`.

---

## 4. Estructura de Navegación Oficial (Según DER 2.1)
- **Top Strip**: Planta Buga (Cra 24 N° 13-04 Barrio Palo Blanco) | Correo institucional | Teléfonos: 317 859 7112 · 314 508 0630 · 310 464 6032.
- **Menú**:
  1. `Inicio`
  2. `Nosotros` (Institucional, Misión, Visión, Historia 1974-Presente, Valores)
  3. `Servicios` (Torno, Mecanizado, Corte Plasma CNC, Soldadura, Montajes)
  4. `Infraestructura & SST` (Parque de maquinaria, Certificación alturas y espacios confinados)
  5. `Clientes` (Nutresa, Yara, Solla, Finca, Comolsa)
  6. `Contacto` (Formulario con casilla obligatoria de Habeas Data Ley 1581)
- **CTAs Principales**: `[ Solicitar Cotización ]` y `[ WhatsApp Directo ]`.
