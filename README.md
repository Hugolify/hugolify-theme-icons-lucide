# Hugolify theme icons: Lucide

The [Lucide](https://lucide.dev/icons/) icons for
[hugolify-theme-icons](https://github.com/hugolify/hugolify-theme-icons), the
default set: UI and content icons such as `map-pin`, `phone` or `wrench`.

## Install

Nothing to do: hugolify-theme-icons imports this module. A site writes Lucide
names directly (`map-pin`), or with the prefix (`lucide:map-pin`) when another
set is its default.

## What it does

It mounts the `icons` folder of `github.com/lucide-icons/lucide` to
`assets/icons/lucide/`, where the engine resolves Lucide names. It holds no code.

## Lucide version

This module requires Lucide commit `cf0e1e44baa6` (2026-06-18), the oldest one
Hugolify sites have used. Go selects the highest version required, so a site
keeps the Lucide it pinned, and moves it on its own, from the site:

```sh
hugo mod get github.com/lucide-icons/lucide@main
```

Before that, check the site's icons against the new version: on 2026-11-03
Lucide removed or renamed about sixty icons (`circle-alert`, `triangle-alert`,
`trash-2`, `smile`, `history`, `heading`…). A name that no longer exists renders
nothing and logs `[icons] "name" not found in icons/lucide/`.

Never use `@latest`: `lucide-icons/lucide` stopped tagging around v0.289.0, and
its commits on `main` resolve to pseudo-versions numerically *below* that tag, so
`@latest` would move back to an old, legacy-named set (`home`, not `house`).

## Documentations

- [Lucide icons](https://lucide.dev/icons/)
- [hugolify-theme-icons](https://github.com/hugolify/hugolify-theme-icons)
- [Hugolify](https://www.hugolify.io/docs/)

## Licensing

Hugolify is free for personal or commercial projects (MIT license). Lucide is
licensed under the [ISC license](https://lucide.dev/license).
