# Macros

A single-file macro and calorie tracker. Phone-first, installable to the home screen, no build step and no backend.

Log food by scanning a barcode, photographing a nutrition label, searching by name, or typing the numbers in. Everything you log is saved to a personal food library so the second time is one tap.

## Privacy

There is no account, no server, and no analytics. All data lives in your own browser's `localStorage` under the key `macrotracker.v1` and never leaves your device. The Targets tab has Export / Restore / Erase — export a backup before clearing browser data or switching phones.

The only outbound requests are to the public [Open Food Facts](https://world.openfoodfacts.org) API when you look up a barcode or search by name, and to a CDN for two libraries loaded lazily when you first use a scan feature.

## Use it

Open the site on your phone and add it to your home screen. HTTPS is required for the live camera scanner.

## Stack

No dependencies bundled, no build step. Two libraries load from CDN only when the feature is used:

- `@zxing/library` 0.21.3 — barcode fallback when the browser has no native `BarcodeDetector`
- `tesseract.js` 5.1.1 — nutrition label OCR

## License

MIT
