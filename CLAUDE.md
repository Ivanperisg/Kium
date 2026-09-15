# Kium — instrucciones del proyecto

Landing page de Kium, hosting de servidores Minecraft especializado en Cobblemon. Sitio de una sola página, HTML/CSS/JS estático, sin build step.

## Archivo canónico

**`index.html` es el único archivo real del sitio.** No crear alternativas paralelas (`kium-landing.html`, `landing.html`, etc.) para probar direcciones distintas — si se quiere explorar otra dirección visual, se hace sobre `index.html` a través del flujo de la skill `impeccable` (ver abajo), no con un archivo nuevo.

## Este repo se edita con dos herramientas a la vez

Además de Claude Code (`.claude/`), este proyecto se trabaja con Codex (`.codex/`, `.agents/`). Ambas comparten:
- La skill de diseño **impeccable** (`.claude/skills/impeccable` y `.agents/skills/impeccable` son el mismo sistema).
- El estado en `.impeccable/` (config, historial de decisiones de diseño, capturas de review). No asumas que el estado ahí lo escribiste tú en la sesión anterior — puede venir de una sesión de Codex.

Antes de cualquier trabajo de diseño/rediseño, correr `impeccable context` para cargar `PRODUCT.md`, `DESIGN.md` (si existe) y el brief de superficie correspondiente, en vez de asumir el estado del proyecto desde cero.

## Product truth vive en PRODUCT.md

`PRODUCT.md` tiene los hechos reales del producto (tiers de planes, precios placeholder, tono de copy, compromisos de marca). Léelo antes de escribir o cambiar copy. Reglas duras de ese archivo:
- Nombres de planes: **Poké Ball / Ultra Ball / Master Ball** — no cambiar esta convención sin pedirlo explícitamente.
- Copy en español, registro es-AR (informal, directo).
- **No inventar** cifras, testimonios o precios nuevos. Los que ya existen en `index.html` (uptime, testimonios, "Desde $X/mes") son placeholders declarados como tales — no convertirlos en hechos implícitos ni añadir más.

## Git

Remoto: `https://github.com/Ivanperisg/Kium.git`. Rama de trabajo actual: `claude/determined-wozniak-u8dce7`. No hacer commit ni push salvo que se pida explícitamente.

## Idioma

Responder siempre en español.
