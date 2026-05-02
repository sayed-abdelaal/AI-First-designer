# Codex Prompt for New Presentations

Use this prompt when asking Codex to create a new presentation in the same style as this project.

---

Create this presentation using the exact same presentation system as my current project.

Working file:
- [index.html](</G:/Codex/AI-First designer/index.html>)

Design system reference:
- [design.md](</G:/Codex/AI-First designer/design.md>)

Important:
- The existing coded presentation system is the source of truth
- Do not redesign the system
- Do not invent a new visual language
- Follow the same layout logic, spacing rhythm, typography, colors, framing, motion style, and asset workflow

Use the exact same stack:
- plain HTML
- plain CSS
- vanilla JavaScript
- no React
- no Tailwind
- no Bootstrap
- no slide framework

Keep the architecture clean:
- HTML structure should stay readable
- CSS should remain systematic and reusable
- JavaScript should remain simple and presentation-focused

Presentation rules:
- every slide is a fixed `1920 x 1080` canvas
- aspect ratio is `16:9`
- do not build slides as responsive web sections
- use pixel-based positioning and sizing where exact matching matters
- preserve safe areas, component dimensions, and spacing values from the existing system
- preserve exact `cover` vs `contain` image behavior per slide/frame
- preserve the shared chrome:
  - top title
  - progress bar
  - bottom brand
  - slide count
  - centered nav

Asset rules:
- use local assets from [assets](</G:/Codex/AI-First designer/assets>)
- do not leave finished slides linked to temporary Figma asset URLs
- if you fetch from Figma, download locally first and then update the HTML path

Typography rules:
- use `Bebas Neue` for display/headlines
- use `Inter` for body/UI text
- preserve existing text size categories and spacing logic from `design.md`

Animation rules:
- use the same CSS keyframe approach
- use stagger classes like:
  - `.a1`
  - `.a2`
  - `.a3`
  - `.a4`
  - `.a5`
  - `.af`
- keep motion subtle and presentation-like

Implementation rules:
- reuse existing tokens whenever possible
- reuse existing components whenever possible
- do not scale content arbitrarily
- do not improve spacing unless explicitly instructed
- do not make stylistic assumptions outside the current system

When creating new slides:
- treat all existing slides as locked unless I explicitly say otherwise
- add only the slides I request
- match the Figma/design reference exactly
- keep dimensions, padding, margins, and alignment literal
- if a class already exists and should be reused, reuse it
- if a new slide needs slide-specific overrides, scope them to that slide only

Output expectations:
- update the real project files directly
- keep the implementation visually consistent with the existing presentation
- explain only the meaningful changes

If I provide a Figma link:
- implement the slide as closely as possible to the design
- do not reinterpret the composition
- keep the same system style and technical structure

Non-negotiable:
- no framework migration
- no Tailwind conversion
- no responsive redesign
- no ad-hoc scaling tricks
- no typography substitution unless absolutely necessary

---

Short version:

"Use the same stack and visual system as my current presentation project: plain HTML, plain CSS, vanilla JS, fixed 1920x1080 slides, Bebas Neue + Inter, shared presentation chrome, CSS keyframe stagger animations, pixel-precise layout, and local assets from the assets folder. Treat existing slides as locked unless I say otherwise. Follow design.md as the source of implementation rules."
