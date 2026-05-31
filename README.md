
## Build & Load

```bash
npm install
npm run build
```

`npm run build` runs `scripts/copy-static.js`, which cleans `dist/`, bundles the entry points with esbuild, and copies the manifest, icons, and popup markup into the output directory.

To test locally:

1. Open `chrome://extensions`
2. Enable **Developer mode**
3. Choose **Load unpacked** → select the `dist/` folder
4. Pin the extension and click it to open the website list

## Usage

1. Type a website in the popup and press **Save website**.
2. Remove saved websites anytime from the list.

## Development Notes

- Update popup UI or logic under `src/ui/popup.*`
- Saved website data is stored via `chrome.storage.local` under the `savedSites` key
- When you change anything, re-run `npm run build` and reload the unpacked extension

## License

MIT
