# app-snapshots

The full visual catalog of **every in-app screen and Compose/SwiftUI preview**,
mirrored here from each app's automated snapshot-test goldens. These are distinct
from the locale marketing screenshots in the top-level locale folders
(`en-US`, `cs`, `de-DE`, …) — those are curated App-Store assets; these are the
exhaustive per-screen regression references.

```
app-snapshots/
├── android/   # Roborazzi goldens, grouped by feature (budget, guests, onboarding, …)
└── ios/       # swift-snapshot-testing goldens, grouped by module (BudgetKit, GuestKit, …)
```

## Source of truth

The canonical goldens live in each app repo next to the tests, and CI diffs
against them on every PR:

- **Android** — `our-wedding-android` → `app/src/test/screenshots/`
  (record with `./gradlew recordRoborazziDevDebug`)
- **iOS** — `apple-single-spm` (SingleOne) → `Tests/*/__Snapshots__/`
  (recorded by the snapshot suites in record mode)

This folder is a **read-only mirror** — don't edit images here. To refresh after
re-recording, run the sync script in the relevant app repo:

```bash
# Android
tools/sync-snapshots.sh --commit
# iOS
Scripts/sync-snapshots.sh --commit
```

(The screenshots repo is found at `../../Our-Wedding-Screenshots` by default;
override with `SCREENSHOTS_REPO=/path/to/repo`.)
