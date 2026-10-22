# Orbital — Premium Tab Manager

Search, group, sleep, and manage your tabs in one place. Orbital maps windows, groups, and tabs as a solar system, saves sessions, protects starred tabs, and shows active browsing time by site.

**Current Chrome Web Store version: 1.12.** Version 1.13 is prepared and tested, but has not yet been published. This repository provides product information, privacy details, support, and release notes; it does not distribute the application source.

## Installation

[Install Orbital from the Chrome Web Store](https://chromewebstore.google.com/detail/opkpmahpmiecgcojolbmigjeojkaemod).

Install the extension, then click Orbital's icon in Chrome's toolbar. Pin the icon for easy access. The published package uses a seven-day Pro trial; the store's older three-day description is being corrected with the next update.

## Pricing

Try Pro for seven days with no credit card required. After the trial, unlock Pro for life with a **one-time $9.99 purchase**, not a recurring subscription.

[Purchase Orbital Pro through Gumroad](https://gumroad.com/l/rjxed). Paste the license key into Orbital's settings and select Activate. Existing lifetime licenses and trial start dates are preserved in the prepared 1.13 update.

## Features

- **Orbits:** visualize every window, group, and tab as a solar system.
- **Search:** find an open tab by its title or URL.
- **Groups and windows:** organize tabs by category, custom rule, or window.
- **Tab sleeping:** discard inactive tabs to reduce memory use and wake them when needed.
- **Saved sessions:** save tabs and restore their URLs and pin state later.
- **Starred tabs:** protect important tabs from group/window close actions.
- **Time history:** view active time per domain across several date ranges.
- **Appearance:** light/dark and glass/solid styles, orbit controls, and full-screen mode.

## How to use

1. Open Orbital from the toolbar.
2. Search or choose All, Orbits, Groups, Windows, Time, or Sleeping.
3. Use the tab/group/window controls to navigate, sleep, merge, or close tabs.
4. Open Settings to manage custom rules, save sessions, adjust sleep timing, or activate Pro.

The prepared 1.13 update also adds settings to pause recording, choose daily-history retention, and keep activation local to a device. Those controls become available when 1.13 is published.

## Privacy and permissions

Orbital stores tab-management data and time history in the browser. Preferences and activation credentials can use Chrome sync; license verification contacts Gumroad. The live 1.12 version also makes favicon requests to site-provided icon URLs and Google's favicon service. The upcoming 1.13 version replaces those requests with Chrome's local favicon cache.

[Read the full privacy policy](PRIVACY_POLICY.md). The policy distinguishes the currently published behavior from the upcoming changes.

| Permission | Purpose |
|---|---|
| `tabs` | Read open-tab titles/URLs and manage tabs |
| `storage` | Keep sessions, history, preferences, rules, and activation |
| `alarms` | Schedule sleep checks and history flushes |
| `idle` | Pause time recording when the system is inactive |
| `https://api.gumroad.com/*` | Verify a Pro license over HTTPS |
| `favicon` — upcoming 1.13 | Read Chrome's local favicon cache |

There are no content scripts or page-content scraping features.

## Support

- [Report a bug or request a feature](https://github.com/kingofthecipher-ctrl/orbital/issues).
- Contact: [kingofthecipher@gmail.com](mailto:kingofthecipher@gmail.com).
- If activation verification is temporarily unavailable, try again later. Version 1.13 includes fixes that preserve existing access during these failures and stale-sync conflicts.
- Saved data belongs to the browser profile where Orbital is installed. Avoid clearing extension storage or uninstalling if you need to retain locally saved sessions/history.

## Version history

[Patch notes for the upcoming 1.13 update](PATCH_NOTES.md) · [Changelog](CHANGELOG.md).

The Chrome Web Store listing is the installation source. This repository's upcoming release notes do not mean a store update has already shipped.
