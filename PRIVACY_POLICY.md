# Privacy policy for Orbital — Premium Tab Manager

Updated October 22, 2026.

This policy describes the currently published Chrome Web Store version **1.12**. Version **1.13** is prepared but has not yet been published; its changes are described separately below. Orbital has no developer-operated data backend or analytics service.

## Tab information and saved data

Orbital reads the URLs, titles, favicons, pin state, and other browser-provided metadata of open tabs for search, grouping, navigation, sleeping, and session management. It does not read page content, passwords, form entries, or keystrokes through a content script.

Saved sessions contain the name you enter, complete tab URLs, titles, pin settings, and a creation date. Stars store complete URLs. These records remain locally until you delete the session or unstar the URL. Full URLs can contain sensitive query strings or fragments. Sleeping-tab IDs, tab-activity timestamps, the current view, and onboarding state are also kept locally.

Orbital does not transmit saved sessions, starred URLs, or tab-management records to the developer or sync those records through its own code. Favicon requests are an exception to purely local tab display and are explained below.

## Active browsing time

In version 1.12, active-time recording starts in the background by default, including before you open the Time view. It records the active site's domain and seconds of activity while a browser window has focus. Idle/lock events pause recording after the system's inactivity threshold. Orbital records domains, not URL paths or page content, in the time-history series.

Time data is stored locally in minute buckets for approximately six hours, half-hour buckets for approximately 32 days, and daily domain totals indefinitely. In version 1.12 there is no recording-off setting. You may delete one site's history or use Clear all in the Time view; new activity can be recorded afterward. Version 1.13 adds a recording toggle, retention controls, and a fix for a background-write race that could restore pre-deletion history.

## Preferences, activation, and Chrome sync

Custom rules, sleep threshold, theme/skin, animation settings, labels, trial start, and license key/status/verification time are stored using Chrome's local and sync storage. If Chrome account sync is enabled, Google can carry sync data between your signed-in browsers. Custom rule text may contain sites or keywords you enter. The developer does not receive Chrome sync data.

Sessions, starred URLs, and time history are local in this package. Chrome sync and its account controls are provided by Google, under [Google's privacy policy](https://policies.google.com/privacy).

## Network requests and third parties

### Site icons in version 1.12

Tab lists may load the browser-provided favicon URL directly. Those URLs can point to arbitrary site/CDN origins and can use HTTP or HTTPS. Their requests include the favicon URL's path/query and normal connection metadata; HTTP requests can be visible to the network. They are not limited to Google's service.

The Time view also requests icons from Google's public favicon service using displayed domains, including historical domains whose tabs may no longer be open. This sends the domain, not Orbital's time totals or the original page's URL path. Google and other icon destinations may observe connection metadata such as IP address and request timing. Normal browser cookie/referrer handling can depend on browser settings.

### Gumroad license verification

When you activate Pro, Orbital sends your license key and the public product identifier to `https://api.gumroad.com/v2/licenses/verify` to verify the purchase and refund/chargeback status. A saved key can be rechecked after 14 days when Orbital opens. The request does not ask Gumroad to increment the key's usage counter.

The extension does not send browsing history, saved sessions, page content, account passwords, or payment-card details in this verification request. Gumroad receives the key and normal network metadata. Checkout and Gumroad's own purchase records are governed by [Gumroad's privacy policy](https://gumroad.com/privacy). The extension stores activation state rather than a complete purchase response, and does not log license keys or purchase responses.

## Use, retention, and deletion

Data is used for tab management, session restore, active-time history, preferences, trial status, and purchase activation. Orbital does not sell browsing data or use it for advertising. The developer does not operate a server that receives the extension's local tab/time data.

Use the session delete buttons, unstar controls, and Time-view deletion controls for their corresponding records. Uninstalling removes the extension's local storage. Chrome sync and data on other devices are controlled separately by Chrome; clearing local history is not a general account-wide deletion request. People with access to your browser profile may be able to read locally stored URLs/history or activation credentials.

Orbital's use of information obtained through Chrome APIs is limited to the features described here, consistent with the Chrome Web Store User Data Policy and its Limited Use requirements.

## Permissions

| Permission | Why it is used |
|---|---|
| `tabs` | Search, display, navigate, sleep, and manage open tabs |
| `storage` | Keep local data and sync selected preferences/activation |
| `alarms` | Run sleep checks and time-history flushes |
| `idle` | Detect inactivity for time recording |
| Gumroad HTTPS API host | Verify a Pro key |

Orbital has no content scripts or page-content scraping feature.

## Upcoming version 1.13

These changes apply after the 1.13 extension update is published, not merely because this policy page has been updated:

- Replace direct/Google favicon requests with Chrome's local favicon cache, using the additional `favicon` permission. Ordinary browsing by Chrome may still fetch icons independently of Orbital.
- Add a recording toggle that keeps existing history when switched off.
- Add daily-history retention choices of 30 days, 90 days, one year, or until deleted. Selecting a shorter period deletes older history.
- Add a device-local activation option. Turning activation sync off keeps local paid access and attempts to remove synced credentials; failures are reported so removal can be retried. Other devices keep their local activation, and Google's storage/backups remain subject to Google's policies.
- Store a coherent activation record to reconcile stale sync data, preserve access through temporary verification failures, and retain recoverable keys. A confirmed refund/chargeback can still deactivate its key.
- Restrict storage access to trusted extension contexts and serialize history deletion with background writes.

Default recording, indefinite daily-history retention, existing activation sync, saved data, original trial starts, and one-time lifetime purchases are preserved. Version 1.13 introduces no recurring subscription or new developer backend.

## Contact and changes

Questions: [kingofthecipher@gmail.com](mailto:kingofthecipher@gmail.com). Material changes will be explained in the extension and public policy when they take effect. Orbital is not directed at children.
