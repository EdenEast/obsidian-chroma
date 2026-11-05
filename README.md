# Chroma

Chroma is a personal Obsidian theme with neutral backgrounds and a choice of color schemes. It has six schemes of its own, each with light and dark versions. It also includes ported schemes such as Dracula and Gruvbox.

## Install the theme

1. Copy this folder to `<vault>/.obsidian/themes/Chroma`. Keep the folder name, because it must match the name in `manifest.json`.
2. In Obsidian, open **Settings > Appearance > Themes** and select **Chroma**.

Obsidian loads `theme.css` directly, so the theme has no build step.

## Change the settings

Install the [Style Settings](https://github.com/community-archive/obsidian-style-settings) plugin, then open **Settings > Style Settings > Chroma**. Without the plugin, Chroma uses the Neutral scheme and the default options.

### Chroma color schemes

**Color scheme** offers Neutral, Harbor, Parchment, Forest, Carbon, and Mulberry.

### Other color schemes

Dark mode and light mode each have their own setting, so each mode can use a different scheme. A selected scheme replaces the Chroma color scheme in that mode. If you select None, that mode uses the Chroma color scheme.

- **Dark mode scheme** offers Dracula, Tokyo Night, Gruvbox Dark, Horizon, Sonokai Espresso, Nordic, Coffee, Nightfox, Mocha Dark, and Panda Syntax.
- **Light mode scheme** offers Gruvbox Light, Dayfox, and Panda Syntax.

### Components

These settings work with every color scheme.

- **Callout appearance** offers Filled, Outlined, Accent line, Tinted with accent line, Tinted, and Solid.
- **Heading colors** offers Plain, Accent, and Rainbow.
- **Folder colors** offers Plain, Colored text, and Colored blocks.
- **Disable alternate checkboxes** restores Obsidian's standard checkboxes.
- **Colorful links and emphasis** shows internal links as soft pills and colors bold and italic text.
- **Disable table style** restores Obsidian's standard tables.
- **Disable active line highlight** removes the accent color from the line that holds the text cursor.

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
