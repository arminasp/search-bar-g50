# Development Instructions

## Reloading the GNOME extension

When asked to reload the extension, run these commands from the repository root:

```bash
EXTENSION_DIR="$HOME/.local/share/gnome-shell/extensions/searchbar@tiszui.asd"

cp -r extension.js metadata.json stylesheet.css schemas "$EXTENSION_DIR/"
glib-compile-schemas "$EXTENSION_DIR/schemas"
gnome-extensions disable searchbar@tiszui.asd
gnome-extensions enable searchbar@tiszui.asd
```
