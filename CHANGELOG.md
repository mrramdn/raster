# Changelog

Raster uses semantic versions. While it is in beta, a minor version adds or changes tokens, components or rules,
and a patch fixes them. Every version is a git tag (`v0.1.0`) and an entry in the design site's record.

## 0.3.0 (2026-10-26)

Button labels reach WCAG AA in both modes, and the files say who made them and how they may be used.

- `primary` is `#0066E0` in both modes (was `#007AFF` light, `#0A84FF` dark), `primary-hover` is `#0058C2` light
  and `#0071E3` dark (was `#006AE0` and `#3D9BFF`), and `destructive` is `#D70015` in both modes (was `#FF3B30`
  and `#FF453A`). White labels are now 5.3:1 on the blue and 5.4:1 on the red, and at least 4.7:1 on every hover
  fill, where before they were 2.9:1 to 4.0:1. `ring` keeps the lighter blues `#007AFF` and `#0A84FF`, so focus
  still stands out. `DESIGN.md`'s front matter, Colors table and contrast notes give the new values and ratios;
  only the `input` outline is still below AA.
- A licence: `LICENSE` puts `raster.css` and `preview/` under MIT and `DESIGN.md` and the Figma library under
  CC BY 4.0. `package.json` says `MIT AND CC-BY-4.0`, line 1 of `raster.css` (carried into
  `preview/preview.css`) names the release, the author and the licence, and `DESIGN.md` opens its Overview with
  the same.
- `color-scheme: light` in `:root` and `color-scheme: dark` in `.dark`, so native controls and scrollbars follow
  the theme.
- `--raster-build` in `:root` names the release a copy of `raster.css` came from. It is not a token; nothing
  reads it.
- `pnpm check` (`scripts/check-version.mjs`) fails while `package.json`, this file, the banners and
  `--raster-build` name different versions. `pnpm build` now also runs `scripts/banner-first.mjs`, which keeps the
  theme's banner on line 1 of `preview/preview.css`, above Tailwind's own. The README's release steps now cover
  `pnpm check`, the GitHub Release and the design site's pictures.
- The example screen's phone number is an invented, masked one.
- The example screen's header shows Catat as a word, without the round C beside it, and the Profile card's heading
  stands alone above the photo and its buttons. `DESIGN.md`'s Do's and Don'ts say the wordmark and headlines carry
  no icon, logo mark or initials badge.
- Figma: the variables `primary`, `primary-hover` and `destructive` take the new values.

## 0.2.2 (2026-10-24)

For screen readers; nothing looks different.

- The gallery's title, Raster, is its `h1`.
- The Figma library does not change.

## 0.2.1 (2026-10-15)

- The gallery has no filter row under the header any more. Its 18 cards are grouped under category headings
  (Input, Navigation, Status, Motion, Layout) in `type-title`, 32px above and 16px below; card names are `h3`.
- Figma: the filter chip row is gone from the headers of `Gallery/Light` and `Gallery/Dark`.

## 0.2.0 (2026-10-14)

A blank component sheet, the missing components and an example screen.

- The gallery is a blank template: neutral content ("Save", "Email", "Option A", "Active / Pending / Failed",
  "Card title") instead of "Get Started" and a delivery choice, and every card shows the variants and states its
  recipe defines (primary, secondary, ghost and destructive buttons, two sizes, disabled controls, a field with
  an error, selected and unselected). 18 live components, up from 10, with copy on every card and reset on the 9
  that keep state. Card footers now line up with the 24px content edge.
- `DESIGN.md` has 18 recipes, up from 13, with the same markup as the gallery. New: Checkbox, Button sizes,
  Destructive and disabled, Text field states and List with controls; Icon button gains a filled 40px variant,
  Spinner a 20px size, and Card is now a content card. The front matter gains `button-destructive`,
  `button-small`, `icon-button-filled`, `checkbox`, `segmented-control`, `badge` and `progress`. The contrast
  notes add white on `destructive` (3.6:1 and 3.4:1, below AA, with `#D70015` as the AA-safe value).
- `raster.css` gains the `raster-checkbox` utility: a round native checkbox, a blue disc with a white check.
- `preview/demo.html`: the settings screen of Catat, an invented notes app, built only from the recipes
  (15 kinds of component). `preview/input.css` scans it too.
- Figma: every recipe now has a component. New sets Checkbox, Segment (with a Segmented Control), Badge,
  Progress, Spinner and List Item, and a content Card; Button gains Destructive, Icon Button a Filled style,
  Text Field an Error state. 16 components, with 66 variants in 13 sets, up from 8 and 35; 23 Lucide icons, up
  from 12; 68 variables. Neutral text in the components, both galleries (now the same 18 cards as the web
  gallery) and the cover. A new page Example holds `Example/Light` and `Example/Dark`, the settings screen
  rebuilt from 77 instances each.

## 0.1.0 (2026-10-13)

First beta.

- Tokens in light and dark mode, in `raster.css` (Tailwind CSS v4, shadcn/ui token names) and in the front
  matter of `DESIGN.md`.
- `DESIGN.md` with the rules, the measured contrast of both modes and 13 recipes.
- A component gallery in `preview/` with 10 live components, category filters, and copy and reset on every
  card.
- The Figma library "Raster Design System": 67 variables in four collections, 10 text styles, 8 components
  with 35 variants, 12 icons, and a light and a dark gallery built from instances.
