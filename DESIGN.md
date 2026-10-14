---
version: alpha
name: Raster
description: A soft, neutral design system. White cards on light gray, pill controls and one blue.
colors:
  primary: "#007AFF"
  primary-hover: "#006AE0"
  primary-foreground: "#FFFFFF"
  background: "#F4F4F4"
  foreground: "#0A0A0A"
  card: "#FFFFFF"
  card-foreground: "#0A0A0A"
  popover: "#FFFFFF"
  popover-foreground: "#0A0A0A"
  secondary: "#EEEEEE"
  secondary-foreground: "#0A0A0A"
  muted: "#EEEEEE"
  muted-foreground: "#666666"
  accent: "#EEEEEE"
  accent-foreground: "#0A0A0A"
  destructive: "#FF3B30"
  destructive-foreground: "#FFFFFF"
  success: "#34C759"
  warning: "#FF9500"
  border: "#EBEBEB"
  input: "#D1D1D1"
  ring: "#007AFF"
typography:
  display:
    fontFamily: Inter
    fontSize: 48px
    fontWeight: 700
    lineHeight: 52px
    letterSpacing: -0.03em
  h1:
    fontFamily: Inter
    fontSize: 36px
    fontWeight: 700
    lineHeight: 40px
    letterSpacing: -0.025em
  h2:
    fontFamily: Inter
    fontSize: 28px
    fontWeight: 700
    lineHeight: 32px
    letterSpacing: -0.02em
  h3:
    fontFamily: Inter
    fontSize: 22px
    fontWeight: 600
    lineHeight: 28px
    letterSpacing: -0.015em
  title:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: 600
    lineHeight: 24px
    letterSpacing: -0.01em
  body:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 400
    lineHeight: 24px
  button:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: 500
    lineHeight: 24px
  small:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 400
    lineHeight: 20px
  ui:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: 500
    lineHeight: 20px
  caption:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: 500
    lineHeight: 16px
rounded:
  lg: 24px
  2xl: 32px
  full: 9999px
spacing:
  "1": 4px
  "2": 8px
  "3": 12px
  "4": 16px
  "5": 20px
  "6": 24px
  "7": 28px
  "8": 32px
  "12": 48px
  "16": 64px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.primary-foreground}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    height: 48px
    padding: 0 28px
  button-primary-hover:
    backgroundColor: "{colors.primary-hover}"
  button-secondary:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.secondary-foreground}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    height: 48px
    padding: 0 28px
  button-ghost:
    textColor: "{colors.foreground}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    height: 48px
    padding: 0 28px
  button-ghost-hover:
    backgroundColor: "{colors.accent}"
  button-destructive:
    backgroundColor: "{colors.destructive}"
    textColor: "{colors.destructive-foreground}"
    typography: "{typography.button}"
    rounded: "{rounded.full}"
    height: 48px
    padding: 0 28px
  button-small:
    typography: "{typography.ui}"
    rounded: "{rounded.full}"
    height: 36px
    padding: 0 16px
  icon-button:
    textColor: "{colors.muted-foreground}"
    rounded: "{rounded.full}"
    size: 32px
  icon-button-hover:
    backgroundColor: "{colors.accent}"
    textColor: "{colors.foreground}"
  icon-button-filled:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.foreground}"
    rounded: "{rounded.full}"
    size: 40px
  chip:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.muted-foreground}"
    typography: "{typography.ui}"
    rounded: "{rounded.full}"
    height: 32px
    padding: 0 14px
  chip-selected:
    backgroundColor: "{colors.card}"
    textColor: "{colors.foreground}"
  toggle:
    backgroundColor: "{colors.input}"
    rounded: "{rounded.full}"
    width: 70px
    height: 30px
  toggle-checked:
    backgroundColor: "{colors.primary}"
  checkbox:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.full}"
    size: 22px
  checkbox-checked:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.primary-foreground}"
  segmented-control:
    backgroundColor: "{colors.secondary}"
    rounded: "{rounded.full}"
    padding: 4px
  segment-selected:
    backgroundColor: "{colors.card}"
    textColor: "{colors.foreground}"
  badge:
    backgroundColor: "{colors.secondary}"
    textColor: "{colors.foreground}"
    typography: "{typography.caption}"
    rounded: "{rounded.full}"
    height: 28px
  progress:
    backgroundColor: "{colors.secondary}"
    rounded: "{rounded.full}"
    height: 6px
  text-field:
    backgroundColor: "{colors.card}"
    textColor: "{colors.foreground}"
    typography: "{typography.body}"
    rounded: "{rounded.full}"
    height: 48px
    padding: 0 20px
  card:
    backgroundColor: "{colors.card}"
    textColor: "{colors.card-foreground}"
    rounded: "{rounded.2xl}"
    padding: 24px
---

# Raster

## Overview

Raster is a soft, neutral system for product interfaces. Content sits on white cards with a 32px radius, the cards sit on a light gray page, every control is a pill, and one blue marks what is on, selected or primary. Nothing else has color unless it reports a status.

The visual language was measured from a public screenshot of a component gallery (colors sampled from the pixels, sizes from the layout). Button, Toggle, Slider and Single Selection follow that screenshot closely. Everything else in this file extends the same language.

The same tokens exist in three places and must stay in sync:

- `raster.css` for Tailwind CSS v4. Token names follow shadcn/ui.
- This file, for people and coding agents.
- The Figma library "Raster Design System" (variables, text styles, components).

When building with Raster, use the semantic tokens and the recipes under Components. If a screen needs something this file does not cover, build it from the same parts: a pill or a 32px card, a gray or white surface, 14px medium interface text, and at most one blue element competing for attention.

## Colors

Use semantic tokens only. The default Tailwind palette is removed in `raster.css`, so `bg-blue-500` and similar classes produce nothing.

| Token | Light | Dark | Use |
| --- | --- | --- | --- |
| `background` | `#F4F4F4` | `#000000` | Page background |
| `foreground` | `#0A0A0A` | `#FAFAFA` | Text and icons |
| `card` | `#FFFFFF` | `#1A1A1A` | Cards, header bar, selected chip, form controls |
| `popover` | `#FFFFFF` | `#1A1A1A` | Menus, popovers, dialogs |
| `primary` | `#007AFF` | `#0A84FF` | Primary button and the on state of toggle, slider, radio |
| `primary-hover` | `#006AE0` | `#3D9BFF` | Hover fill for primary |
| `primary-foreground` | `#FFFFFF` | `#FFFFFF` | Text on primary |
| `secondary` | `#EEEEEE` | `#2A2A2A` | Unselected chips, secondary buttons, tracks |
| `muted` | `#EEEEEE` | `#2A2A2A` | Subtle surface behind grouped content |
| `muted-foreground` | `#666666` | `#A1A1A1` | Secondary text and resting icons |
| `accent` | `#EEEEEE` | `#2A2A2A` | Hover surface for ghost and icon buttons |
| `destructive` | `#FF3B30` | `#FF453A` | Errors and destructive actions |
| `success` | `#34C759` | `#30D158` | Success indicator |
| `warning` | `#FF9500` | `#FF9F0A` | Warning indicator |
| `border` | `#EBEBEB` | `#2A2A2A` | Card outlines, dividers, ring of the selected chip |
| `input` | `#D1D1D1` | `#4A4A4A` | Outline of form controls, off track of a toggle |
| `ring` | `#007AFF` | `#0A84FF` | Focus ring |

`card-foreground`, `popover-foreground`, `secondary-foreground` and `accent-foreground` equal `foreground`. `destructive-foreground` is white. Dark mode is the `.dark` class on a parent element.

Rules:

- One blue. `primary` is for the single main action of a view and for on or selected states. Do not use it for decoration, headings or large surfaces.
- `accent` is the hover surface, as in shadcn/ui. It is not a brand accent.
- `destructive`, `success` and `warning` are fills, dots and icons. For status text, write the status in `foreground` next to a colored dot or icon.
- `muted-foreground` passes WCAG AA on `card`, `background` and `secondary` in both modes.

Three values are kept faithful to the reference or to the iOS palette it uses, and fall short of WCAG AA in both modes. Change them if the product needs strict conformance:

- White text on `primary` is 4.0:1 on `#007AFF`, 3.6:1 on the dark mode's `#0A84FF` and 2.9:1 on its hover `#3D9BFF` (AA asks 4.5:1 for 16px text). `#0066E0` gives 5.3:1 in both modes with nearly the same look, with a hover that stays at 4.5:1 or more, such as `#0058C2`.
- White text on `destructive` is 3.6:1 on `#FF3B30` and 3.4:1 on the dark mode's `#FF453A`. `#D70015` gives 5.4:1 and still reads as the system red. The red outline of a field with an error is 3.6:1 on white and 5.1:1 on the dark card, which passes the 3:1 asked of control boundaries.
- The `input` outline is 1.5:1 for `#D1D1D1` on white and 2.0:1 for `#4A4A4A` on the dark `card` `#1A1A1A` (AA asks 3:1 for control boundaries). `#949494` reaches 3:1 on white, `#666666` on the dark card.

## Typography

Inter, loaded by the app (`next/font`, `@fontsource-variable/inter` or a link tag). Weights 400, 500, 600 and 700.

| Utility | Size / line | Weight | Tracking | Use |
| --- | --- | --- | --- | --- |
| `type-display` | 48 / 52 | 700 | -0.03em | One per page at most |
| `type-h1` | 36 / 40 | 700 | -0.025em | Page title |
| `type-h2` | 28 / 32 | 700 | -0.02em | Section title |
| `type-h3` | 22 / 28 | 600 | -0.015em | Subsection |
| `type-title` | 18 / 24 | 600 | -0.01em | Dialog and card titles |
| `type-body` | 16 / 24 | 400 | 0 | Body text, text inputs |
| `type-ui` | 14 / 20 | 500 | 0 | Chips, card titles, list rows, field labels |
| `type-small` | 14 / 20 | 400 | 0 | Option labels, hints, secondary text |
| `type-caption` | 12 / 16 | 500 | 0 | Badges and metadata |

Buttons use `text-base font-medium` (16 / 24, weight 500).

Rules:

- Use the `type-*` utilities instead of composing size, weight and tracking by hand. They are not named `text-*` so that `tailwind-merge` does not confuse them with text colors.
- Interface text is `type-ui`. Reach for 16px only for buttons, body copy and text the user types.
- Sentence case everywhere. No all caps except a wordmark.
- Text inputs stay at 16px so mobile browsers do not zoom on focus.

## Layout

- Spacing uses the Tailwind 4px unit. Common steps: 8 (inside a control), 16 (between cards, page margin, between stacked options), 24 to 28 (card padding).
- The page is `bg-background`. Content lives in cards; do not place loose content directly on the gray except the page title.
- Cards form a grid with `gap-4` and `p-4` page margins: one column on phones, two from 480px, three from 1024px, four from 1280px. Gallery cards keep a 9:10 ratio (`aspect-[9/10]`).
- A sticky or top header is a `bg-card` bar with a bottom border. Keep it to the wordmark and a few actions.
- Group a long page of cards under section titles: an `h2` in `type-title`, 32px above it and 16px below (`pt-8 pb-4`), aligned with the card edge.
- Inside a gallery card, the content is centered and the footer holds the title on the left and quiet icon buttons on the right. The title starts at the same 24px edge as the content.
- A product screen puts its sections in cards of 24 to 28px padding, with the page title on the gray above them and the section list in a card of its own.

## Elevation & Depth

The system is flat. Depth comes from the step between the gray page and the white card, plus a 1px `border`.

- Cards and the header have a border and no shadow.
- `shadow-sm` is for small parts that sit on a track: the toggle thumb, the slider thumb, the selected segment.
- `shadow-lg` is for surfaces that float above the page: menus, popovers and dialogs. Pair it with the border.
- The selected chip uses a 2px ring in `border` color, not a shadow.

## Shapes

Everything is round.

- Controls are pills: `rounded-full` for buttons, chips, text fields, toggles, badges and tracks. Radios and checkboxes are circles.
- Cards are `rounded-2xl` (32px).
- Menus, popovers, dialogs and panels inside a card are `rounded-lg` (24px).
- No square corners and no small radii such as 4px or 8px.

`--radius` is `1.5rem`, so shadcn/ui components that use `rounded-md` or `rounded-lg` come out pill-like without changes.

Icons are Lucide with its default round caps and joins, at 16px (`size-4`) in `currentColor`. Use 20px only when an icon stands alone in a header. Icon-only buttons need an `aria-label`.

## Components

Copy these recipes. The live versions are in `preview/index.html`, and each card's Copy button copies the same markup as the block here. `preview/demo.html` is an example screen, a settings page for an invented notes app, built only from these recipes.

### Button

48px pill. One primary button per view; a second action is secondary, a third is ghost.

```html
<div class="flex flex-col items-center gap-3">
  <button type="button" class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-primary text-primary-foreground hover:bg-primary-hover">Save</button>
  <button type="button" class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-secondary text-secondary-foreground hover:bg-input/60">Cancel</button>
  <button type="button" class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 text-foreground hover:bg-accent">Skip</button>
</div>
```

- Primary: `bg-primary text-primary-foreground hover:bg-primary-hover`.
- Secondary: `bg-secondary text-secondary-foreground hover:bg-input/60`.
- Ghost: `text-foreground hover:bg-accent`.
- With an icon, put a 16px Lucide icon after the label; `gap-2` spaces it.

### Button sizes

Large is 48px with `px-7 text-base font-medium`. Small is 36px with `h-9 px-4 type-ui`, for buttons inside cards, rows and toolbars.

```html
<div class="flex flex-col items-center gap-4">
  <button type="button" class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-primary text-primary-foreground hover:bg-primary-hover">Continue</button>
  <button type="button" class="inline-flex h-9 items-center justify-center gap-2 rounded-full px-4 type-ui transition-colors disabled:pointer-events-none disabled:opacity-40 bg-primary text-primary-foreground hover:bg-primary-hover">Continue</button>
</div>
```

### Destructive and disabled

Destructive is the red fill, for an action that deletes or cannot be undone. Use it once, at the end of the flow it belongs to, never as the main action of a page. Disabled buttons keep their variant at 40% opacity and ignore the pointer.

```html
<div class="flex flex-col items-center gap-3">
  <button type="button" class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-destructive text-destructive-foreground hover:bg-destructive/85">Delete</button>
  <button type="button" disabled class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-primary text-primary-foreground hover:bg-primary-hover">Save</button>
  <button type="button" disabled class="inline-flex h-12 items-center justify-center gap-2 rounded-full px-7 text-base font-medium transition-colors disabled:pointer-events-none disabled:opacity-40 bg-secondary text-secondary-foreground hover:bg-input/60">Cancel</button>
</div>
```

White on `destructive` is 3.6:1 in light mode and 3.4:1 in dark mode; see Colors for the AA-safe value.

### Icon button

32px round hit area around a 16px icon, for quiet actions in footers and toolbars. The filled 40px variant sits on a white card where the icon has to read as a button on its own.

```html
<div class="flex flex-col items-center gap-5">
  <div class="flex gap-1">
    <button type="button" aria-label="Search" class="inline-flex size-8 items-center justify-center rounded-full text-muted-foreground transition-colors hover:bg-accent hover:text-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg></button>
    <button type="button" aria-label="Add" class="inline-flex size-8 items-center justify-center rounded-full text-muted-foreground transition-colors hover:bg-accent hover:text-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M5 12h14"/><path d="M12 5v14"/></svg></button>
    <button type="button" aria-label="More" class="inline-flex size-8 items-center justify-center rounded-full text-muted-foreground transition-colors hover:bg-accent hover:text-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="1"/><circle cx="19" cy="12" r="1"/><circle cx="5" cy="12" r="1"/></svg></button>
  </div>
  <div class="flex gap-2">
    <button type="button" aria-label="Search" class="inline-flex size-10 items-center justify-center rounded-full bg-secondary text-foreground transition-colors hover:bg-input/60"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg></button>
    <button type="button" aria-label="Add" class="inline-flex size-10 items-center justify-center rounded-full bg-secondary text-foreground transition-colors hover:bg-input/60"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="M5 12h14"/><path d="M12 5v14"/></svg></button>
    <button type="button" aria-label="More" class="inline-flex size-10 items-center justify-center rounded-full bg-secondary text-foreground transition-colors hover:bg-input/60"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="1"/><circle cx="19" cy="12" r="1"/><circle cx="5" cy="12" r="1"/></svg></button>
  </div>
</div>
```

Every icon button needs an `aria-label`.

### Chip

Filter pill. Exactly one chip in a group has `aria-pressed="true"`.

```html
<div role="group" aria-label="Filter" class="flex flex-wrap justify-center gap-2.5">
  <button type="button" aria-pressed="true" class="h-8 shrink-0 rounded-full bg-secondary px-3.5 type-ui text-muted-foreground transition-colors hover:text-foreground aria-pressed:bg-card aria-pressed:text-foreground aria-pressed:ring-2 aria-pressed:ring-border">All</button>
  <button type="button" aria-pressed="false" class="h-8 shrink-0 rounded-full bg-secondary px-3.5 type-ui text-muted-foreground transition-colors hover:text-foreground aria-pressed:bg-card aria-pressed:text-foreground aria-pressed:ring-2 aria-pressed:ring-border">Active</button>
  <button type="button" aria-pressed="false" class="h-8 shrink-0 rounded-full bg-secondary px-3.5 type-ui text-muted-foreground transition-colors hover:text-foreground aria-pressed:bg-card aria-pressed:text-foreground aria-pressed:ring-2 aria-pressed:ring-border">Pending</button>
</div>
```

### Toggle

70 by 30px switch for a setting that applies at once. Flip `aria-checked` on click.

```html
<div class="flex flex-col items-center gap-5">
  <button type="button" role="switch" aria-checked="true" aria-label="Option A" class="group relative h-7.5 w-17.5 shrink-0 rounded-full bg-input transition-colors aria-checked:bg-primary disabled:opacity-40"><span class="absolute top-1 left-1 h-5.5 w-9 rounded-full bg-white shadow-sm transition-transform group-aria-checked:translate-x-6.5"></span></button>
  <button type="button" role="switch" aria-checked="false" aria-label="Option B" class="group relative h-7.5 w-17.5 shrink-0 rounded-full bg-input transition-colors aria-checked:bg-primary disabled:opacity-40"><span class="absolute top-1 left-1 h-5.5 w-9 rounded-full bg-white shadow-sm transition-transform group-aria-checked:translate-x-6.5"></span></button>
  <button type="button" role="switch" aria-checked="true" aria-label="Option C" disabled class="group relative h-7.5 w-17.5 shrink-0 rounded-full bg-input transition-colors aria-checked:bg-primary disabled:opacity-40"><span class="absolute top-1 left-1 h-5.5 w-9 rounded-full bg-white shadow-sm transition-transform group-aria-checked:translate-x-6.5"></span></button>
</div>
```

### Slider

A native range input with the `raster-slider` utility from `raster.css`. Chrome and Safari need `--slider-fill` to paint the filled part, so update it on every `input` event.

```html
<div class="w-full space-y-10">
  <input type="range" min="0" max="100" value="50" aria-label="Volume" class="raster-slider" />
  <input type="range" min="0" max="100" value="30" aria-label="Brightness" disabled class="raster-slider" />
</div>
```

```js
el.style.setProperty('--slider-fill', `${((el.value - el.min) / (el.max - el.min)) * 100}%`);
```

### Single selection

Native radios in a `fieldset` with a `legend`. The checked state is a 7px blue border around a white center. Stack options with `space-y-4`.

```html
<fieldset class="space-y-4">
  <legend class="sr-only">Options</legend>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="radio" name="option" checked class="size-5.5 appearance-none rounded-full border-[1.5px] border-input bg-card transition-[border-width,border-color] checked:border-7 checked:border-primary checked:bg-white disabled:opacity-40" />Option A</label>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="radio" name="option" class="size-5.5 appearance-none rounded-full border-[1.5px] border-input bg-card transition-[border-width,border-color] checked:border-7 checked:border-primary checked:bg-white disabled:opacity-40" />Option B</label>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="radio" name="option" disabled class="size-5.5 appearance-none rounded-full border-[1.5px] border-input bg-card transition-[border-width,border-color] checked:border-7 checked:border-primary checked:bg-white disabled:opacity-40" />Option C</label>
</fieldset>
```

### Checkbox

Native checkboxes with the `raster-checkbox` utility from `raster.css`. Like the radio it is a 22px circle; checked is a blue disc with a white check, so the two never look alike. Use it when several options can be on together.

```html
<fieldset class="space-y-4">
  <legend class="sr-only">Options</legend>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="checkbox" checked class="raster-checkbox" />Option A</label>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="checkbox" class="raster-checkbox" />Option B</label>
  <label class="flex items-center gap-2 type-small has-disabled:text-muted-foreground"><input type="checkbox" checked disabled class="raster-checkbox" />Option C</label>
</fieldset>
```

### Text field

48px pill with a visible label above. Text stays at 16px.

```html
<label class="block w-full"><span class="type-ui">Email</span><input type="email" placeholder="name@example.com" class="mt-2 h-12 w-full rounded-full border bg-card px-5 text-base placeholder:text-muted-foreground disabled:opacity-40 border-input" /></label>
```

### Text field states

For an error, add `aria-invalid="true"`, swap `border-input` for `border-destructive`, and put a message below that says how to fix the value: a red `circle-alert` icon and `type-small` text in `foreground`, linked with `aria-describedby`. A disabled field fades to 40%.

```html
<div class="w-full space-y-5">
  <label class="block w-full"><span class="type-ui">Email</span><input type="email" value="name.example.com" aria-invalid="true" aria-describedby="email-error" class="mt-2 h-12 w-full rounded-full border bg-card px-5 text-base placeholder:text-muted-foreground disabled:opacity-40 border-destructive" /><span id="email-error" class="mt-2 flex items-center gap-1.5 type-small"><span class="text-destructive"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><circle cx="12" cy="12" r="10"/><line x1="12" x2="12" y1="8" y2="12"/><line x1="12" x2="12.01" y1="16" y2="16"/></svg></span>Add an @ to the address.</span></label>
  <label class="block w-full"><span class="type-ui">Name</span><input type="text" placeholder="Your name" disabled class="mt-2 h-12 w-full rounded-full border bg-card px-5 text-base placeholder:text-muted-foreground disabled:opacity-40 border-input" /></label>
</div>
```

### Segmented control

Two to four views of the same content. The selected segment is a white pill with `shadow-sm` on the gray track.

```html
<div role="tablist" aria-label="Period" class="inline-flex rounded-full bg-secondary p-1">
  <button type="button" role="tab" aria-selected="true" class="h-9 rounded-full px-4 type-ui text-muted-foreground transition-colors aria-selected:bg-card aria-selected:text-foreground aria-selected:shadow-sm">Day</button>
  <button type="button" role="tab" aria-selected="false" class="h-9 rounded-full px-4 type-ui text-muted-foreground transition-colors aria-selected:bg-card aria-selected:text-foreground aria-selected:shadow-sm">Week</button>
  <button type="button" role="tab" aria-selected="false" class="h-9 rounded-full px-4 type-ui text-muted-foreground transition-colors aria-selected:bg-card aria-selected:text-foreground aria-selected:shadow-sm">Month</button>
</div>
```

### Badge

Status is a colored dot plus a word, never color alone.

```html
<div class="flex flex-col items-start gap-2">
  <span class="inline-flex h-7 items-center gap-1.5 rounded-full bg-secondary px-3 type-caption"><span class="size-1.5 rounded-full bg-success"></span>Active</span>
  <span class="inline-flex h-7 items-center gap-1.5 rounded-full bg-secondary px-3 type-caption"><span class="size-1.5 rounded-full bg-warning"></span>Pending</span>
  <span class="inline-flex h-7 items-center gap-1.5 rounded-full bg-secondary px-3 type-caption"><span class="size-1.5 rounded-full bg-destructive"></span>Failed</span>
  <span class="inline-flex h-7 items-center gap-1.5 rounded-full bg-secondary px-3 type-caption"><span class="size-1.5 rounded-full bg-muted-foreground"></span>Draft</span>
</div>
```

### Progress

A 6px track with a blue fill. Put the label and the value above it.

```html
<div class="w-full space-y-6">
  <div>
    <p class="mb-2 flex justify-between type-small"><span>Upload</span><span class="text-muted-foreground">64%</span></p>
    <div role="progressbar" aria-label="Upload" aria-valuenow="64" aria-valuemin="0" aria-valuemax="100" class="h-1.5 w-full overflow-hidden rounded-full bg-secondary"><div class="h-full w-[64%] rounded-full bg-primary"></div></div>
  </div>
  <div>
    <p class="mb-2 flex justify-between type-small"><span>Download</span><span class="text-muted-foreground">28%</span></p>
    <div role="progressbar" aria-label="Download" aria-valuenow="28" aria-valuemin="0" aria-valuemax="100" class="h-1.5 w-full overflow-hidden rounded-full bg-secondary"><div class="h-full w-[28%] rounded-full bg-primary"></div></div>
  </div>
</div>
```

### List

Rows of 48px inside a 24px panel, divided by hairlines. A row that opens a page ends with a chevron.

```html
<ul class="w-full divide-y divide-border overflow-hidden rounded-lg border border-border">
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Account<span class="text-muted-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="m9 18 6-6-6-6"/></svg></span></li>
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Notifications<span class="text-muted-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="m9 18 6-6-6-6"/></svg></span></li>
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Privacy<span class="text-muted-foreground"><svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="m9 18 6-6-6-6"/></svg></span></li>
</ul>
```

### List with controls

A settings list: each row names a setting on the left and holds its control or value on the right. A toggle row applies at once; a value row with a chevron opens a choice.

```html
<ul class="w-full divide-y divide-border overflow-hidden rounded-lg border border-border">
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Notifications<button type="button" role="switch" aria-checked="true" aria-label="Notifications" class="group relative h-7.5 w-17.5 shrink-0 rounded-full bg-input transition-colors aria-checked:bg-primary disabled:opacity-40"><span class="absolute top-1 left-1 h-5.5 w-9 rounded-full bg-white shadow-sm transition-transform group-aria-checked:translate-x-6.5"></span></button></li>
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Language<span class="flex items-center gap-1 type-small text-muted-foreground">English<svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" aria-hidden="true"><path d="m9 18 6-6-6-6"/></svg></span></li>
  <li class="flex h-12 items-center justify-between gap-4 px-4 type-ui">Sync<span class="inline-flex h-7 items-center gap-1.5 rounded-full bg-secondary px-3 type-caption"><span class="size-1.5 rounded-full bg-success"></span>Active</span></li>
</ul>
```

### Spinner

28px for a region that is loading, 20px inside a row or next to a button.

```html
<div class="flex items-center gap-6">
  <span role="status" aria-label="Loading" class="size-7 border-3 animate-spin rounded-full border-secondary border-t-primary"></span>
  <span role="status" aria-label="Loading" class="size-5 border-2 animate-spin rounded-full border-secondary border-t-primary"></span>
</div>
```

### Card

A white surface with a 32px radius and a hairline border, on the gray page. Padding is 24px (`p-6`); a card that holds a whole section of a page, such as a group of settings, may use 28px (`p-7`).

```html
<article class="w-full rounded-2xl border border-border bg-card p-6">
  <h3 class="type-title">Card title</h3>
  <p class="mt-1 type-small text-muted-foreground">Supporting text that explains the item in a line or two.</p>
  <div class="mt-5 flex gap-2">
    <button type="button" class="inline-flex h-9 items-center justify-center gap-2 rounded-full px-4 type-ui transition-colors disabled:pointer-events-none disabled:opacity-40 bg-primary text-primary-foreground hover:bg-primary-hover">Continue</button>
    <button type="button" class="inline-flex h-9 items-center justify-center gap-2 rounded-full px-4 type-ui transition-colors disabled:pointer-events-none disabled:opacity-40 text-foreground hover:bg-accent">Cancel</button>
  </div>
</article>
```

The gallery's own cards add a footer with the title on the left and icon buttons on the right: `flex aspect-[9/10] flex-col` on the card, the demo in `flex flex-1 items-center justify-center px-6 pt-6`, and the footer `flex h-16 items-center justify-between pr-4 pb-2 pl-6`, so the title lines up with the content edge.

### Focus

Every interactive element gets the global focus ring from `raster.css`: a 2px `ring` outline with a 2px offset. Do not remove it.

## Do's and Don'ts

- Do keep one primary button per view. A second action is secondary or ghost.
- Do put content on cards and let the gray page separate them.
- Do pair every status color with a word.
- Do give icon-only buttons an `aria-label` and form controls a visible label.
- Don't add a second accent color, gradients or tinted backgrounds.
- Don't use square or slightly rounded corners. Controls are pills, cards are 32px.
- Don't add shadows to cards. Only thumbs and floating surfaces have one.
- Don't use the default Tailwind palette or hard-coded hex values in components.
- Don't shrink interface text below 12px or text inputs below 16px.
