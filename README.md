# Search Light 50

A lightweight Spotlight-style search bar for GNOME Shell 50. Press <kbd>Ctrl</kbd> + <kbd>Space</kbd> to search installed applications or run a web search.

<img width="590" height="350" alt="Search Light 50 search bar" src="https://github.com/user-attachments/assets/7c8749c0-1e89-43ed-8c18-7eb9491740d1">

## Features

- Opens with <kbd>Ctrl</kbd> + <kbd>Space</kbd>
- Finds installed applications by name or application ID
- Supports keyboard navigation with <kbd>↑</kbd>, <kbd>↓</kbd>, and <kbd>Enter</kbd>
- Opens a Google search when no application result is selected
- Closes with <kbd>Esc</kbd> or when it loses focus

## Requirements

- GNOME Shell 50

## Installation

From the project directory, copy the extension files into GNOME Shell's local extensions directory and compile the settings schema:

```bash
EXTENSION_DIR="$HOME/.local/share/gnome-shell/extensions/searchbar@tiszui.asd"

mkdir -p "$EXTENSION_DIR"
cp -r extension.js metadata.json stylesheet.css schemas "$EXTENSION_DIR/"
glib-compile-schemas "$EXTENSION_DIR/schemas"
```

Enable the extension:

```bash
gnome-extensions enable searchbar@tiszui.asd
```

Log out and back in if the extension does not appear or load immediately.

## Usage

1. Press <kbd>Ctrl</kbd> + <kbd>Space</kbd>.
2. Type an application name or search term.
3. Select an application using <kbd>↑</kbd>/<kbd>↓</kbd> and press <kbd>Enter</kbd> to launch it.
4. Press <kbd>Enter</kbd> without selecting an application to search the web.

The shortcut can be changed in the extension's settings through GNOME Extensions.

## Development

After making changes, copy the updated files, compile the schema, and reload the extension:

```bash
EXTENSION_DIR="$HOME/.local/share/gnome-shell/extensions/searchbar@tiszui.asd"

cp -r extension.js metadata.json stylesheet.css schemas "$EXTENSION_DIR/"
glib-compile-schemas "$EXTENSION_DIR/schemas"
gnome-extensions disable searchbar@tiszui.asd
gnome-extensions enable searchbar@tiszui.asd
```

## License

No license has been specified for this project.
