# Stone

A muted, neutral grey colour theme with slate blue and teal accents, in a light and a dark variant. Inter is used for UI text and Fira Code for code.

## Palette

### Base colours

| Token | Stone (light) | Stone dark | Used for |
|---|---|---|---|
| `bg` | `#d3d3cf` | `#1a1b1a` | page and window background |
| `surface` | `#c6c6c1` | `#242524` | raised surfaces, code blocks, today column |
| `hover` | `#c8c8c3` | `#2a2c2a` | hover and selected rows |
| `text` | `#2e302f` | `#d9dbd7` | main text |
| `text-2` | `#2e302f` | `#c3c6c1` | secondary text |
| `muted` | `#636663` | `#8a8d88` | muted text, inactive items |
| `faint` | `#7d807c` | `#6b6e6a` | hints, placeholders |
| `line` | `#858883` | `#4a4d49` | strong borders, focus |
| `border` | `#b3b4af` | `#333532` | default borders and dividers |

On the websites, `--line` uses `#858883` in light and `#333532` in dark, because borders are drawn with `--line` there.

### Accents

| Name | Light | Dark | Used for |
|---|---|---|---|
| Slate | `#4f6577` | `#8fa6b8` | primary accent, H1, focus, active states |
| Teal | `#4a6f6a` | `#86aaa3` | secondary accent, H2, section labels |
| Sage | `#5d6e52` | `#9aab8c` | H3, blockquotes |
| Steel | `#566a80` | `#94a7bd` | H4 |
| Moss | `#627056` | `#a4b292` | H5 |
| Blue-grey | `#5b6a73` | `#9daab2` | H6, list markers |

### Derived

| Name | Light | Dark | Used for |
|---|---|---|---|
| Selection | `#aeb3b2` | `#3e4446` | selected row, surface tinted 20% toward slate |
| Slate on selection | `#3c4f5e` | `#8fa6b8` | accent text on a selected row |
| OK | `#6f7d5f` | `#8d9b7b` | status: up |
| Down / error | `#9a5f5a` | `#b47e79` | status: down, errors |
| Warning | `#8a7a45` | `#b09a55` | warnings |

### Categorical colours

Used for calendar events and DMS category badges. Each has a background, a bar (accent stripe) and a foreground.

| # | Name | Light bg / bar / fg | Dark bg / bar / fg |
|---|---|---|---|
| 0 | sage | `#c5cdb9` `#6f7d5f` `#2c3324` | `#2f3529` `#8d9b7b` `#d6dccb` |
| 1 | clay | `#dfc3ac` `#a0694a` `#3d2a1c` | `#3b2e25` `#b8876a` `#e6d3c4` |
| 2 | ochre | `#dccd9b` `#98803a` `#3a3214` | `#37311f` `#b29b58` `#e3dab8` |
| 3 | rose | `#dcbab8` `#9a5f5a` `#3b2422` | `#3b2b2a` `#b47e79` `#e6cfcc` |
| 4 | lavender | `#c9c1d6` `#6f6390` `#2a2636` | `#2f2b38` `#9087ad` `#d8d4e3` |
| 5 | slate | `#b7c5d1` `#56718a` `#222d36` | `#263039` `#7e98ae` `#cfd9e1` |
| 6 | teal | `#b3cbc6` `#4c7a72` `#1f322f` | `#233431` `#74a198` `#cde0dc` |
| 7 | plum | `#d2bccb` `#85597a` `#36222f` | `#362932` `#a87d9d` `#e3cfdc` |

### Terminal: Stone Latte (light)

The background is one step darker than Stone (`#c1c1bc`), with darker accents so text stays readable.

| Role | Hex |
|---|---|
| Background | `#c1c1bc` |
| Foreground | `#2a2c2b` |
| Cursor | `#2c4677` |
| Selection | `#a9aaa5` |
| Tab bar / inactive tab / hover | `#b1b1ac` / `#b9b9b4` / `#b5b5b0` |

| Slot | Normal | Bright |
|---|---|---|
| black | `#5a5d59` | `#7e817d` |
| red | `#8c3e38` | `#b05a52` |
| green | `#36592c` | `#527b45` |
| yellow | `#6a5212` | `#8f7425` |
| blue | `#34528a` | `#5070ac` |
| magenta | `#684380` | `#8a5fa3` |
| cyan | `#215c54` | `#367d72` |
| white | `#a9aaa5` | `#d0d1cc` |

### Terminal: Stone Frappé (dark)

A mid-dark grey with pastel accents, inspired by Catppuccin Frappé.

| Role | Hex | Role | Hex |
|---|---|---|---|
| Crust | `#2d2f2e` | Red | `#d4918c` |
| Mantle | `#333534` | Peach | `#d8a07e` |
| Base | `#393b3a` | Yellow | `#d6c28e` |
| Surface 0 | `#444745` | Green | `#a9c08f` |
| Surface 1 | `#505351` | Teal | `#8dbfb4` |
| Surface 2 | `#5d605d` | Sky | `#93bccc` |
| Overlay | `#7d807c` | Blue | `#8fa9cf` |
| Subtext | `#bfc2bd` | Lavender | `#a9b3d6` |
| Text | `#dcdfda` | Mauve | `#c4a3c8` |

## Fonts

- **Inter:** UI text. Weights 300 (body), 400 (headings) and 500 (bold).
- **Fira Code / FiraCode Nerd Font:** Code and terminals. The Nerd Font version adds icons. Use `FiraCode Nerd Font Mono` in terminals.

Installing the Nerd Font:

```bash
mkdir -p ~/.local/share/fonts/FiraCodeNerd && cd $_
curl -fLO https://github.com/ryanoasis/nerd-fonts/releases/latest/download/FiraCode.tar.xz
tar -xf FiraCode.tar.xz && rm FiraCode.tar.xz && fc-cache -f
```

## Repository layout

```
stone/
├── README.md
├── web/themes.css               tokens for the websites
├── obsidian/Stone/              manifest.json, theme.css
├── firefox/manifest.json        static theme with light + dark
├── dms/stone.json               DankMaterialShell custom theme
├── niri/focus-ring.kdl          fallback focus-ring colours
├── fuzzel/fuzzel.ini            light and dark [colors] blocks
├── wezterm/stone.lua            Stone Latte and Stone Frappé
├── canvas/canvas.user.css       Stylus style for Canvas
└── zsh/completion.zsh           readable completion highlight
```

## Programs

### Websites (NTNU dashboard, server homepage)

- **Files:** `src/styles/themes.css` (NTNU) and `site/styles.css` (homepage).
- **How it works:** Tokens are defined once with `light-dark(light, dark)` in `:root`. With no theme chosen, the browser follows the system: Stone in light mode, Stone dark in dark mode. Each `[data-theme]` block pins `color-scheme` and overrides only what differs.
- **Accents:** Components use `--accent` (slate) and `--accent-2` (teal) directly. Other palettes set these back to their own text and muted colours.
- **Adding a theme:** Add an entry in `config/themes.ts` (NTNU) or `THEMES` in `app.js` (homepage), plus a CSS block.

### Obsidian

- **Location:** `<vault>/.obsidian/themes/Stone/manifest.json` and `theme.css`.
- **Enable:** Settings → Appearance → Themes → Stone. Base colour scheme Light or Dark picks the variant.
- **Contents:** Headings use the six accent colours. Tags, checkboxes and inline code are teal, blockquotes sage, list markers blue-grey.
- **Fonts:** Obsidian uses installed fonts, so install Inter and Fira Code locally.

### Firefox

- **File:** `manifest.json` with a `theme` (light) and a `dark_theme` block. Firefox switches between them with the system setting.
- **Testing:** `about:debugging` → This Firefox → Load Temporary Add-on.
- **Permanent install:** Zip the folder, submit it as unlisted on addons.mozilla.org, then install the signed `.xpi` from Manage Status & Versions.
- **Forcing light:** If tabs stay dark in light mode, set `ui.systemUsesDarkTheme` to `0` in `about:config`, and make sure `frame_inactive` and `tab_text` are set.
- **Updating:** Raise `"version"` and upload with New Version.

### DankMaterialShell

- **Location:** `~/.config/DankMaterialShell/themes/stone/stone.json`.
- **Enable:** Settings → Theme & Colors → Custom → pick the file. Selecting it in the UI is more reliable than editing `settings.json` by hand.
- **Contents:** `dark` and `light` variants that follow DMS's own light/dark mode. Primary is slate, secondary teal, tertiary sage. The `accents` block sets category badge colours. `matugen_type` is `scheme-neutral`.
- **Version note:** Written for DMS 1.6/1.7. The `accents` block is from the 1.7 docs and may be ignored on 1.6.

### niri

- DMS writes niri's focus-ring and border colours to `~/.config/niri/dms/colors.kdl`, which `config.kdl` includes. Switching DMS theme away and back regenerates it with the Stone colours.
- Don't edit `dms/colors.kdl` itself. To override it, put a `layout { focus-ring { … } }` block after the `include` lines in `config.kdl` (later settings win). Values: `#4f6577` / `#b3b4af` (light), `#8fa6b8` / `#333532` (dark).

### Fuzzel

- **Location:** `~/.config/fuzzel/fuzzel.ini`. It doesn't exist by default; create it.
- **Variant:** There's no automatic light/dark, so keep the `[colors]` block for the variant you use.
- **Colours:** RRGGBBAA without `#`. Matches use slate, and the selected row uses the derived selection colour, like DMS.
- **Font:** `font=FiraCode Nerd Font:size=11:weight=light`, or Inter.

### WezTerm

- **Location:** `~/.config/wezterm/wezterm.lua`. The schemes go in `config.color_schemes`, then set `config.color_scheme = 'Stone Latte'`.
- **Recommended settings:**
  ```lua
  config.font = wezterm.font('FiraCode Nerd Font Mono', { weight = 'Regular' })
  config.bold_brightens_ansi_colors = 'No'
  ```
- **Light/dark switching:** Use `wezterm.gui.get_appearance()` to choose between Stone Latte and Stone Frappé.
- **If the background looks wrong:** WezTerm silently falls back to its dark default theme when `color_scheme` doesn't match a defined name.

### Powerlevel10k (zsh prompt)

Run `p10k configure` and choose **8 colors**. The prompt then uses the terminal's ANSI colours instead of fixed 256-colour values, so it follows the terminal scheme.

### zsh completion

Coloured completion highlights are hard to read in a light theme. Use a grey highlight in `~/.zshrc`:

```zsh
zstyle ':completion:*' list-colors "${(s.:.)LS_COLORS}" 'ma=48;5;250;38;5;236'
```

### Canvas LMS

- **How:** Install the Stylus extension, open the Canvas site, then Write style for that site, and paste `canvas.user.css`.
- **What it does:** It overrides Canvas's `--ic-brand-*` variables plus the main layout backgrounds.
- **Limitations:** Newer Instructure UI parts may need extra selectors, and Canvas updates can rename classes.
- **Dark:** For dark mode, Dark Reader with background `#1a1b1a` and text `#d9dbd7` is easier.

## Checking colours in a terminal

```bash
for i in {0..15}; do
  printf '\e[38;5;%sm %2d ████ sample \e[0m' "$i" "$i"
  (( i % 4 == 3 )) && echo
done
```
