# Changelog

Every published build of Drift™, newest first. Versions follow `versionName` in
`app/build.gradle.kts`; the current build is **2.4** (`versionCode 16`).

## 2.4 — 9 November 2026

Branding, licence and the public face of the project.

- `LICENSE` added: copyright line, Drift™ trademark line, no open-source grant.
- Settings → **ABOUT** now shows `Drift™ 2.4`, the copyright notice and the
  trademark notice.
- Launcher and shortcut label read `Drift™`; the home wordmark and the settings
  header carry the mark.
- Public landing page published, with the same copyright footer.
- Repository README, curated screenshots, changelog and contributing notes
  written for a GitHub release.

## 2.3 — 9 November 2026

- **GLASS** theme: translucent milk-white panes with bright edges over a slowly
  drifting teal-and-violet liquid backdrop.
- Still frames of the same backdrop behind settings, drawer and search, so home
  icons never ghost through.
- Theme cycle grows to seven: AUTO → LIGHT → DARK → E-INK → SPACE → GREEN →
  GLASS.

## 2.2 — 9 November 2026

- **GREEN** theme: mint text and a vivid green accent on carbon black.
- Themes moved into their own **THEMES** section in Settings, with a palette
  swatch, description and ON marker per row.
- Controls page shows all themes in two rows; home chip cycles through them.
- Accent buttons and selected pills switch to near-black text on light accents.

## 2.1 — 9 November 2026

- **SPACE** live background: deep navy sky, two star layers drifting at
  different speeds, a slow brightness pulse and a shooting star about every
  eight seconds.
- Stars are baked into two tiles and scrolled, so a frame costs four image
  draws.
- Animation pauses while the drawer, search or settings is open and whenever
  Drift is not visible.

## 2.0 — 9 November 2026

- **E-INK** theme: warm paper page, white cards, near-black text, ink outlines
  instead of shadows, round grayscale icons and an ink-black accent.
- Animations shortened and lite mode forced on, so the theme also removes the
  expensive per-frame drawing.
- Applies to home, drawer, search, folders, settings, pickers and sheets.

## 1.9 — 9 November 2026

- **Edge lighting**: both screen edges glow for about three seconds when a
  notification arrives, in blue, red or amber.
- Optional for incoming calls, and optional overlay permission so the glow can
  appear over other apps.
- Rides the notification listener already used for unread badges.

## 1.8 — 8 November 2026

- **Double tap empty home space to turn the screen off**, using a device-admin
  receiver with only the `force-lock` policy.
- The tap watcher is passive: it never consumes touches, so swipes, icons and
  the 1.5 s hold keep working, and a drag cancels it.
- New **DOUBLE TAP** settings section with on/off, grant state and a manage
  button.

## 1.7 — 8 November 2026

- Drawer no longer recomposes the whole app list on every scrolled pixel.
- **LITE MODE** in Settings → PERFORMANCE: no shadows or gradients, half-length
  slides.
- **HZ PROBE** in Settings: panel mode, supported display modes and a
  three-second measured frame count, independent of what Drift requested.
- MAX refresh mode also sends the request at the view level for phones that
  ignore the window hint.

## 1.6 — 8 November 2026

- Three app-drawer layouts in Settings → APP DRAWER → LAYOUT:
  **GRID** (one scrolling A–Z grid with a letter scrubber), **PAGES** (fixed
  screens swiped sideways, with page dots) and **LIST** (one app per row with
  its package name).
- Recents, folders, pull-down-to-home, drawer search and the app sheet work in
  every layout; the columns setting controls icons per row and apps per page.

## 1.5.1 — 8 November 2026

- Refresh-rate fix: the **MAX** mode now pins the actual display mode with
  `preferredDisplayModeId` instead of only hinting with
  `preferredRefreshRate`.
- The mode is re-applied on resume and when the window regains focus. **60HZ**
  pins the 60 Hz mode the same way; **SMART** still leaves the choice to
  Android.

## 1.5 — 8 November 2026

- **Widgets** from any installed app on page 2, with an ADD picker and × to
  remove.
- **Icon packs** in ADW/Nova format (`assets/appfilter.xml`).
- Dock on/off, stat tiles one or two per row, and a compact home layout in
  Settings → HOME LAYOUT.

## 1.4 — 8 November 2026

- **Folders** in the drawer: hold an app → FOLDERS → NEW FOLDER.
- **RECENT** and **FOLDERS** rows at the top of the drawer.
- Sort by name or most used; hide app labels.
- System settings rows in search (`wifi`, `battery`, `alarms`…).
- **Unread badges** on app icons, fed by the notification listener.

## 1.3 — 7 November 2026

- Search inside the app drawer.
- App sheet on a 1.5 s hold: shortcuts, OPEN, APP INFO, HIDE APP, UNINSTALL.
- Hide and unhide apps, a custom dock picker, mono icons, and tap the clock for
  alarms.

## 1.2 — 7 November 2026

- Swipe down at the drawer's top row returns home; header swipe and back arrow
  still work.
- Removed the per-icon drag detector that consumed scroll movement — the main
  cause of drawer lag.
- Icon loading cache, and a high-refresh request so scrolling could use faster
  panels.

## 1.1 — 7 November 2026

- Swipe up anywhere on home (clock, cards, gap, dock) opens the drawer, with a
  48 dp threshold and support for a fast flick.
- Full settings page added alongside the side panel.
- Contrast, drawer, long-press, search and refresh-rate issues from the first
  round of testing fixed.

## 1.0 — 7 November 2026

First build: a gesture-first home screen with a large clock, pickable stat
cards, a scrolling app drawer, search, a dock and a settings panel. Built in
Kotlin and Jetpack Compose, `dev.tusk.drift`, Android 8.0+.
