# Our-Wedding-Screenshots

Unified screenshot gallery for **Events Mate** — iOS and Web marketing screenshots.

Published automatically via GitHub Pages at: https://events-mate-apps.github.io/Our-Wedding-Screenshots/

## Structure

```
├── ios/                  # iOS screenshots (via Fastlane snapshot + frameit)
│   ├── raw/              # Raw XCUITest captures
│   └── framed/           # Device-framed marketing screenshots
│       └── {locale}/{device}/*.png
├── web/                  # Web screenshots (via Playwright + framing script)
│   ├── raw/              # Raw Playwright captures
│   └── framed/           # Device-framed marketing screenshots
│       └── {locale}/{device}/*.png
├── index.html            # GitHub Pages gallery
└── README.md
```

## Locales

| Code  | Language |
|-------|----------|
| en-US | English (US) |
| en-GB | English (UK) |
| de-DE | German |
| es-ES | Spanish |
| cs    | Czech |
| sk    | Slovak |
| ca    | Catalan |

## iOS Devices
- iPhone 16 Pro Max (6.9")
- iPhone 16 Pro (6.3")  
- iPhone SE (4.7")

## Web Viewports
- Desktop (1440×900)
- Tablet (768×1024)
- Mobile (375×812)

## Publishing

- **iOS:** Fastlane `publish_screenshots` lane in [our-wedding-ios](https://github.com/Events-Mate-Apps/our-wedding-ios)
- **Web:** GitHub Action / script in [our-wedding-web](https://github.com/Events-Mate-Apps/our-wedding-web)

