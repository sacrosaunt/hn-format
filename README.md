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

### Prerequisites
You need a userscript manager browser extension:
- [Tampermonkey](https://www.tampermonkey.net/) (Chrome, Firefox, Safari, Edge)
- [Greasemonkey](https://www.greasespot.net/) (Firefox)
- [Violentmonkey](https://violentmonkey.github.io/) (Chrome, Firefox, Edge)

### Install the Script
1. Install a userscript manager (Tampermonkey recommended)
2. Click on the userscript manager icon in your browser
3. Select "Create a new script" or "Add new script"
4. Copy and paste the contents of `hn-markdown-formatter.user.js` into the editor
5. Save the script (Ctrl+S or Cmd+S)

Alternatively, if you have the raw script file:
1. Open your userscript manager dashboard
2. Drag and drop the `hn-markdown-formatter.user.js` file onto the dashboard

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

- **Target Sites**: `*://news.ycombinator.com/*`
- **Permissions**: No special permissions required (`@grant none`)
- **Execution**: Runs after page load (`@run-at document-end`)
- **Compatibility**: Works with HN's dynamic content loading

## Features in Detail

### Security
- HTML entities are properly escaped to prevent XSS attacks
- Existing HN links are preserved during processing
- Only processes text content, not executable code

### Performance
- Uses MutationObserver for efficient dynamic content detection
- Processes only new/unprocessed content
- Minimal performance impact on page load

### Styling
- Matches HN's visual design language
- Responsive and accessible formatting
- Proper contrast and readability

## Browser Compatibility

Works in all modern browsers that support:
- ES6+ JavaScript features
- MutationObserver API
- CSS3 styling

Tested with:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

## Contributing

Feel free to submit issues or pull requests to improve the script. Common areas for enhancement:
- Additional markdown syntax support
- Improved styling
- Performance optimizations
- Bug fixes

## License

This project is open source. Feel free to modify and distribute according to your needs.

## Version History

- **v1.0**: Initial release with basic markdown formatting support
  - Bold, italic, underline text
  - Code blocks and inline code
  - Blockquotes and bullet points
  - Dynamic content support

## Troubleshooting

**Script not working?**
- Ensure your userscript manager is enabled
- Check that the script is active in your userscript manager
- Refresh the Hacker News page
- Check browser console for any error messages

**Formatting not appearing?**
- Make sure you're using the correct markdown syntax
- The script only processes new content after installation
- Try refreshing the page to reprocess existing content

**Conflicts with other extensions?**
- Disable other HN-related extensions temporarily to test
- Check if other userscripts are interfering
- Ensure this script loads after page content
