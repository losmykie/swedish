# Design System

> My personal visual design system. Any AI building a site, UI, or interface for me should read this first. All my projects share this aesthetic unless I explicitly say otherwise.

---

## 1. Visual Theme & Atmosphere

Clean, modern, and light. Interfaces should feel effortless — like the UI is staying out of the way so the content can breathe. The aesthetic is rooted in functional minimalism: nothing decorative that isn't also useful, nothing heavy where something light will do.

White is always the base. The palette is built from four warm, vibrant accent colors — sky blue, soft yellow, orange, and coral red — used selectively against that white canvas. Typography does most of the visual hierarchy work. Spacing is generous. Borders are subtle or absent.

The overall impression should be: friendly, modern, and energetic without being loud. Clean like a SaaS product, but with warmth and personality from the accent palette.

**Key Characteristics:**
- Pure white background — always, on every project
- Four-color accent palette used intentionally, never all at once
- Typography-driven hierarchy — size and weight over decoration
- Generous whitespace — content is never cramped
- Subtle depth — shadows exist but never dominate
- Minimal borders — used for structure, not decoration
- Smooth, consistent border-radius throughout
- Interactive states are clear but understated

---

## 2. Color Palette & Roles

### Base (always white)
- **Pure White** (`#FFFFFF`): Page background — the foundation of every layout, no exceptions
- **Near-White** (`#F9FAFB`): Secondary surface, sidebar backgrounds, alternating rows, input fills
- **Light Gray** (`#F3F4F6`): Muted surface, disabled states

### Neutral Scale
- **Border Gray** (`#E5E7EB`): Dividers, card outlines, input borders
- **Muted Text** (`#9CA3AF`): Placeholders, helper text, secondary labels
- **Secondary Text** (`#6B7280`): Supporting text, captions, metadata
- **Primary Text** (`#111827`): Body copy, headings — near-black, not pure black

### Accent Palette
These four colors form the entire accent system. Use them against white — never as backgrounds for body text, never all four in one view. Pick the one that fits the context or the project's primary tone.

- **Sky Blue** (`#8CE4FF`): Primary accent — CTAs, active states, links, highlights, focus rings
- **Sky Blue Tint** (`#E8F9FF`): Background wash for sky blue — selected states, info badges, hero tints
- **Soft Yellow** (`#FEEE91`): Secondary accent — highlights, callouts, warm badges, hover fills
- **Soft Yellow Tint** (`#FFFDE8`): Background wash for yellow — subtle warnings, feature callouts
- **Orange** (`#FFA239`): Energetic accent — featured items, progress indicators, warm CTAs
- **Orange Tint** (`#FFF3E0`): Background wash for orange
- **Coral Red** (`#FF5656`): Alert accent — errors, destructive actions, urgent states
- **Coral Red Tint** (`#FFE8E8`): Background wash for coral red — error surfaces, danger zones

### Accent Usage Rules
- Each project picks **one primary accent** from the four; the others play supporting roles only
- Default primary: **Sky Blue** (`#8CE4FF`) — works for most professional/neutral contexts
- Tint versions (the washes) are the only acceptable colored backgrounds on white
- Never use a full accent color (`#8CE4FF`, `#FFA239`, etc.) as a text color on white — contrast is insufficient; darken or use `#111827` text on a tinted background instead

### Semantic Overrides
When semantic meaning requires it, these override the accent palette:
- **Success** (`#16A34A`): Positive confirmations — use sparingly
- **Error**: Use **Coral Red** (`#FF5656`) — it's already in the palette
- **Warning**: Use **Orange** (`#FFA239`) — it's already in the palette

---

## 3. Typography Rules

### Font Family
- **Primary**: `Inter`, fallbacks: `system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`
- **Monospace**: `"JetBrains Mono"`, fallbacks: `"Fira Code", "Cascadia Code", monospace`

If Inter is unavailable, the system-ui stack is acceptable — it reads as modern and native on all platforms.

### Hierarchy

| Role | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|--------|-------------|----------------|-------|
| Display | 48–60px | 700 | 1.1 | -0.02em | Hero/landing headings only |
| H1 | 36px | 700 | 1.2 | -0.01em | Page titles |
| H2 | 28px | 600 | 1.3 | -0.01em | Section headings |
| H3 | 22px | 600 | 1.4 | 0 | Subsection headings |
| H4 | 18px | 500 | 1.4 | 0 | Card titles, minor headings |
| Body | 16px | 400 | 1.6 | 0 | Default prose |
| Small | 14px | 400 | 1.5 | 0 | Captions, metadata, labels |
| Micro | 12px | 400 | 1.4 | 0.01em | Badges, tags, fine print |
| Code | 14px | 400 | 1.6 | 0 | Monospace — inline and block |

### Principles
- Weight discipline is strict: 400 for body, 500–600 for UI labels and subheadings, 700 for titles only. Never 700 on body copy.
- Negative letter-spacing on large headings prevents text from feeling too open at display sizes.
- Line height increases as font size decreases — body needs more breathing room than headings.
- Avoid decorative typefaces. Clarity over personality.

---

## 4. Component Stylings

### Buttons

**Primary Button**
- Background: `#8CE4FF` | Text: `#111827` | Padding: `10px 20px` | Radius: `8px`
- Border: none | Shadow: none
- Hover: background `#6EDAF7` (darken ~10%)
- Focus: `outline: 2px solid #8CE4FF; outline-offset: 2px`
- Use: primary action on any screen — one per view. Text is dark (`#111827`) because sky blue doesn't have sufficient contrast with white text.

**Secondary Button**
- Background: `#FFFFFF` | Text: `#111827` | Padding: `10px 20px` | Radius: `8px`
- Border: `1px solid #E5E7EB` | Shadow: none
- Hover: background `#F9FAFB`
- Focus: `outline: 2px solid #8CE4FF; outline-offset: 2px`
- Use: secondary or cancel actions

**Ghost Button**
- Background: transparent | Text: `#111827` | Padding: `10px 20px` | Radius: `8px`
- Border: none | Shadow: none
- Hover: background `#E8F9FF` (Sky Blue Tint)
- Use: tertiary actions, inline text-adjacent buttons

**Destructive Button**
- Background: `#FF5656` | Text: `#FFFFFF` — same geometry as Primary
- Hover: background `#E63E3E`
- Use: irreversible actions only; never the default CTA

### Cards & Containers

- Background: `#FFFFFF`
- Border: `1px solid #E5E7EB`
- Radius: `12px`
- Padding: `24px`
- Shadow: `0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04)`
- Hover (interactive cards): shadow `0 4px 12px rgba(0,0,0,0.08)`

### Inputs & Forms

- Background: `#FFFFFF`
- Border: `1px solid #E5E7EB`
- Radius: `8px`
- Padding: `10px 14px`
- Text: `#111827` | Placeholder: `#9CA3AF`
- Focus: border `#8CE4FF`, `box-shadow: 0 0 0 3px rgba(140,228,255,0.30)`
- Error: border `#FF5656`, `box-shadow: 0 0 0 3px rgba(255,86,86,0.20)`
- Labels: 14px, weight 500, `#374151`, 6px gap above input
- Helper text: 13px, `#6B7280`, 4px gap below input

### Navigation

- Background: `#FFFFFF` with `border-bottom: 1px solid #E5E7EB`
- Nav links: 14–15px, weight 500, `#374151`
- Active link: `#111827`, weight 600, with `border-bottom: 2px solid #8CE4FF` underline indicator
- Hover: `#111827`
- Logo/brand: H3-equivalent weight, `#111827`
- Sticky top nav with subtle backdrop-blur if scrolling over content

### Badges & Tags

- Background: `#F3F4F6` | Text: `#374151` | Padding: `2px 10px` | Radius: `999px` (pill)
- Sky Blue variant: background `#E8F9FF`, text `#111827`
- Yellow variant: background `#FFFDE8`, text `#111827`
- Orange variant: background `#FFF3E0`, text `#111827`
- Coral variant: background `#FFE8E8`, text `#111827`
- Font: 12px, weight 500

---

## 5. Layout Principles

### Spacing System
- **Base unit:** 4px
- **Scale:** 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96px
- Prefer multiples of 8 for component-level spacing; multiples of 4 for fine-grained internal padding

### Grid & Container
- Max content width: `1200px`, centered with `auto` margins
- Narrow content (prose, forms): `680px` max
- Page padding (horizontal): `24px` mobile, `48px` tablet, `64px` desktop
- Grid: 12-column with `24px` gutters

### Whitespace Philosophy
Let content breathe. When in doubt, add more space — not less. Dense UIs feel busy and are harder to scan. Section spacing should be visibly larger than component spacing. Group related elements tightly; separate unrelated elements generously.

### Border Radius Scale
- **2px**: Subtle, nearly-square (chips, small badges)
- **6px**: Form inputs, small buttons
- **8px**: Buttons, dropdowns, tooltips
- **12px**: Cards, modals, panels
- **16px+**: Large feature cards, image containers
- **999px**: Pills, avatar circles

---

## 6. Depth & Elevation

| Level | CSS Value | Use |
|-------|-----------|-----|
| Flat | none | Default surface — most elements |
| Lifted | `0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04)` | Cards, inputs |
| Raised | `0 4px 12px rgba(0,0,0,0.08), 0 2px 4px rgba(0,0,0,0.05)` | Hovered cards, sticky nav |
| Floating | `0 10px 24px rgba(0,0,0,0.10), 0 4px 8px rgba(0,0,0,0.06)` | Dropdowns, popovers |
| Modal | `0 20px 48px rgba(0,0,0,0.14), 0 8px 16px rgba(0,0,0,0.08)` | Modals, drawers |

Shadow philosophy: shadows should imply elevation, not drama. They're always soft, low-opacity, and multi-layered (two values: one for ambient, one for direct). Never use a single hard-edged shadow or pure black. The lighter surfaces should feel like they're floating above the page, not punching out of it.

---

## 7. Do's and Don'ts

### Do
- Use generous padding and margin — 24px internal card padding minimum
- Establish hierarchy with font size and weight before reaching for color
- Use the accent palette (Sky Blue, Yellow, Orange, Coral) for interactive and decorative highlights only
- Use `#111827` (near-black) instead of `#000000` for text
- Keep components aligned to the 4px grid
- Use border-radius consistently — pick the right scale tier and stick to it
- Ensure interactive states (hover, focus, active) are always defined
- Default to a single-column layout on mobile; max two columns on tablet

### Don't
- Use dark backgrounds unless the user has explicitly requested dark mode
- Use more than one accent color in a single view — it dilutes hierarchy
- Use `font-weight: 700` on body copy or paragraphs
- Apply drop shadows to elements that are not elevated above the surface
- Use borders and shadows together on the same card (pick one)
- Mix border-radius values arbitrarily — everything should belong to the scale
- Use full-saturated colors (`#FF0000`) — always use the semantic palette
- Center-align body text — left-align prose, center only for short hero copy

---

## 8. Responsive Behavior

### Breakpoints

| Name | Min Width | Strategy |
|------|-----------|----------|
| Mobile | 0px | Single column, full-width components |
| Tablet | 640px | 2-column grids, condensed nav |
| Desktop | 1024px | Full layout, sidebar patterns |
| Wide | 1280px | Max-width container kicks in |

### Touch Targets
- Minimum 44×44px for any tappable element on mobile
- Buttons and nav items must meet this without relying on padding tricks

### Collapsing Strategy
- Navigation: hamburger menu below 640px; horizontal nav above
- Cards: single column on mobile, 2-col at 640px, 3-col at 1024px
- Sidebars: collapse to drawer or bottom sheet on mobile
- Tables: horizontal scroll on mobile or convert to stacked card layout
- Hero text: reduce Display size to H1 equivalent on mobile

---

## 9. Quick Reference for AI Agents

When building any UI for me, start here:

### Core Tokens
| Purpose | Value |
|---------|-------|
| Page background | `#FFFFFF` — always |
| Secondary surface | `#F9FAFB` |
| Border | `#E5E7EB` |
| Primary text | `#111827` |
| Secondary text | `#6B7280` |
| Accent 1 — Sky Blue | `#8CE4FF` |
| Accent 1 Tint | `#E8F9FF` |
| Accent 2 — Yellow | `#FEEE91` |
| Accent 2 Tint | `#FFFDE8` |
| Accent 3 — Orange | `#FFA239` |
| Accent 3 Tint | `#FFF3E0` |
| Accent 4 — Coral Red | `#FF5656` |
| Accent 4 Tint | `#FFE8E8` |

### Accent Selection Guide
- **Sky Blue** (`#8CE4FF`): Default primary accent. Use for main CTAs, active nav, focus rings, hero accents.
- **Yellow** (`#FEEE91`): Warmth and highlights. Use for callouts, featured badges, hover fills on secondary elements.
- **Orange** (`#FFA239`): Energy and progress. Use for progress bars, featured/highlighted cards, warm CTAs.
- **Coral Red** (`#FF5656`): Urgency and errors. Use for destructive buttons, error states, alert badges.

One project = one primary accent. The others appear only in semantic or supporting roles.

### Example Prompts (adapt these)
- "Build a settings page with a sidebar nav. Use Near-White (`#F9FAFB`) for the sidebar, White for the main content area, card radius 12px, Primary Button (Sky Blue `#8CE4FF`) for save."
- "Design a pricing table with three plan cards. Cards use Lifted shadow, Sky Blue CTA button on the recommended plan, Orange pill badge labeled 'Most Popular'."
- "Create a login form: centered on white background, card with 12px radius and Lifted shadow, inputs with 8px radius, Sky Blue Primary Button for submit, Coral Red error states."
- "Build a dashboard with stat cards. Each card gets a subtle tint background from one of the four accent colors to visually group them."

### Iteration Checklist
Before considering a UI complete:
1. Is the background white (`#FFFFFF`)? No exceptions unless explicitly overridden.
2. Are all colors from this palette? No ad-hoc hex values.
3. Is there at most one primary accent color driving the main interactive elements?
4. Is the type hierarchy clear with size and weight alone?
5. Does every interactive element have hover AND focus states defined?
6. Is spacing consistent with the 4px grid?
7. Does it look correct at mobile width (single column, 44px tap targets)?
8. Is there only one Primary Button per view?
9. Does the page feel light and uncluttered — would removing anything make it cleaner?
