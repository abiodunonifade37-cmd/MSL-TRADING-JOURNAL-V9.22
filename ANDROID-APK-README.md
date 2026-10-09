# MSL Trading Journal V9.2 — Corrected Android APK Builder

## Important: repository layout
Upload the **contents of this ZIP** to the repository root, preserving this structure:

- `.github/workflows/android-apk.yml`
- `package.json`
- `capacitor.config.json`
- `www/index.html`
- `www/app.js`
- `www/styles.css`
- `www/assets/icon.svg`
- other original files under `www/`

Do not upload only the ZIP. Do not put everything inside an extra parent folder.

## Build on GitHub using your phone
1. Create/open the GitHub repository and select the `main` branch.
2. Upload/replace the package contents while preserving the layout above.
3. Commit the files.
4. Open **Actions** → **Build MSL Trading Journal Android APK**.
5. If needed, tap **Run workflow**.
6. Wait for the run to finish with a green check.
7. Open the run and download the artifact named `MSL-Trading-Journal-V9.2-Android-APK`.
8. Extract the artifact ZIP and install `app-debug.apk`.

## What changed
- Pinned Capacitor dependencies to 7.4.3 to avoid untested floating major versions.
- Removed npm cache configuration that can fail when no lockfile is present.
- Added a preflight step that reports missing root/web files clearly.
- Uses Java 21 and Node.js 22.
- Verifies Gradle wrapper exists before building.

## Supabase security
Keep using your Supabase project URL and publishable/anon key. Never add a service-role/secret key to the app or repository.
