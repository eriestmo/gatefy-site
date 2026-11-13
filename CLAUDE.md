# gatefy-site

Landing de Gatefy en gatefy.techadvisorsla.com: un solo `index.html` estático con su CSS y JS adentro, publicado con GitHub Pages desde `main`. El código del producto está en otro repo (`~/dev/gatefy`, privado y confidencial).

## No inventar

- La landing promete solo lo que el producto hace hoy. Antes de agregar o cambiar una función, se confirma en `~/dev/gatefy` (manuales en `docs/manuals/`, `CHANGELOG.md` y los ADR).
- Los manuales marcan cada función como **Disponible**, **Implementado pero sin conectar** o **Decidido, no implementado**. Solo "Disponible" se anuncia sin matices.
- No hay clientes, testimonios, cifras de uso ni precios publicados. No se inventan; el panel siempre dice "Datos de ejemplo".
- Nunca se publica contenido interno del repo del producto: nombres del equipo, ADR, infraestructura, llaves ni el README confidencial.

## Lo que sí es cierto hoy (revisado el 13 de noviembre de 2026)

- Equipos: solo Hikvision. La plataforma está preparada para otras marcas, pero no las soporta.
- Condominios: "Próximamente". Faltan los pases QR, la aprobación por el residente y el parqueo por unidad.
- ISO 27001: "prácticas" o "controles", nunca "certificado".
- Retención configurable y supresión por la Ley 8968: existen en la base de datos, pero todavía no tienen pantalla ni manual.

## Diseño

- `DESIGN.md` manda: colores, fuentes, formas y reglas.
- Las variables CSS llevan el nombre del color o la fuente en `DESIGN.md` (`--surface`, `--mint`, `--text-2`, `--font-display`…). Un color nuevo se agrega primero en `DESIGN.md`.
- Diseño nuevo: proponer 3 versiones distintas y que Eric elija una.
- Ediciones de una línea: se cambia lo pedido y nada más.
- Antes de publicar: axe-core sin fallas de contraste y revisión a 375px y en escritorio.

## Flujo de trabajo

- Rama → commit firmado → PR → Eric hace el merge.
- Vista previa local: configuración "gatefy-site" de `/Users/ericestrada/Claude Code/.claude/launch.json` (puerto 8767).
