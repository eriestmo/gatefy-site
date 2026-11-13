---
name: Gatefy
description: Control de acceso multiempresa para edificios, presentado por Tech Advisors LA.
colors:
  surface: "#0A1628"
  surface-band: "#0E1D38"
  card: "#112240"
  audit-deep: "#07101F"
  text: "#F0F6FF"
  text-2: "#C3CFDF"
  muted: "#8FA3BB"
  mint: "#00E5A0"
  mint-hover: "#5CF2C3"
  on-mint: "#06231A"
  danger: "#FF7A7A"
  danger-text: "#FF8C80"
  visit-blue: "#8DB3FF"
  warn-amber: "#FFB86B"
typography:
  display:
    fontFamily: "General Sans, Space Grotesk, system-ui, sans-serif"
    fontSize: "clamp(2.6rem, 5.6vw, 4.7rem)"
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  headline:
    fontFamily: "General Sans, Space Grotesk, system-ui, sans-serif"
    fontSize: "clamp(2rem, 4vw, 3.2rem)"
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: "-0.02em"
  title:
    fontFamily: "General Sans, Space Grotesk, system-ui, sans-serif"
    fontSize: "clamp(1.6rem, 2.8vw, 2.2rem)"
    lineHeight: 1.05
  body:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "Inter, system-ui, sans-serif"
    fontSize: "0.85rem"
    fontWeight: 600
  data:
    fontFamily: "JetBrains Mono, ui-monospace, monospace"
    fontSize: "1.35rem"
    fontWeight: 500
rounded:
  input: "10px"
  button: "12px"
  card: "22px"
  pill: "50px"
spacing:
  gutter: "24px"
  feature: "3.2rem"
  section: "6.5rem"
components:
  button-primary:
    backgroundColor: "{colors.mint}"
    textColor: "{colors.on-mint}"
    rounded: "{rounded.button}"
    padding: "0.95rem 1.5rem"
  button-primary-hover:
    backgroundColor: "{colors.mint-hover}"
  input:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.text}"
    rounded: "{rounded.input}"
    padding: "0.8rem 0.9rem"
  panel:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.card}"
    padding: "1.2rem"
  feature-visual:
    backgroundColor: "{colors.surface-band}"
    rounded: "{rounded.card}"
    padding: "1.6rem"
---

# Design System: Gatefy

## Overview

**Creative North Star: "El registro sereno"**

Todo queda anotado, claro y sin alarma: seguridad que da calma. La landing usa el mismo tema oscuro que el portal de Gatefy, así quien la ve y después entra a la app reconoce la misma marca. Azul marino profundo de fondo, tarjetas un tono más claro y un solo verde menta para la acción y para "acceso permitido".

La densidad es media. Cada función se cuenta en una franja con texto a un lado y una demostración animada al otro. El tono es de servicio: claro, sin jerga de ciberseguridad. Todo lo que muestra el panel está marcado como "Datos de ejemplo".

**Key Characteristics:**
- Tema oscuro del portal: el fondo, las tarjetas y el menta son los mismos de la app.
- Un solo acento, el menta; el rojo solo para accesos negados y errores.
- Titulares pesados (800) en General Sans; cuerpo en Inter de 17px.
- Datos, horas y cifras en JetBrains Mono.

## Colors

Noche marina con una sola luz verde: la del acceso permitido.

### Primary
- **Menta** (mint): botones, palabras destacadas del H1, viñetas, pasos activos, foco y estado "activo". El texto sobre menta va siempre en verde casi negro (on-mint, 10:1).

### Tertiary
- **Rojo suave** (danger, danger-text): "Revocado", accesos negados y errores de formulario.
- **Azul visita** (visit-blue) y **ámbar** (warn-amber): solo dentro del panel y la bitácora, para distinguir tipos de evento.

### Neutral
- **Fondo** (surface): la página y los campos.
- **Franja** (surface-band): secciones alternas y fondo de las demostraciones.
- **Tarjeta** (card): panel de eventos, pasos, formularios y tarjetas.
- **Bitácora** (audit-deep): el registro de auditoría, un tono más hondo.
- **Texto** (text) para titulares, **texto 2** (text-2) para párrafos y **gris** (muted) para lo secundario (5.6:1 o más sobre cualquier fondo).
- **Línea** (`rgba(240,246,255,.1)`): bordes y separadores.

### Named Rules
**The One Light Rule.** El menta es la única luz de la página. Si todo brilla, nada se ve permitido.

**The Same As The App Rule.** Los colores salen de los tokens `--g-*` del portal. Si el portal cambia, la landing cambia con él.

## Typography

**Display Font:** General Sans (con Space Grotesk y system-ui), autoalojada.
**Body Font:** Inter (con system-ui)
**Data Font:** JetBrains Mono

### Hierarchy
- **Display** (800, clamp 2.6–4.7rem, 1.05): solo el H1.
- **Headline** (800, clamp 2–3.2rem): títulos de sección.
- **Title** (clamp 1.6–2.2rem): título de cada función.
- **Body** (400, 17px, 1.6): párrafos de 44ch como máximo.
- **Label** (600, 0.85rem): eyebrows y etiquetas.
- **Data** (JetBrains Mono 500, cifras tabulares): números y horas del panel.

## Layout

Contenedor de 1200px con margen de 24px (o el área segura del iPhone). Secciones de 6.5rem. Las funciones alternan texto y demostración en dos columnas, separadas por líneas finas. Cortes en 960px y 560px; en celular todo pasa a una columna y el panel esconde las horas.

## Elevation & Depth

La profundidad viene de los tonos: fondo, franja y tarjeta, cada uno un poco más claro. Las sombras son negras y largas, solo para el panel de eventos y el formulario.

### Shadow Vocabulary
- **Panel flotante** (`box-shadow: 0 40px 80px -30px rgba(0,0,0,.6), 0 0 0 1px rgba(240,246,255,.1)`): solo el panel de eventos del hero.
- **Formulario** (`box-shadow: 0 24px 50px -30px rgba(0,0,0,.5)`): la tarjeta del formulario de demo.

### Named Rules
**The Tone Steps Rule.** Para separar, primero un tono de fondo; después una línea; la sombra es lo último.

## Shapes

Esquinas de 22px en paneles y demostraciones, 12px en botones, 10px en campos y píldoras de 50px en las etiquetas. Las viñetas son cuadrados menta de 8px con 2px de radio.

## Components

### Buttons
- **Shape:** 12px (10px en el encabezado).
- **Primary:** menta con texto on-mint, 600, padding 0.95rem 1.5rem.
- **Hover / Focus:** pasa a menta claro y sube 1px; al presionar se encoge al 98%. Foco con contorno menta de 2px.
- **Enlace (`.lnk`):** texto en peso 600 con un subrayado de línea que se aclara en hover.

### Chips / Tags
- **Disponible:** menta sobre menta translúcido.
- **Próximamente:** gris claro sobre blanco translúcido.

### Inputs / Fields
- **Style:** fondo de página dentro de la tarjeta del formulario, borde de línea, 10px.
- **Focus:** borde menta con anillo menta translúcido de 3px.

### Navigation
Barra pegajosa de 72px con fondo marino translúcido y desenfoque; muestra la línea inferior solo al hacer scroll. El logo es la versión para fondo oscuro (`assets/gatefy-logo-oscuro.svg`).

### Panel de eventos en vivo (Signature Component)
Una tarjeta con tres cifras (accesos, visitas activas, equipos en línea) y una lista de eventos con punto de estado, persona, puerta y hora. Siempre lleva la nota "Datos de ejemplo".

## Do's and Don'ts

### Do:
- **Do** marcar como "Datos de ejemplo" todo dato de demostración.
- **Do** escribir el texto sobre menta en on-mint, nunca en blanco.
- **Do** usar el logo para fondo oscuro.
- **Do** atenuar con el gris (muted), nunca con `opacity`.
- **Do** respetar el área segura del iPhone (`env(safe-area-inset-*)`).

### Don't:
- **Don't** volver a fondos crema o blancos.
- **Don't** usar el menta como decoración: significa acción o acceso permitido.
- **Don't** mostrar capturas o cifras como si fueran de un cliente real.
