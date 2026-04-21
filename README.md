# luc-themes

A collection of themes for [luc](https://github.com/lutefd/luc), packaged for `luc pkg install`.

## Themes included

| Name           | Inherits | Vibe                                                              |
|----------------|----------|-------------------------------------------------------------------|
| `white`        | `light`  | Crisp, high-contrast light theme with a paper feel.               |
| `cyberpunk`    | `dark`   | Neon-on-near-black: electric yellow + cyan accents.               |
| `weaver-ember` | `dark`   | Warm orange-on-ember dark theme; cream text on near-black canvas. |

More themes can be added to this package over time — just drop another file in `themes/` and bump the version.

## Install

```sh
luc pkg install github.com/lutefd/luc-themes@latest
```

Or pin to an exact version:

```sh
luc pkg install github.com/lutefd/luc-themes@v0.2.0
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
  theme: white          # or: cyberpunk, weaver-ember
```

## Layout

```
luc-themes/
├── luc.pkg.yaml              # package manifest (schema: luc.pkg/v1)
├── themes/
│   ├── white.yaml            # light
│   ├── cyberpunk.yaml        # dark — neon
│   └── weaver-ember.yaml     # dark — warm orange
├── LICENSE
└── README.md
```

---

## Theme: `white`

A crisp, high-contrast light theme. GitHub Light-inspired palette, carefully chosen diff colors, pure white canvas.

### Design

- **`bg: #ffffff`** — true white canvas.
- **`text: #1f2328`** — near-black ink, softer than `#000` on bright white, still AAA contrast.
- **`accent: #0969da`** — GitHub Light blue; works both as text and as a highlight background.
- **Muted tiers** (`#57606a` / `#6e7781`) — secondary info recedes without disappearing; both pass AA on white.
- **`warn: #9a6700`** (ochre) — yellow text on white is a readability trap; ochre stays legible.
- **Diffs** — pale green/red washes with deep ink, readable side-by-side.

### Palette

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

---

## Theme: `cyberpunk`

Neon-on-near-black dark theme. Electric yellow as primary accent with cyan counter-accent, magenta/pink error and diff tones — everything reads like neon signs on matte panels.

### Design

- **`bg: #090B10`** — near-black with a slight cool cast so neon reads cleanly.
- **`accent: #FCEE0A`** — electric yellow; high-visibility selection highlight.
- **`accent_alt: #00F0FF`** — saturated cyan; pairs with yellow as the "second neon".
- **`error_text: #FF5C8A`** — hot pink error; stands apart from the warm warn color.
- **Diffs** lean magenta (del) and mint (add) to avoid colliding with accents.

### Palette

| Token         | Hex       | Purpose                  |
|---------------|-----------|--------------------------|
| `bg`          | `#090B10` | Near-black canvas        |
| `panel`       | `#11151C` | Panel surface            |
| `panel_alt`   | `#161C26` | Deeper panel             |
| `line`        | `#2B3442` | Borders                  |
| `accent`      | `#FCEE0A` | Electric yellow          |
| `accent_alt`  | `#00F0FF` | Cyan counter-accent      |
| `text`        | `#F5F7FA` | Primary text             |
| `muted`       | `#B7C0CC` | Secondary text           |
| `subtle`      | `#7E8A99` | Tertiary text            |
| `success`     | `#3DFFB5` | Mint                     |
| `warn`        | `#FFB020` | Amber                    |
| `blue`        | `#4DA3FF` | Blue semantic            |
| `cyan`        | `#00F0FF` | Neon cyan                |
| `error_text`  | `#FF5C8A` | Hot pink                 |
| `diff_add_bg` | `#123229` | Deep teal                |
| `diff_add_fg` | `#8DFFCF` | Mint glow                |
| `diff_del_bg` | `#3A1622` | Deep magenta             |
| `diff_del_fg` | `#FF9FBE` | Pink glow                |

---

## Theme: `weaver-ember`

Warm orange-on-ember dark theme. Cream body text on a faintly warm near-black canvas; orange accents feel native rather than tacked on. Designed as a companion for the Weaver workflow but general-purpose.

### Design

- **`bg: #1a110a`** — faintly warm near-black so orange accents feel native instead of neon.
- **`text: #f5e6d3`** — warm cream, ~14:1 contrast against `bg`.
- **`accent: #ff8c42`** — primary orange; `accent_alt: #ffb070` is a softer companion for secondary highlights.
- **Cool semantics** (`blue`, `cyan`) are muted so they read as "not orange" rather than competing with the accent.
- **Diffs** use balanced warm-green / warm-red washes so they don't clash with the orange UI.

### Palette

| Token         | Hex       | Purpose                   |
|---------------|-----------|---------------------------|
| `bg`          | `#1a110a` | Warm near-black canvas    |
| `panel`       | `#241810` | Panel surface             |
| `panel_alt`   | `#2e2016` | Deeper panel              |
| `line`        | `#4a3322` | Borders                   |
| `accent`      | `#ff8c42` | Primary orange            |
| `accent_alt`  | `#ffb070` | Soft orange               |
| `text`        | `#f5e6d3` | Warm cream                |
| `muted`       | `#c9a37a` | Secondary text            |
| `subtle`      | `#8a6a4a` | Tertiary text             |
| `success`     | `#7fd17f` | Green                     |
| `warn`        | `#ffcc66` | Amber                     |
| `blue`        | `#7eb6ff` | Muted blue                |
| `cyan`        | `#7ed4d4` | Muted cyan                |
| `error_text`  | `#ff6b6b` | Red                       |
| `diff_add_bg` | `#1f3a1f` | Warm green wash           |
| `diff_add_fg` | `#b8e8b8` | Soft green ink            |
| `diff_del_bg` | `#3a1f1f` | Warm red wash             |
| `diff_del_fg` | `#f0b0b0` | Soft red ink              |

---

## License

MIT — see [LICENSE](./LICENSE).
