# luc-themes

A collection of themes for [luc](https://github.com/lutefd/luc), packaged for `luc pkg install`.

## Themes included

| Name    | Inherits | Description                                                 |
|---------|----------|-------------------------------------------------------------|
| `white` | `light`  | Crisp, high-contrast light theme with a paper feel.         |

More themes can be added to this package over time — just drop another file in `themes/` and bump the version.

## Install

```sh
luc pkg install github.com/lutefd/luc-themes
```

Or, for a local checkout:

```sh
luc pkg install ./path/to/luc-themes
```

## Activate

After installing, reload luc (`luc reload` or `ctrl+r`) and pick a theme from the theme switcher.

To persist one across sessions, add to `~/.config/luc/config.yaml`:

```yaml
ui:
  theme: white
```

## Layout

```
luc-themes/
├── luc.pkg.yaml        # package manifest (schema: luc.pkg/v1)
├── themes/
│   └── white.yaml      # individual theme files
├── LICENSE
└── README.md
```

## Theme: `white`

A crisp, high-contrast light theme. GitHub Light-inspired palette, carefully chosen diff colors, pure white canvas.

### Design

- **`bg: #ffffff`** — true white canvas.
- **`text: #1f2328`** — near-black ink, softer than `#000` on bright white, still AAA contrast.
- **`accent: #0969da`** — GitHub Light blue; works both as text and as a highlight background.
- **Muted tiers** (`#57606a` / `#6e7781`) — secondary info recedes without disappearing; both pass AA on white.
- **`warn: #9a6700`** (ochre) — yellow text on white is a readability trap; ochre stays legible.
- **Diffs** — pale green/red washes with deep ink, readable side-by-side.

### Palette reference

| Token         | Hex       | Purpose                        |
|---------------|-----------|--------------------------------|
| `bg`          | `#ffffff` | Terminal background            |
| `panel`       | `#f6f8fa` | Faint panel surface            |
| `panel_alt`   | `#eaeef2` | Deeper panel tone              |
| `line`        | `#d0d7de` | Borders / dividers             |
| `accent`      | `#0969da` | Primary blue                   |
| `accent_alt`  | `#8250df` | Secondary violet               |
| `text`        | `#1f2328` | Primary ink                    |
| `muted`       | `#57606a` | Secondary text                 |
| `subtle`      | `#6e7781` | Tertiary text / hints          |
| `success`     | `#1a7f37` | Deep green                     |
| `warn`        | `#9a6700` | Ochre                          |
| `blue`        | `#0969da` | Blue semantic                  |
| `cyan`        | `#1b7c83` | Darkened cyan                  |
| `error_text`  | `#cf222e` | Red                            |
| `diff_add_bg` | `#dafbe1` | Added line background          |
| `diff_add_fg` | `#116329` | Added line foreground          |
| `diff_del_bg` | `#ffebe9` | Removed line background        |
| `diff_del_fg` | `#82071e` | Removed line foreground        |

## License

MIT — see [LICENSE](./LICENSE).
