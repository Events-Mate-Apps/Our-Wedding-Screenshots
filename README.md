# Our-Wedding-Screenshots

Unified screenshot gallery for **Events Mate** — iOS and Web marketing screenshots.

Published automatically via GitHub Pages at: https://events-mate-apps.github.io/Our-Wedding-Screenshots/

The gallery (`index.html`) reads the repository tree at runtime via the GitHub API,
so any newly pushed screenshots that follow the naming convention show up
automatically — no manual edits required.

## Structure

```
├── ios/                          # iOS screenshots (Fastlane snapshot + frameit)
│   ├── raw/{locale}/             # Raw XCUITest captures
│   ├── framed/{locale}/          # Device-framed (with background)
│   └── framed_nobg/{locale}/     # Device-framed (transparent background)
├── web/                          # Web screenshots (Playwright + framing)
│   ├── raw/{locale}/{viewport}/
│   └── framed/{locale}/{viewport}/
├── index.html                    # GitHub Pages gallery (dynamic)
└── README.md
```

## iOS naming convention

```
{Device}-{NN}_{Screen_Name}[_landscape][_dark][_framed].png
```

- `{Device}`: e.g. `iPhone_17_Pro_Max`, `iPhone_17_Pro`, `iPad_Pro_13-inch_M4`
- `_landscape`: present on iPad shots
- `_dark`: dark-mode variant (omitted ⇒ light mode)
- `_framed`: present in `framed/` and `framed_nobg/`, absent in `raw/`

Both light and dark variants are produced for **raw**, **framed**, and **framed_nobg**.

## Web naming convention

```
{NN}-{slug}[_framed].png
```

Stored under `web/{style}/{locale}/{viewport}/`, where `viewport` is one of
`mobile`, `tablet`, or `desktop`.

## Locales

| Code  | Language      | iOS | Web |
|-------|---------------|-----|-----|
| en-US | English (US)  | ✅  |     |
| en-GB | English (UK)  | ✅  |     |
| en    | English       |     | ✅  |
| de-DE | German        | ✅  |     |
| de    | German        |     | ✅  |
| es-ES | Spanish       | ✅  |     |
| ca    | Catalan       | ✅  |     |
| cs    | Czech         | ✅  | ✅  |
| sk    | Slovak        | ✅  | ✅  |

## iOS devices
- iPhone 17 Pro Max (6.9")
- iPhone 17 Pro (6.3")
- iPad Pro 13-inch (M4)

## Web viewports
- Desktop (1440×900)
- Tablet (768×1024)
- Mobile (375×812)

## Publishing

- **iOS:** Fastlane `publish_screenshots` lane in [our-wedding-ios](https://github.com/Events-Mate-Apps/our-wedding-ios)
- **Web:** GitHub Action / script in [our-wedding-web](https://github.com/Events-Mate-Apps/our-wedding-web)
