# Chroma

Chroma is an Obsidian theme with neutral backgrounds and a choice of color schemes. It has seven schemes of its own, each with light and dark versions. It also includes ported schemes such as Dracula and Gruvbox.

## Install the theme

1. Copy this folder to `<vault>/.obsidian/themes/Chroma`. Keep the folder name, because it must match the name in `manifest.json`.
2. In Obsidian, open **Settings > Appearance > Themes** and select **Chroma**.

Obsidian loads `theme.css` directly, so the theme has no build step.

## Change the settings

Install the [Style Settings](https://github.com/community-archive/obsidian-style-settings) plugin, then open **Settings > Style Settings > Chroma**. Without the plugin, Chroma uses the Neutral scheme and the default options.

The settings are grouped into collapsible sections.

### Color schemes

- **Color scheme** offers Neutral, Harbor, Parchment, Forest, Carbon, Mulberry, and Crimson. Crimson pairs warm red accents with burgundy-tinted dark backgrounds and warm ivory light backgrounds.
- **Dark mode scheme** offers Dracula, Tokyo Night, Gruvbox Dark, Horizon, Sonokai Espresso, Nordic, Coffee, Nightfox, Mocha Dark, and Panda Syntax.
- **Light mode scheme** offers Gruvbox Light, Dayfox, and Panda Syntax.

Dark mode and light mode each have their own setting, so each mode can use a different scheme. A selected scheme replaces the **Color scheme** choice in that mode. If you select None, that mode uses **Color scheme**.

### Interface

- **Panel style** applies on desktop only. It offers these options:
  - **Default** gives sidebars a darker background.
  - **Cards** shows each panel as a borderless rounded card on a darker background, with floating tabs.
  - **Soft shadows** replaces the lines between panels with shadows.
  - **Three levels** makes the ribbon and tab bars darkest and the sidebars medium.
  - **Raised editor** darkens everything around the editor and rounds its top corners.
- **Folder colors** offers Plain, Colored text, and Colored blocks.
- **Disable active line highlight** removes the accent color from the line that holds the text cursor.

### Components

- **Callout appearance** offers Filled, Outlined, Accent line, Tinted with accent line, Tinted, and Solid.
- **Heading colors** offers Plain, Accent, and Rainbow.
- **Disable alternate checkboxes** restores Obsidian's standard checkboxes.
- **Colorful links and emphasis** shows internal links as soft pills and colors bold and italic text.
- **Disable table style** restores Obsidian's standard tables, Bases views, and Dataview lists.

Bases tables use the same filled headers and alternating row shading as Markdown tables. Tinted group headings and an outline around each table group make groups easier to scan. Bases list views and Dataview lists also use alternating row shading. Summary rows and cell selection keep their native behavior.

## Add a color scheme

1. In the settings block at the top of `theme.css`, add a labeled option to the setting for your scheme.
2. Add a CSS block for your scheme. Put a Chroma scheme after the last Chroma scheme, and put an other scheme after the last other scheme. Other schemes must stay below Chroma schemes, because the later block wins.
3. Start each selector with `:root`, as in `:root body.theme-dark:where(.chroma-palette-your-name)`. Without `:root`, Obsidian forces a black background on mobile.

The two kinds of scheme have different requirements:

- A Chroma scheme needs a `chroma-palette-*` class and a block for each mode.
- An other scheme needs a `chroma-other-dark-*` or a `chroma-other-light-*` class. It must set every variable that a Chroma scheme sets. A variable that it leaves out keeps the value from the Chroma scheme underneath.

Keep setting IDs stable, because Style Settings saves choices against them.

## Credits

The alternate checkbox icons are adapted from the [Border theme](https://github.com/Akifyss/obsidian-border) under the MIT license, and `theme.css` carries that notice. `theme.css` also lists the source of each other color scheme.
