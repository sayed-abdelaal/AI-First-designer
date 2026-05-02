# Presentation Design System

Source of truth: [index.html](G:/Codex/AI-First designer/index.html)

This file documents the implemented presentation system so new presentations can follow the exact same style, proportions, and behavior.

## Purpose

Use this system when creating a new presentation that should feel identical in structure, spacing, tone, and motion to the current project.

This is a fixed-slide presentation system, not a responsive web page system.

## Core Stack

- Single-presentation front end
- Plain HTML
- Plain CSS
- Vanilla JavaScript
- Google Fonts:
  - `Bebas Neue` for display/headlines
  - `Inter` for body/UI text
- CSS keyframe animations
- No React
- No Tailwind
- No Bootstrap
- No slide framework

## Master Canvas

- Slide size: `1920px × 1080px`
- Aspect ratio: `16:9`
- Every slide must be treated as a fixed artboard
- Do not redesign layouts as responsive sections
- Do not use fluid typography for slide content

## Global Tokens

Defined in `:root`:

```css
--bg: #10111a;
--white: #ffffff;
--white-10: rgba(255, 255, 255, 0.1);
--white-12: rgba(255, 255, 255, 0.12);
--white-25: rgba(255, 255, 255, 0.25);
--white-03: rgba(255, 255, 255, 0.03);
--text-secondary: #9899af;
--text-muted: #6b6c82;
--accent: #cc004c;
--primary: #5955f4;
--nav-glass: rgba(16, 17, 26, 0.72);
--shadow: 0 4px 24px rgba(0, 0, 0, 0.3);
--deck-width: 1920px;
--deck-height: 1080px;
--safe-x: 60px;
--safe-top: 32px;
--safe-bottom: 60px;
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
--dur-fast: 220ms;
--dur-slow: 680ms;
--font-display: "Bebas Neue", "Arial Narrow", sans-serif;
--font-body: "Inter", system-ui, sans-serif;
```

## Layout Rules

### Safe Areas

- Left safe inset: `60px`
- Right safe inset: `60px`
- Top safe inset: `32px`
- Bottom safe inset: `60px`

### Common Anchors

- Many primary text blocks start at `left: 120px`
- Common text widths:
  - `540px`
  - `724px`
  - `780px`
  - `1020px`
- Large framed screen width: `1680px`

### Grid Language

Dark grid:
- `68px × 68px` grid cells
- `1px` lines
- line color from `--white-03`

Light grid:
- `68px × 68px` grid cells
- `1px` lines
- line tint: `rgba(89, 85, 244, 0.055)`

### Common Spacing Values

Repeated spacing values used in the system:

- `0`
- `5`
- `6`
- `7`
- `10`
- `14`
- `16`
- `18`
- `20`
- `24`
- `27`
- `30`
- `32`
- `36`
- `40`
- `44`
- `60`
- `74`
- `80`
- `104`
- `110`
- `120`

Do not invent a new spacing scale unless the new presentation requires it. Prefer these existing values first.

## Typography

### Font Roles

- Display font: `Bebas Neue`
- Body/UI font: `Inter`

### Implemented Text Sizes

- `11px`
- `14px`
- `16px`
- `18px`
- `20px`
- `22px`
- `28px`
- `36px`
- `40px`
- `48px`
- `56px`
- `64px`
- `80px`
- `96px`
- `128px`

### Core Text Styles

Hero XL:
- `font-family: var(--font-display)`
- `font-size: 128px`
- `font-weight: 400`
- `line-height: 0.95`
- `letter-spacing: -1.28px`
- `text-transform: uppercase`

Hero L:
- `font-family: var(--font-display)`
- `font-size: 96px`
- `font-weight: 400`
- `line-height: 0.95`
- `letter-spacing: -0.96px`
- `text-transform: uppercase`

Section Title:
- `font-family: var(--font-display)`
- `font-size: 80px`
- `font-weight: 400`
- `line-height: 0.95`
- `letter-spacing: -0.8px`
- `text-transform: uppercase`

Card / Small Headline:
- `font-family: var(--font-display)`
- `font-size: 28px`
- `font-weight: 400`
- `line-height: 1.1`
- `letter-spacing: 0.28px`
- `text-transform: uppercase`

Step Title:
- `font-family: var(--font-display)`
- `font-size: 36px`
- `font-weight: 400`
- `line-height: 1.1`
- `letter-spacing: 0.36px`
- `text-transform: uppercase`

Quote Mark:
- `font-family: var(--font-display)`
- `font-size: 56px`
- `font-weight: 400`
- `line-height: 0.3`
- `letter-spacing: 0.56px`

Body Regular:
- `font-size: 16px`
- `font-weight: 400`
- `line-height: 1.5`

Body Medium:
- `font-size: 18px`
- `font-weight: 500`
- `line-height: 1.65`

Overline / Label:
- `font-size: 14px`
- `font-weight: 500`
- `line-height: 1.65`
- `letter-spacing: 1.12px`
- `text-transform: uppercase`

Meta Small:
- `font-size: 11px`
- `font-weight: 500`
- `line-height: 1.65`
- `letter-spacing: 0.44px`
- `text-transform: uppercase`

UI Meta:
- `font-size: 16px`
- `line-height: 1.5`

## Color System

Primary colors:

- Background: `#10111a`
- White: `#ffffff`
- Accent: `#cc004c`
- Primary blue/violet: `#5955f4`
- Secondary text: `#9899af`
- Muted text: `#6b6c82`

Supporting literals used in the implementation:

- `#161724`
- `#32334a`
- `#3c3d54`
- `#d7e1eb`
- `#dbe3eb`
- `#eeeeff`
- `#f5dada`
- `#659bd11c`
- `#659bd142`

## Shared Components

### Presentation Chrome

Top meta row:
- `x: 60px`
- `y: 32px`
- width: `1800px`

Bottom meta row:
- `x: 60px`
- bottom: `60px`
- width: `1800px`

Progress bar:
- top pinned
- height: `3px`
- fill color: `--accent`

Bottom cover line:
- width: `1280px`
- height: `3px`
- accent-to-transparent gradient

### Nav

Container:
- bottom: `74px`
- centered horizontally
- `gap: 6px`
- `padding: 7px`
- `border-radius: 999px`
- `border: 1px solid var(--white-10)`
- `background: var(--nav-glass)`
- `box-shadow: var(--shadow)`
- `backdrop-filter: blur(8px)`

Buttons:
- `32px × 32px`
- `border-radius: 16px`
- icon `16px × 16px`

Dots:
- default: `5px × 5px`
- active: `20px × 5px`
- gap: `5px`

### Brand Row

- icon: `24px × 24px`
- text gap: `10px`
- label font size: `20px`

### Overline

- row gap: `10px`
- line: `120px × 3px`
- text style: `14px`, medium, uppercase

### Info Card

- `border: 1px solid #eeeeff`
- `border-radius: 16px`
- `padding: 16px 14px`
- half width: `254px`
- full width: `100%`

### Side Card

- top border: `4px solid var(--accent)`
- `padding: 16px`
- vertical gap: `6px`
- title size: `28px`
- body/list size: `16px`
- list padding-left: `24px`

### Speaker Row

- row gap: `16px`
- avatar: `48px × 61px`
- avatar fit: `object-fit: contain`
- divider: `1px × 40px`
- stacks: `white-space: nowrap`

### Demo Frame

Base:
- `left: 120px`
- `top: 331px`
- width: `1680px`
- `border-radius: 32px`
- `overflow: hidden`

GAIA variant:
- height: `917px`
- border: `10px solid rgba(187, 213, 234, 0.1)`

Smart variant:
- height: `945px`
- border: `10px solid rgba(187, 213, 234, 0.3)`

### Workflow Frame

- `left: 120px`
- `top: 331px`
- width: `1680px`
- height: `1183px`
- border: `10px solid rgba(234, 214, 187, 0.4)`
- radius: `32px`

## Animation System

This project uses simple CSS-only staged reveal animations.

Classes:

- `.a1`
- `.a2`
- `.a3`
- `.a4`
- `.a5`
- `.af`

Behavior:

- default state: `opacity: 0`
- active slide triggers staggered animation

Timings:

- `.a1`: `60ms`
- `.a2`: `170ms`
- `.a3`: `290ms`
- `.a4`: `420ms`
- `.a5`: `540ms`
- `.af`: `120ms` fade-in

Keyframes:

`fade-up`
- from `opacity: 0; transform: translateY(22px)`
- to `opacity: 1; transform: translateY(0)`

`fade-in`
- from `opacity: 0`
- to `opacity: 1`

Core motion tokens:

- `--dur-fast: 220ms`
- `--dur-slow: 680ms`
- `--ease-out: cubic-bezier(0.16, 1, 0.3, 1)`

## JavaScript Behavior

Presentation behavior is implemented in vanilla JS.

Included:

- slide list from `.slide`
- previous/next buttons
- keyboard navigation
- clickable nav dots
- page title sync from `data-title`
- slide counter sync
- progress bar sync
- deck scaling to viewport

Important behavior:

```js
const scale = Math.max(vw / 1920, vh / 1080);
```

This means the deck uses cover-style scaling, not contain-style scaling.

## Rules for New Presentations in This Style

- Keep the master frame at `1920 × 1080`
- Keep slide content pixel-based
- Reuse the same safe insets: `60 / 32 / 60`
- Reuse the same display/body fonts
- Reuse the same nav, chrome, overlines, and card patterns
- Reuse the same grid look
- Reuse the same animation classes and timing language
- Prefer the existing spacing values before adding new ones
- Use absolute positioning for slide composition when matching this style
- Treat every slide like a designed canvas, not a fluid section layout

## Figma Recreation Notes

If recreating this in Figma:

- frame size must be `1920 × 1080`
- use pixel values only
- create reusable components for:
  - nav
  - brand/footer
  - progress/top and bottom lines
  - overline
  - side cards
  - info cards
  - speaker row
  - framed image/screen containers
- do not allow text or children to auto-scale when frames resize
- preserve exact image fit behavior:
  - some use `cover`
  - some use `contain`

## Non-Negotiable Match Rules

- Do not change the slide frame size
- Do not replace pixel values with relative sizing
- Do not substitute a different visual rhythm or spacing scale
- Do not swap fonts unless explicitly intended
- Do not rebuild slides as responsive layouts
- Do not center by eye; use exact coordinates or exact frame centering
- Do not change `cover`/`contain` behavior without checking the source slide
- Do not introduce Tailwind or framework abstractions into this presentation system unless the project intentionally changes architecture

