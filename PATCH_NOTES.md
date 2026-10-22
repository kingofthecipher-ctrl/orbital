# Orbital 1.13 — upcoming patch notes

Prepared October 22, 2026. **Not yet published to the Chrome Web Store.** The current store version is 1.12.

## Fixes

- Preserve existing paid activation during temporary license-service failures, unexpected responses, and stale Chrome sync conflicts.
- Prevent older pending history writes from restoring data after deletion.
- Support reserved custom group names and safely handle malformed saved rules.
- Keep saved-session deletion separate from custom group rules.

## Privacy controls

- Use Chrome's local favicon cache instead of requesting icons from site-provided URLs or Google's public favicon service.
- Pause time recording while retaining existing history.
- Choose daily-history retention: 30 days, 90 days, one year, or until manually deleted. Choosing a shorter period removes older time history.
- Keep activation local to a device by switching off activation sync, preserving local paid access.
- Read a fuller in-app privacy policy covering saved URLs, history, preferences, sync, and verification.

## Compatibility

Existing sessions, stars, preferences, history, trial start dates, and valid paid access are preserved. The Pro trial remains seven days and the purchase remains a one-time lifetime unlock. Recording, indefinite daily retention, and activation sync retain their existing defaults.

Confirmed refunds and chargebacks can still deactivate the affected key. No backend migration or recurring subscription is introduced.

## Validation

42 checks passed: 25 focused security tests and 17 native Chrome tests. The tested upgrade used synthetic data in a disposable profile, preserved saved data/access, and recorded zero external requests during the final tested flows. This does not replace testing the actual signed store rollout.

The store-description update will correct the older three-day text to match the seven-day implementation. These notes will be marked released after the Google/Chrome Web Store update is published.
