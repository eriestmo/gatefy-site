---
name: Gatefy
description: Control de acceso multiempresa para edificios, presentado por Tech Advisors LA.
colors:
  brand-blue: "#2A6FEA"
  brand-blue-deep: "#1F58C4"
  access-green: "#1FA582"
  access-green-text: "#14785E"
  signal-green: "#00E5A0"
  alert-red: "#D9483B"
  alert-red-text: "#B4352A"
  cream: "#F4F2E2"
  paper: "#FBFAF3"
  ink: "#0A1628"
  ink-2: "#2B3648"
  muted: "#5D6676"
  grey: "#9CA3A8"
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
    backgroundColor: "{colors.brand-blue}"
    textColor: "#FFFFFF"
    rounded: "{rounded.button}"
    padding: "0.95rem 1.5rem"
  button-primary-hover:
    backgroundColor: "{colors.brand-blue-deep}"
  input:
    backgroundColor: "{colors.cream}"
    textColor: "{colors.ink}"
    rounded: "{rounded.input}"
    padding: "0.8rem 0.9rem"
  panel:
    backgroundColor: "{colors.ink}"
    rounded: "{rounded.card}"
    padding: "1.2rem"
  feature-visual:
    backgroundColor: "{colors.paper}"
    rounded: "{rounded.card}"
    padding: "1.6rem"
---

# Design System: Gatefy

## Overview

**Creative North Star: "La portería moderna"**

Gatefy es la recepción del edificio hecha software: ordenada, amable y con control. La página se siente como un mostrador bien llevado: papel crema, tinta azul marino y un azul de marca que guía sin gritar. Frente a esa calma, el panel oscuro de eventos en vivo es el puesto de seguridad: datos en tipografía mono, puntos de estado y horas exactas.

La densidad es media. Cada función se cuenta en una franja con texto a un lado y una demostración animada al otro. El tono es de servicio: claro, sin alarma y sin jerga de ciberseguridad. Todo lo que muestra el panel está marcado como "Datos de ejemplo".

**Key Characteristics:**
- Fondo crema y papel; nada de blanco puro de fondo.
- Un solo azul de marca para la acción; verde y rojo solo para estados de acceso.
- Titulares pesados (800) en General Sans; cuerpo en Inter de 17px.
- Panel oscuro de eventos como pieza firma.

## Colors

Papel crema con tinta marina: una portería a plena luz.

### Primary
- **Azul de marca** (brand-blue): botones y palabras destacadas del H1. Sobre crema solo sirve para texto grande; el texto pequeño en azul usa el azul profundo (brand-blue-deep, 5.7:1).

### Secondary
- **Verde de acceso** (access-green): bordes y puntos de estado "activo". Como texto se usa su tono oscuro (access-green-text).
- **Verde señal** (signal-green): punto "En vivo" y etiquetas sobre el panel oscuro.

### Tertiary
- **Rojo de alerta** (alert-red): estado "Revocado" y errores. Como texto se usa alert-red-text.

### Neutral
- **Crema** (cream): fondo de la página y de los campos.
- **Papel** (paper): fondo de las demostraciones de cada función.
- **Tinta** (ink): titulares y fondo del panel de eventos.
- **Tinta 2** (ink-2): párrafos.
- **Gris medio** (muted): texto secundario y pasos inactivos (5.8:1 sobre blanco).
- **Línea** (`rgba(10,22,40,.12)`): bordes y separadores.

### Named Rules
**The Status Color Rule.** El verde y el rojo significan acceso permitido y acceso negado. No se usan como decoración.

**The Text Tone Rule.** Un color de marca usado como texto pequeño va en su tono de texto (brand-blue-deep, access-green-text, alert-red-text), que llega a 4.5:1 o más.

## Typography

**Display Font:** General Sans (con Space Grotesk y system-ui), autoalojada.
**Body Font:** Inter (con system-ui)
**Data Font:** JetBrains Mono

**Character:** General Sans pesada da firmeza de marca; Inter mantiene la lectura cómoda; la mono se reserva para cifras, horas y códigos del panel.

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

El sistema es plano sobre crema. La única pieza elevada es el panel oscuro de eventos, que flota con una sombra larga y suave. El foco de los campos es un anillo azul translúcido de 3px.

### Shadow Vocabulary
- **Panel flotante** (`box-shadow: 0 40px 80px -30px rgba(10,22,40,.55), 0 0 0 1px rgba(10,22,40,.9)`): solo el panel de eventos del hero.
- **Tarjeta suave** (`box-shadow: 0 24px 50px -30px rgba(10,22,40,.25)`): tarjetas que se separan del fondo.

### Named Rules
**The One Floating Panel Rule.** Solo una pieza flota por pantalla. Lo demás se separa con líneas y fondos, no con sombras.

## Shapes

Esquinas de 22px en paneles y demostraciones, 12px en botones, 10px en campos y píldoras de 50px en las etiquetas. Las viñetas son cuadrados azules de 8px con 2px de radio.

## Components

### Buttons
- **Shape:** 12px (10px en el encabezado).
- **Primary:** azul de marca con texto blanco, 600, padding 0.95rem 1.5rem.
- **Hover / Focus:** pasa al azul profundo y sube 1px; al presionar se encoge al 98%. Foco con contorno azul de 2px.
- **Enlace (`.lnk`):** texto en peso 600 con un subrayado de línea que se oscurece en hover.

### Chips / Tags
- **Disponible:** verde señal sobre un fondo verde translúcido.
- **Próximamente:** gris claro sobre blanco translúcido, en el bloque oscuro.

### Inputs / Fields
- **Style:** fondo crema, borde de línea, 10px.
- **Focus:** anillo azul translúcido de 3px.

### Navigation
Barra pegajosa de 72px con crema translúcida y desenfoque; muestra la línea inferior solo al hacer scroll. Enlaces en tinta 2 que pasan a tinta en hover.

### Panel de eventos en vivo (Signature Component)
Un tablero oscuro con tres cifras (accesos, visitas activas, equipos en línea) y una lista de eventos con punto de estado, persona, puerta y hora. Siempre lleva la nota "Datos de ejemplo".

## Do's and Don'ts

### Do:
- **Do** marcar como "Datos de ejemplo" todo dato de demostración.
- **Do** usar los tonos de texto (brand-blue-deep, access-green-text, alert-red-text) para texto pequeño de color.
- **Do** atenuar con el gris medio (muted), nunca con `opacity`.
- **Do** respetar el área segura del iPhone (`env(safe-area-inset-*)`).

### Don't:
- **Don't** usar el verde o el rojo fuera de los estados de acceso.
- **Don't** hacer flotar más de una pieza por pantalla.
- **Don't** usar blanco puro como fondo de página.
- **Don't** mostrar capturas o cifras como si fueran de un cliente real.
