<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds logo">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Block ads and trackers on your phone, your computer and your browser.<br>
  One switch, five filter levels, no account.
</p>

<p align="center">
  <b>English</b> · <a href="README.vi.md">Tiếng Việt</a>
</p>

---

## What it does

MuteAds stops ads and trackers by refusing to connect to the domains that serve them. It does not need root, does not need an account, and does not send your browsing history anywhere: filtering happens on your own device.

- **Blocks ads and trackers by domain**, across every app on the device (Android, desktop) or inside the browser (extension).
- **Five filter levels**, from "Basic" (fewest false positives) to "Maximum" (blocks the most, some pages may break). The default is level 3.
- **YouTube ad blocking** in the browser extension, active as soon as the switch is on.
- **One switch.** Turn it off and everything goes back to normal.
- **Encrypted DNS** upstream: DNS-over-HTTPS and DNS-over-TLS are supported on Android and desktop.
- **Your own rules**: allowlist, blocklist and custom IP mappings, with `*` wildcards.

## Download

> MuteAds is in early release (version 0.1). Installers are published on the [Releases](../../releases) page as they become ready. Store listings are in preparation.

| Platform | How it works | Status |
| --- | --- | --- |
| **Android** | Local VPN that filters DNS on the device. No root. Android 4.2+ | APK on [Releases](../../releases) |
| **Windows** | Local DNS filter for the whole computer (x64, ARM64) | On [Releases](../../releases) |
| **macOS** | Local DNS filter for the whole computer | On [Releases](../../releases) |
| **Linux** | DNS proxy for one machine or the whole network (requires Java) | On [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Browser extension | Store listing in preparation |
| **Firefox** 128+ | Browser extension | Store listing in preparation |

## Filter levels

| Level | Name | What it blocks |
| --- | --- | --- |
| 1 | Basic | Highest-priority domains only. Least likely to block something by mistake. |
| 2 | Balanced | Wider coverage. |
| 3 | Extended | Broad coverage. **Default.** |
| 4 | Strict | Very broad. May start to block things by mistake. |
| 5 | Maximum | The whole list except social networks. Some pages may not display correctly. |

If a site stops working, lower the level or turn the switch off for a moment.

## How it works

Every time an app or a page wants to load something, it first asks for the address of a domain name. MuteAds answers that question itself:

- If the domain is on the block list, MuteAds answers "nowhere" and the ad or tracker never loads.
- Otherwise the question is passed on to a normal DNS server and the page loads as usual.

On Android this runs through a local VPN that stays on the device; no traffic is sent to a MuteAds server. On desktop the app becomes the DNS server of your computer. The browser extension uses the browser's built-in blocking API (`declarativeNetRequest`) with the same list.

## Privacy

- No account and no sign-up.
- Filtering runs on your device. MuteAds has no server that sees the sites you visit.
- The only download the apps make on their own is the block list, refreshed about once a week.
- The browser extension asks only for the permissions it uses: blocking requests, saving your settings, a weekly refresh timer, and access to `youtube.com` for YouTube ad blocking.

## Good to know

- **Android:** turn off *Private DNS* in the network settings, otherwise the filter is bypassed. Allow the app to run in the background without battery optimisation.
- Domain-based blocking cannot remove ads that are served from the same domain as the content itself (for example inside some mobile apps). The browser extension handles YouTube separately for that reason.
- YouTube changes often. If ads come back, update to the latest version.

## Feedback

Found a site that breaks, or an ad that gets through? Open an [issue](../../issues) with the address of the page and the filter level you were using.

## License

The Android app and the standalone DNS proxy are based on [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) and are released under the GNU General Public License, version 2 or later. The program comes with no warranty.
