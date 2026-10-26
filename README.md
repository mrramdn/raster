# Raster

A soft, neutral design system: white cards on light gray, pill controls and one blue. The same tokens exist as a Tailwind CSS v4 theme, a `DESIGN.md` that people and coding agents follow, and a Figma library.

"Raster" is a working name.

## Files

| File | What it is |
| --- | --- |
| `raster.css` | Tailwind CSS v4 theme: color tokens (light and dark), radius, type utilities, slider and checkbox utilities. Token names follow shadcn/ui. |
| `DESIGN.md` | The rules and the component recipes, in the [design.md](https://github.com/google-labs-code/design.md) format. |
| `preview/index.html` | Component gallery built with the theme: 18 live components with neutral placeholder content and their variants and states, grouped under category headings, with a dark mode switch and copy and reset buttons per component. |
| `preview/demo.html` | An example screen built only from the recipes: the account settings of Catat, an invented notes app. |
| `CHANGELOG.md` | What changed in each version. |
| `LICENSE` | MIT for the CSS and the preview, CC BY 4.0 for `DESIGN.md` and the Figma library. |
| `scripts/check-version.mjs` | `pnpm check`: fails while a place that names the release disagrees with `package.json`. |
| `scripts/banner-first.mjs` | Run by `pnpm build`: puts the theme's `/*!` banner back on line 1 of `preview/preview.css`, above Tailwind's. |

Figma: [Raster Design System](https://www.figma.com/design/tQxnBjmeXskenoVIb4wCzd) (pages Cover, Foundations, Components and Example; Example rebuilds the demo screen from instances in light and dark).

## Use it in a project

1. Load Inter (for example `pnpm add @fontsource-variable/inter` and import it, or `next/font`).
2. Copy `raster.css` next to your main stylesheet and import it after Tailwind:

   ```css
   @import "tailwindcss";
   @import "./raster.css";
   ```

3. Copy `DESIGN.md` to the project root so coding agents follow the same rules.
4. Dark mode is the `.dark` class on `<html>`.

The theme removes the default Tailwind color palette on purpose. Use the semantic tokens (`bg-card`, `text-muted-foreground`, `bg-primary` and so on).

## Preview

```sh
pnpm install
pnpm build   # writes preview/preview.css from the classes in preview/index.html and preview/demo.html
pnpm dev     # same, watching for changes
```

Then open `preview/index.html` (the gallery) or `preview/demo.html` (the example screen) in a browser. Copy needs a secure context, so serve the folder (`python3 -m http.server -d preview`) if the clipboard button does nothing over `file://`.

`npx @google/design.md lint DESIGN.md` checks the token file. It reports no errors and no contrast warnings; the eight warnings are tokens that only the prose uses.

## Versions

The version is in `package.json`, `CHANGELOG.md` says what changed, and every release is a git tag. To release:

1. Change the files and run `pnpm build`, so `preview/preview.css` matches.
2. Raise the version everywhere it is written: `version` in `package.json`, a new entry at the top of `CHANGELOG.md`, the `/*!` banner on line 1 of `raster.css` and `preview/input.css`, and `--raster-build` in `raster.css`'s `:root`. Run `pnpm build` again and `pnpm check`, which fails while any of them differ.
3. Commit, tag `v<version>` (`git tag -a v0.3.0 -m "Raster 0.3.0"`) and push with `git push --follow-tags`, then publish a GitHub Release from the tag with the CHANGELOG entry.
4. On the design site, run `pnpm sync:system raster <this folder>`, put the pictures in `public/images/raster/<version>/`, and add the version to the record. The site's tests fail while the record, the synced files or a version the gallery names disagree.
5. Optionally, after the site deploys, save a Wayback snapshot of the product page in both languages.

## The look

Raster is calm and rounded. Content sits on white cards with a 32px radius on a light gray page, depth comes from that step and a 1px border rather than from shadows, every control is a pill, and a single blue marks what is on, selected or primary. Button, Toggle, Slider and Single selection set the language; the other components, the dark mode and the type scale are built from the same parts. `DESIGN.md` has the rules and the contrast of the main color pairs.

## Licence

The code and the written rules are licensed separately; [`LICENSE`](LICENSE) has both texts.

- `raster.css` and everything in `preview/` (HTML and CSS) are under the MIT License.
- `DESIGN.md` and the Figma library "Raster Design System" are under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Copy and adapt them, also commercially, with credit: "Raster by Rifki Ramdani, https://uiux.mrramdn.com/en/systems/raster".
