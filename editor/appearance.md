---
title: Themes and Editor Settings
---

## Themes

Drafts supports app-wide themes to customize appearance, and light and dark modes. To access theme settings, open the `Aa` appearance settings screen from the bottom right of the editor.

<div class="doc-image">
<img src="{{ site.baseurl }}/images/docs/editor/appearance-themes.png" alt="Advanced Settings"/>
</div>

The **Active Theme** section controls whether the light or dark theme is currently active. Automatic mode can be used to switch between light and dark themes based on the brightness of the device. This works great when Auto-brightness is enabled in iOS Settings, but also if you manually adjust brightness on the device.  The "brightness Threshold" slider controls the what device brightness is the switching point between themes in automatic mode.

The **Theme Selection** section allows selection of which of Drafts installed theme options should be used for light and dark modes. Also, allows selection of alternate app icons by tapping the icon.

#### Syntax Highlighting

Drafts offers support of inline syntax highlighting for several different types of markup, with more planned in the future.  Syntax highlighting is saved per-draft, and editor settings are stored separately by syntax, so font sizes, margins, and other options can differ by syntax.

- **Current**: Assign syntax to use for the current active draft. This selection will be saved with the draft.
- **Default**: Select default syntax to assign to new drafts.

In the syntax highlighting section the selection can be changed for the current active draft, or the default for new drafts.  The remaining syntax specific editor settings below will effect all drafts matching the "Current" syntax selection.

#### Options for Current Syntax

The Appearance screen also offers fine grained control over options for many editor related settings, controlling text behaviors, fonts and sizings as well as the editing environment in general.

- **Font**: Font to use for most text. Any font installed on the device can be selected.
- **Monospace**: Some syntax highlighting options will specify certain text passages be displayed in a Monospace font – like inline code blocks in Markdown. This is the font to use for those passages.
- **Base font size**: The point size of text.
- **Line height**: Multiplier for spacing between lines, where 1.0 is the default spacing for the current font.
- **Paragraph spacing**: Spacing between paragraphs.
- **Margin**: Controls leading and trailing margins in the editor.
- **Paragraph numbers**: Display paragraph numbers to the left of the text.
- **Autocorrect**: Enable or disable iOS autocorrect.
- **Spell checking**: Enable or disable iOS spell checking.
- **Smart quotes**: Enable or disable iOS smart quote replacements which replace straight single and double quotes with open and close quotes.
- **Smart dashes**: Enable or disable iOS smart dashes replacements.
- **Capitalization**: Auto-Capitalization mode.

## Other Settings

- **Hide Status Bar**: Disable iOS status bar when in Drafts.
- **Edit on draft selection**: If enabled, when new drafts are loaded the editor will automatically focus the draft for editing, displaying the keyboard.  If disabled, drafts will be loaded for viewing and an additional tap is need to begin editing.
- **Hide toolbar while editing**: If enabled, the row of icons at the top of the editing screen will slide away when editing text.
