# sed.i Safari Extension

Save articles to [sed.i](https://www.read-sedi.com) with one click from Safari on macOS.

## Install from release

1. Download `sed.i.app.zip` from the [latest release](../../releases/latest)
2. Unzip and move `sed.i.app` to `/Applications`
3. Open `sed.i.app` once — this registers the extension with Safari
4. Go to **Safari → Settings → Extensions**, find **sed.i**, and enable it
5. If macOS blocks the app with a Gatekeeper warning, run once in Terminal:
   ```
   xattr -rd com.apple.quarantine /Applications/sed.i.app
   ```
   Then open the app again.

## Build from source

Requirements: macOS 13+, Xcode 15+

```bash
git clone https://github.com/enpuyou/sedi-safari.git
open sed.i/sed.i.xcodeproj
```

Select the **sed.i** scheme, choose **My Mac** as the destination, and press **⌘B** to build. Run once to register the extension.

## Keeping the extension up to date

The extension JS is synced from the main [sed.i repo](https://github.com/enpuyou/content-queue) via `make safari-sync`. When a new release is cut here, download the updated `.app` and repeat step 3–4 above.

## Requirements

- macOS 13 Ventura or later
- Safari 16 or later
- A [sed.i](https://www.read-sedi.com) account
