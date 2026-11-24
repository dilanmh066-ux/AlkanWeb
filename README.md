# Portal Web Corporativo B2B — Taller Industrial Alkan S.A.S.

Repositorio oficial del portal web institucional y plataforma de cotización técnica para **Taller Industrial Alkan S.A.S.** (Guadalajara de Buga, Valle del Cauca, Colombia), empresa con más de 50 años de trayectoria (fundada en 1974) en mecanizado de precisión, soldadura especializada, rolado de lámina y mantenimiento mecánico en planta.

Proyecto desarrollado en el marco de la **Etapa Productiva del SENA** (Tecnología en Análisis y Desarrollo de Software / ADSO).

---

## 📌 Información General del Proyecto

- **Razón Social:** Taller Industrial Alkan S.A.S. (NIT: 900.882.264-6)
- **Sector:** Metalmecánica pesada, mecanizado de precisión, soldadura calificada y servicios técnicos en sitio para los sectores industrial y agroindustrial.
- **Ubicación de Planta:** Cra 24 N° 13-04, Barrio Palo Blanco, Guadalajara de Buga, Valle del Cauca.
- **Contacto Corporativo:** 312 724 6772 · 317 859 7112 · 314 508 0630 · 310 464 6032 | Correo: `alcam_uno@yahoo.com`
- **Desarrollador / Aprendiz SENA:** Dilan Hernández
- **Supervisión Empresarial:** Paola Villada (Jefe de Etapa Productiva) / Gerardo García (Representante Legal)
- **Fecha de Inicio:** 19 de noviembre de 2026
- **Estado y Fase Actual:** **Fase 2 / 3 — Implementación, Arquitectura Serverless y Despliegue Continuo (Staging / Producción en Render).**

---

## 📂 Estructura Oficial del Repositorio

```text
AlkanWeb/
├── vistas/                          # Frontend funcional y vistas del portal corporativo
│   ├── index.html                   # Portada principal B2B, propuesta de valor y bento grid
│   ├── nosotros.html                # Trayectoria (1974), soldadores calificados y personal SST
│   ├── servicios.html               # Catálogo interactivo y cotizador técnico contextual
│   ├── politica-datos.html          # Cumplimiento legal y política de privacidad (Ley 1581)
│   ├── cotizacion.html              # Enrutador de compatibilidad y redirección a servicios
│   ├── services.data.json           # Especificaciones técnicas estructuradas de maquinaria
│   ├── styles.css                   # Tokens complementarios de estilo y scrollbars
│   └── RecursosVisuales/            # Logos corporativos de alta resolución e insumos gráficos
├── DiagramasUML/                    # Modelado formal de software (Casos de uso y flujos en Draw.io)
│   ├── UML WebAlkanc.drawio.png     # Diagrama de Casos de Uso
│   └── UML WebAlkanD.drawio.png     # Diagrama de Despliegue y Flujo de Datos
├── DocumentacionERS/                # Documentación formal de ingeniería de requisitos
│   └── ESPECIFICACIÓN DE REQUISITOS DE SOFTWARE.docx  # Documento base ERS (IEEE 830)
├── Pendientes/                      # Bitácora y actas de seguimiento de etapa productiva
├── DESIGN.md                        # Sistema de diseño oficial B2B (tokens, paleta y tipografía)
├── PRODUCT.md                       # Especificación de producto, público objetivo y factores de confianza
├── AGENTS.md / GEMINI.md            # Directrices de ingeniería frontend y estándares de calidad
├── .gitignore                       # Control de exclusiones (binarios, herramientas locales y dependencias)
└── README.md                        # Ficha técnica y documentación general del proyecto
```

---

## 🛠️ Stack Tecnológico y Arquitectura

El proyecto está diseñado bajo una arquitectura web **estática de alto rendimiento (Zero Cold-Start)**, garantizando disponibilidad 24/7 sin caídas de servidores ni demoras en la carga:

* **Estructura y Maquetación:** HTML5 semántico con accesibilidad WAI-ARIA y optimización Mobile-First.
* **Sistema de Estilos:** [Tailwind CSS v3](https://tailwindcss.com/) (vía CDN optimizado) basado en el sistema de diseño estricto definido en `DESIGN.md` (*Technical Precision Dark Mode*: `#0B111A`, `#101924`, verde bosque `#235832`, texto Slate-300).
* **Tipografía:** Sans-serif geométrica de alta legibilidad técnica (`Plus Jakarta Sans` e `Inter`).
* **Lógica del Cliente:** JavaScript moderno (ES6+ modular nativo) para interactividad fluida, filtrado de servicios y validaciones de formulario.
* **Procesamiento de Cotizaciones (Serverless):** [Web3Forms API](https://web3forms.com/) para entrega directa de prospectos al correo electrónico corporativo con respuesta JSON asíncrona (`fetch`), protección contra envíos dobles y contingencia directa vía WhatsApp.
* **Control de Versiones y Despliegue Continuo (CI/CD):** Git y GitHub conectado a **Render Static Sites** con compilación y despliegue automático ante cada push a la rama `main`.

---

## 📋 Módulo de Cotización Técnica y Seguridad

El formulario de cotización en `vistas/servicios.html` implementa estándares de nivel de producción:

1. **Captura de Datos B2B:** Nombres y apellidos, empresa / razón social, teléfono/celular de contacto, correo corporativo y especificaciones del requerimiento técnico.
2. **Contexto Automático por Servicio:** Detecta si el cliente cotiza *Torno*, *Soldadura Especializada*, *Mantenimiento y Montaje*, *Rolado de Lámina* o *Fresado*, asignando el asunto correspondiente en el correo y en el enlace de contingencia.
3. **Mecanismo Anti-Spam:** Campo trampa *honeypot* invisible (`botcheck`) que descarta envíos automatizados de bots sin afectar la experiencia del usuario.
4. **Validación en Cliente:** Comprobación de campos obligatorios, sintaxis de correo electrónico y números telefónicos de Colombia (mínimo 10 dígitos).
5. **Cumplimiento Legal (Ley 1581 de 2012):** Casilla obligatoria de autorización expresa para el tratamiento de datos personales conforme al Régimen General de Protección de Datos de Colombia.
6. **Manejo de Errores y Contingencia WhatsApp:** Si la red del cliente falla o se interrumpe la conexión, el formulario conserva todos los datos ingresados y activa un botón de WhatsApp directo con el mensaje técnico estructurado hacia la línea comercial (`310 464 6032`).
7. **Respuesta Directa:** Configuración de cabecera `replyto` para responder al cliente con un solo clic desde Gmail/Yahoo Mail.

---

## 🚀 Despliegue y Ejecución Local

### Previsualización Local
No se requieren dependencias pesadas de Node.js ni bases de datos locales:
1. Clonar el repositorio:
   ```bash
   git clone https://github.com/dilanmh066-ux/AlkanWeb.git
   cd AlkanWeb
   ```
2. Abrir cualquier archivo de la carpeta `vistas/` (`index.html`, `servicios.html`, etc.) directamente en el navegador, o mediante la extensión **Live Server** de VS Code.

### Despliegue en Producción
El repositorio está integrado con **Render** como un *Static Site*. Todo commit subido a la rama `main` ejecuta un build automático y actualiza el sitio en producción de forma instantánea.

---

## ⚖️ Marco Legal y Normativo

- **Ley 1581 de 2012 y Decreto 1377 de 2013:** Política integral de protección y tratamiento de datos personales disponible en `vistas/politica-datos.html`.
- **Ley 527 de 1999:** Validez y eficacia de mensajes de datos y comercio electrónico en Colombia.
- **Resolución 4272 de 2021:** Especificación y acreditación de personal calificado en trabajo seguro en alturas para paradas de planta y montajes industriales.
