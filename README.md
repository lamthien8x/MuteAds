<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds logo">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Silence ads and trackers across your phone, computer, and browser.<br>One switch, five flexible filter levels, zero accounts, 100% on-device.
</p>

<p align="center">
  <b>English</b> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Why we built MuteAds

Like you, we grew tired of the modern internet: flashy banners screaming for attention, invasive tracker scripts recording every click, battery draining in the background, and bloated ad blockers that slow down your machine or sell out to advertisers. We built MuteAds with a single, uncompromising goal: cut ads and trackers off at the root by refusing connections to their domains before they even touch your screen.

No root required. No account or sign-up. And most importantly: **not a single byte of your browsing activity ever leaves your device**. Everything is resolved right where it belongs: locally on your hardware.

- **Domain-level blocking that just works**: Blocks ads and creepy analytics across every single app on your system (Android, desktop) or right inside your favorite browser (extension).
- **5 tailored filter levels**: From "Basic" (super safe, won't break client portals or work sites) to "Maximum" (rock-solid privacy shield). Level 3 is our carefully tuned default.
- **Built-in YouTube ad blocking**: Preloaded in the browser extension. Flip the switch and watch videos without jarring interruptions.
- **Single master switch**: Life is already complicated enough. Need to temporarily bypass filtering for testing? One tap turns it off; flip it back when you're done.
- **Modern encrypted DNS**: Full native support for DNS-over-HTTPS (DoH) and DNS-over-TLS (DoT) on Android and desktop to keep local snoops and ISPs out of your queries.
- **Total rule ownership**: Full support for custom allowlists, blocklists, and direct IP overrides with wildcard `*` matching.

## Downloads & Early Access

> MuteAds is currently in early release (v0.1). We are actively polishing the builds and preparing official store submissions. In the meantime, direct installers are available immediately on the [Releases](../../releases) page.

| Platform | How it works under the hood | Status |
| --- | --- | --- |
| **Android** | Local loopback VPN filtering DNS on-device. No root. Android 4.2+ | Direct APK on [Releases](../../releases) |
| **Windows** | System-wide local DNS filter service (x64, ARM64) | Available on [Releases](../../releases) |
| **macOS** | System-wide local DNS resolver filter | Available on [Releases](../../releases) |
| **Linux** | Standalone DNS proxy for your workstation or whole home LAN (requires Java) | Available on [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Lightweight MV3 browser extension using high-performance rules | Store review in preparation |
| **Firefox 128+** | Fast declarative browser extension | Store review in preparation |

## Filter Levels

| Level | Profile | What gets blocked |
| --- | --- | --- |
| 1 | Basic | Strictly the highest-priority ad and tracking networks. Minimal risk of false positives. |
| 2 | Balanced | Broader coverage including common analytics and telemetry platforms. |
| 3 | Extended | Comprehensive blocking for daily browsing. **Default sweet spot.** |
| 4 | Strict | Aggressive filtering. May occasionally interfere with third-party embed widgets. |
| 5 | Maximum | The full blocklist excluding essential social networks. Some complex pages may need whitelisting. |

💡 **Dev tip:** If a site misbehaves or refuses to load a necessary widget, simply bump the filter down a notch or flick the switch off for a moment.

## How it works (No black magic!)

Every time an application or web page wants to fetch an asset, it must first ask for the IP address behind a domain name (via DNS). MuteAds acts as your local gatekeeper:

- If the domain belongs to a known ad network, telemetric tracker, or spyware host, MuteAds immediately answers: *"Non-existent (NXDOMAIN)"*. The connection never happens, saving bandwidth and processor cycles.
- If it's genuine content you actually requested, the query passes smoothly to your chosen upstream DNS server, loading instantly as expected.

On Android, this is accomplished via a **local loopback VPN** that never routes your traffic outside your phone. On desktop, MuteAds configures itself as your computer's local DNS resolver. In browsers, the extension utilizes the native, lightning-fast `declarativeNetRequest` engine.

## Privacy: We don't want your data

- **No accounts, no email, no tracking**: We literally have no sign-up forms and no central user database.
- **Zero cloud logging**: Filtering runs locally on your machine. We operate zero servers that see or log the websites you visit.
- **Clean updates**: The only outbound network activity initiated by the app is fetching updated domain blocklists roughly once a week.
- **Minimal permissions**: The browser extension requests only what is strictly required to block network requests, persist your local settings, manage the weekly update alarm, and inject rules on `youtube.com`.

## Good to know & Pro tips

- **Android users:** Be sure to disable *Private DNS* in your phone's Android network settings, otherwise the operating system will bypass local VPN filters. Also exclude MuteAds from aggressive battery savers.
- **First-party ads:** Pure DNS filtering cannot strip ads served directly from the same domain as the content (e.g. within certain proprietary mobile apps). That is why our browser extension features a dedicated content-level engine for YouTube.
- **The YouTube cat-and-mouse game:** Video platforms tweak their ad delivery scripts regularly. If an ad ever manages to slip through, make sure you are running the latest version of the extension.

## Feedback & Community

Spotted a broken webpage or a rogue ad that snuck past the filter? Please open an [Issue](../../issues) with the page URL and the filter level you had active. We read every report and genuinely appreciate your help making MuteAds better!

## License & Acknowledgements

The Android app and standalone DNS proxy are built upon the outstanding open-source foundation of [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) by Ingo Zenz, released under the GNU General Public License v2 or later. MuteAds is distributed without warranty in the spirit of open, user-first software.
