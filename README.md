# deepspace.fscss

CSS-only deep-space planet scene for the FSCSS ecosystem.

Planet, atmosphere, moon orbit, starfield, and soft rays — **Pure CSS**.  
Styles are scoped to a host selector so the scene does not overflow the page unless you target `body`.

**Requires FSCSS ≥ 1.2.1**

## Install

```css
@import((*) from deepspace)
```

Quoted URL (always valid):

```css
@import((*) from "https://cdn.jsdelivr.net/gh/fscss-ttr/deepspace.fscss@main/deepspace.fscss")
```

```html
<script src="https://cdn.jsdelivr.net/npm/fscss@1.2.1/runtime.min.js" defer></script>
```

## Quick start (contained)

```css
@deepspace-root()
@deepspace(.scene)
:root {
  @deepspace-size(200px)
}
```

```html
<div class="scene" style="height: 380px">
  <div class="ds-rays"></div>
  <div class="ds-planet-system">
    <div class="ds-atmosphere"></div>
    <div class="ds-planet"></div>
    <div class="ds-moon-orbit"><div class="ds-moon"></div></div>
  </div>
  <div class="ds-title">Deep Space</div>
</div>
```

Overflow stays inside `.scene`.

## Full viewport

```css
@deepspace-root()
@deepspace-as-body()
@deepspace(body)
```

## Helpers

| Define | Role |
|--------|------|
| `@deepspace-root()` | Design tokens on `:root` (or custom root) |
| `@deepspace-size(planet)` | Scale planet / system / moon |
| `@deepspace(sel)` | Scene on `sel` (default `body`) |
| `@deepspace-as-body()` | `100vh` + no margin on `body` |

## Tokens

| Variable | Default |
|----------|---------|
| `--ds-planet` | `220px` |
| `--ds-system` | `320px` |
| `--ds-moon` | `42px` |
| `--ds-glow` | `rgba(80, 160, 255, 0.4)` |
| `--ds-bg-top` | `#0b0c1a` |
| `--ds-bg-bottom` | `#000000` |
| `--ds-title` | `rgba(180, 210, 255, 0.7)` |

## Markup classes

`ds-rays` · `ds-planet-system` · `ds-atmosphere` · `ds-planet` · `ds-moon-orbit` · `ds-moon` · `ds-title`

## License

MIT
