# HN Markdown Formatter

A userscript that adds markdown-style formatting support to [Hacker News](https://news.ycombinator.com) comments and posts.

## Features

- Adds markdown formatting support to HN comments and posts
- Supports **bold**, *italic*, <u>underlined</u>, `code`, and more
- Works automatically on all HN pages
- Preserves existing HN functionality

## Installation

### Option 1: Easy Installation via Greasy Fork (Recommended)
Click this button:

[![Install](https://img.shields.io/badge/Install-Greasy%20Fork-brightgreen)](https://greasyfork.org/en/scripts/547665-hn-markdown-formatter)

### Option 2: Manual Installation

**Steps:**
1. Install a userscript manager like [Tampermonkey](https://www.tampermonkey.net/), [Greasemonkey](https://www.greasespot.net/), or [Violentmonkey](https://violentmonkey.github.io/)
2. Create a new script
3. Copy and paste the contents of `hn-format.user.js`
4. Save the script

## Usage

Once installed, the script automatically works on all Hacker News pages. Simply use markdown syntax in your comments and posts:

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

## License

MIT License - see [LICENSE](LICENSE) file for details.