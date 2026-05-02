# AI-First Designer Presentation

This project is a fixed-canvas presentation system built in plain HTML, CSS, and JavaScript.

Main working file:
- [index.html](</G:/Codex/AI-First designer/index.html>)

## Files

### `index.html`

The actual presentation implementation.

Use this as:
- the visual source of truth
- the code source of truth
- the final rendered presentation

### `assets/`

Local presentation images used by the slides.

Use this as:
- the stable source for slide imagery
- the replacement for temporary Figma asset links

Important:
- do not rely on remote Figma MCP asset URLs for finished slides
- when an asset changes, re-download it locally and update the HTML path

Open:
- [assets](</G:/Codex/AI-First designer/assets>)

### `design.md`

The design system and implementation spec extracted from the coded presentation.

Use this when you want to:
- recreate the presentation in Figma
- understand the spacing, typography, colors, and components
- build new slides in the same style
- preserve exact visual consistency

Open:
- [design.md](</G:/Codex/AI-First designer/design.md>)

### `prompt.md`

A reusable prompt for Codex so new presentations or slides follow the same system.

Use this when you want to:
- ask Codex to create a new presentation in this style
- ask Codex to add new slides while keeping the system consistent
- avoid repeating the same technical and design instructions each time

Open:
- [prompt.md](</G:/Codex/AI-First designer/prompt.md>)

## Recommended Workflow

### If you want to build a new presentation in the same style

1. Start from `prompt.md`
2. Tell Codex what slides or Figma frames to build
3. Use `design.md` as the rulebook for exact spacing, typography, component reuse, and asset handling
4. Keep `index.html` as the live implementation target

### If you want to recreate the system in Figma

1. Read `design.md`
2. Rebuild the master frame at `1920 x 1080`
3. Recreate the shared chrome and reusable components first
4. Match all values literally from the implemented system

### If you want to refine existing slides

1. Treat existing slides as locked unless intentionally changing them
2. Update only the requested slide
3. Reuse existing classes first
4. Add slide-specific overrides only when necessary

## Project Rules

- The coded presentation is the source of truth
- Slides are fixed presentation canvases, not responsive page sections
- Preserve `1920 x 1080` unless the whole system intentionally changes
- Preserve pixel-based spacing and sizing where visual fidelity matters
- Keep presentation assets local
- Do not redesign the system unintentionally

## Quick Start

Use:
- [design.md](</G:/Codex/AI-First designer/design.md>) for system documentation
- [prompt.md](</G:/Codex/AI-First designer/prompt.md>) for Codex instructions
- [assets](</G:/Codex/AI-First designer/assets>) for local imagery
- [index.html](</G:/Codex/AI-First designer/index.html>) for implementation
