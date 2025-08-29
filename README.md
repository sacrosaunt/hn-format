# HN Markdown Formatter

A userscript that adds markdown-style formatting support to Hacker News comments and posts.

## Features

This userscript enhances Hacker News by adding support for common markdown formatting syntax:

- **Bold text**: `**bold**` or `__bold__`
- *Italic text*: `*italic*` or `_italic_`
- <u>Underlined text</u>: `~underlined~`
- `Inline code`: `` `code` ``
- Code blocks: ``` ```code``` ```
- > Blockquotes: `> quoted text`
- Bullet points: `- item` or `* item`
- Proper styling with syntax highlighting and improved readability

## Installation

### Option 1: Easy Installation via Greasy Fork (Recommended)
1. Click the [Install button on Greasy Fork](https://greasyfork.org/en/scripts/547665-hn-markdown-formatter)
2. Your userscript manager will automatically install the script
3. That's it! The script will work immediately on Hacker News

### Option 2: Manual Installation
**Prerequisites:**
You need a userscript manager browser extension:
- [Tampermonkey](https://www.tampermonkey.net/) (Chrome, Firefox, Safari, Edge)
- [Greasemonkey](https://www.greasespot.net/) (Firefox)
- [Violentmonkey](https://violentmonkey.github.io/) (Chrome, Firefox, Edge)

**Install the Script:**
1. Install a userscript manager (Tampermonkey recommended)
2. Click on the userscript manager icon in your browser
3. Select "Create a new script" or "Add new script"
4. Copy and paste the contents of `hn-format.user.js` into the editor
5. Save the script (Ctrl+S or Cmd+S)

**Alternative manual method:**
1. Open your userscript manager dashboard
2. Drag and drop the `hn-format.user.js` file onto the dashboard

## Usage

Once installed, the script automatically works on all Hacker News pages (`news.ycombinator.com`). Simply use markdown syntax in your comments and posts:

### Formatting Examples

**Bold Text:**
```
**This will be bold**
__This will also be bold__
```

**Italic Text:**
```
*This will be italic*
_This will also be italic_
```

**Underlined Text:**
```
~This will be underlined~
```

**Code:**
```
`inline code`

```
code block
with multiple lines
```
```

**Blockquotes:**
```
> This is a quoted text
> It can span multiple lines
```

**Lists:**
```
- First item
- Second item
  - Nested item
- Third item

* Alternative bullet style
* Works the same way
```

## How It Works

The script:
1. Injects custom CSS styles for formatted elements
2. Scans comment and post content for markdown syntax
3. Converts markdown to HTML while preserving existing HN functionality
4. Watches for dynamically loaded content (new comments, etc.)
5. Maintains compatibility with HN's existing link formatting

## Technical Details

- **Target Sites**: `http://news.ycombinator.com/*` and `https://news.ycombinator.com/*`
- **Permissions**: No special permissions required (`@grant none`)
- **Execution**: Runs after page load (`@run-at document-end`)
- **Compatibility**: Works with HN's dynamic content loading

## Features in Detail

### Performance
- Uses MutationObserver for efficient dynamic content detection
- Processes only new/unprocessed content
- Minimal performance impact on page load

### Styling
- Matches HN's visual design language
- Responsive and accessible formatting
- Proper contrast and readability

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

The MIT License allows you to:
- Use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software
- Use the software for any purpose, including commercial use
- Modify the software and distribute modified versions
- The only requirement is that the original copyright notice and license must be included in all copies

For the full license text, see [LICENSE](LICENSE).