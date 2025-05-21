
## Features

1. **Popup**: Displays a simple popup with the message "Hello from Popup!".
2. **Content Script**: Injected into all active pages and logs "Hello from content script" to the console.

## File Descriptions

### `manifest.json`
Defines the extension's metadata, permissions, and behavior. It uses Manifest V3 and specifies:
- A popup (`popup.html`) for the extension's action.
- A content script (`content.js`) that runs on all URLs.

### `popup.html`
The HTML file for the popup UI. It includes a heading with the text "Hello from Popup!".

### `popup.js`
The JavaScript file for the popup. It logs "Popup loaded" to the console when the popup is opened.

### `content.js`
The content script that is injected into all active pages. It logs "Hello from content script" to the console.

## How to Load and Test the Extension

1. Open Chrome and navigate to `chrome://extensions/`.
2. Enable **Developer mode** using the toggle in the top-right corner.
3. Click **Load unpacked** and select the `chrome-extension` folder.
4. The extension will appear in the list of installed extensions.
5. Click the extension's icon in the toolbar to open the popup. You should see "Hello from Popup!".
6. Open the browser's developer console on any webpage. You should see "Hello from content script" logged in the console.

## Permissions

The extension uses the following permissions:
- `activeTab`: Allows the extension to interact with the currently active tab.

## Notes

- The content script is injected into all pages (`<all_urls>`), so it will log the message on every webpage.
- The icons (`icon16.png`, `icon48.png`, `icon128.png`) are placeholders and can be replaced with custom icons.

## License

This project is for educational purposes and does not include a specific license.
