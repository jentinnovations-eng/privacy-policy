# Adding a new app

1. Decide: does the app match the general policy in `index.html` (no analytics, ads or accounts; only data the user enters)? If yes, link to `index.html`. If it collects or transmits anything else, or has no network code at all, give it its own page like `forge.html`.
2. Copy `forge.html` to `<appname>.html`. Rewrite every section from the app's **actual** behavior. Check the code, not memory: SDKs, network calls, crash reporters, purchases, permissions.
3. The policy must match the App Store privacy "nutrition label" and Google Play Data Safety form exactly. A mismatch is the most common way small studios get into trouble.
4. Add the app to `apps.html`.
5. Add a dated entry to `CHANGELOG.md`.
6. Put the page URL in App Store Connect / Play Console and inside the app.
7. If the app later adds a feature that changes data handling (sync, analytics, accounts, ads), update the policy **before** that version ships.
