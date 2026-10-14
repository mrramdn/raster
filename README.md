# Raster

A soft, neutral design system: white cards on light gray, pill controls and one blue. The same tokens exist as a Tailwind CSS v4 theme, a `DESIGN.md` that people and coding agents follow, and a Figma library.

"Raster" is a working name.

## Files

| File | What it is |
| --- | --- |
| `raster.css` | Tailwind CSS v4 theme: color tokens (light and dark), radius, type utilities, slider utility. Token names follow shadcn/ui. |
| `DESIGN.md` | The rules and the component recipes, in the [design.md](https://github.com/google-labs-code/design.md) format. |
| `preview/index.html` | Component gallery built with the theme. Has a dark mode switch, category filters, and copy and reset buttons per component. |
| `CHANGELOG.md` | What changed in each version. |

Figma: [Raster Design System](https://www.figma.com/design/tQxnBjmeXskenoVIb4wCzd) (pages Cover, Foundations and Components).

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
pnpm build   # writes preview/preview.css from the classes in preview/index.html
pnpm dev     # same, watching for changes
```

Then open `preview/index.html` in a browser. Copy needs a secure context, so serve the folder (`python3 -m http.server -d preview`) if the clipboard button does nothing over `file://`.

`npx @google/design.md lint DESIGN.md` checks the token file. It reports no errors; the warnings are tokens that only the prose uses and the documented 4.0:1 contrast of white on the blue.

## Versions

The version is in `package.json`, `CHANGELOG.md` says what changed, and every release is a git tag. To release:

1. Change the files and run `pnpm build`, so `preview/preview.css` matches the gallery.
2. Raise `version` in `package.json` and add an entry to `CHANGELOG.md`.
3. Commit, tag `v<version>` (`git tag -a v0.2.0 -m "Raster 0.2.0"`) and push with `git push --follow-tags`.
4. On the design site, sync this folder and add the version to Raster's record. The site's tests fail while the
   record states a different version from the synced files.

## Where the look comes from

The visual language was measured from one public screenshot of the COMPASS component gallery by Design Compass: colors sampled from the pixels, sizes and radii from the layout. Button, Toggle, Slider and Single Selection follow that screenshot. The other components, the dark mode and the type scale are extrapolated in the same style. This project is not affiliated with Design Compass and contains none of their code or assets.
