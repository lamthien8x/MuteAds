<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo ng MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Patahimikin ang mga ad at tracker sa iyong telepono, kompyuter, at browser.<br>Isang switch, limang antas ng filter, walang account, 100% lokal sa iyong aparato.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <b>Filipino</b>
</p>

---

## Bakit namin binuo ang MuteAds

Tulad mo, sawang-sawa na kami sa modernong internet: kumikislap na banner ad kahit saan, mga tracker script na nagmamasid sa bawat pindot, bateryang mabilis maubos, at mabibigat na ad blocker na nagpapabagal sa system o nagbebenta ng datos ng mga gumagamit. Binuo namin ang MuteAds na may iisang malinaw na layunin: putulin ang mga ad at tracker sa mismong ugat sa pamamagitan ng pagtanggi sa koneksyon sa kanilang mga domain bago pa man umabot sa iyong screen.

Hindi kailangan ng root. Walang account o pagpaparehistro. At higit sa lahat: **walang kahit isang byte ng iyong browsing history ang lumalabas sa iyong aparato**. Ang lahat ng pagsasala ay 100% lokal na nagaganap sa iyong sariling hardware.

- **Mabisang pagharang sa antas ng domain**: Gumagana sa lahat ng app sa iyong system (Android, desktop) o direkta sa loob ng iyong paboritong browser (ekstensyon).
- **5 angkop na antas ng filter**: Mula "Pangunahin" (sobrang ligtas, hindi sumisira sa mga portal sa trabaho) hanggang "Pinakamataas". Ang Antas 3 ang aming balanseng default.
- **May kasamang pangharang sa ad ng YouTube**: Nakapaloob na sa browser extension. Buksan lang ang switch at manood ng mga video nang walang nakakainis na patalastas.
- **Isang pangunahing switch**: Masalimuot na ang buhay. Kailangan bang pansamantalang patayin ang filter para subukan ang isang site? Isang pindot lang at babalik agad sa normal ang lahat.
- **Makabagong naka-encrypt na DNS**: Buong suporta para sa DNS-over-HTTPS (DoH) at DNS-over-TLS (DoT) sa Android at desktop upang protektahan ka sa mga ISP.
- **Ganap na kontrol sa mga patakaran**: Suporta para sa sariling allowlist, blocklist, at custom IP mapping gamit ang wildcard na `*`.

## Mga Pag-download at Katayuan

> Ang MuteAds ay kasalukuyang nasa maagang bersyon (v0.1). Kami ay aktibong naghahanda para sa mga opisyal na tindahan ng app. Samantala, ang mga installer ay direktang makukuha sa pahina ng [Releases](../../releases).

| Platform | Paano gumagana sa loob | Katayuan |
| --- | --- | --- |
| **Android** | Lokal na loopback VPN na sumasala ng DNS sa aparato. Walang root. Android 4.2+ | APK sa [Releases](../../releases) |
| **Windows** | Lokal na serbisyo ng DNS filter para sa buong PC (x64, ARM64) | Makukuha sa [Releases](../../releases) |
| **macOS** | Lokal na DNS filter para sa buong Mac system | Makukuha sa [Releases](../../releases) |
| **Linux** | Standalone na DNS proxy para sa isang PC o buong home network (kailangan ng Java) | Makukuha sa [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Magaan at napakabilis na MV3 browser extension | Inihahanda para sa store review |
| **Firefox 128+** | Mabilis at modernong browser extension | Inihahanda para sa add-on review |

## Mga Antas ng Filter

| Antas | Pangalan | Ano ang hinaharang |
| --- | --- | --- |
| 1 | Pangunahin (Basic) | Ang mga domain ng ad at tracker na may pinakamataas na priyoridad lamang. Halos walang maling pagharang. |
| 2 | Balansado (Balanced) | Mas malawak na saklaw kasama ang karaniwang analytics at telemetry. |
| 3 | Pinalawak (Extended) | Komprehensibong proteksyon para sa pang-araw-araw na pag-browse. **Inirerekomendang default.** |
| 4 | Mahigpit (Strict) | Agresibong pagsasala. Maaaring makaapekto minsan sa ilang third-party embedded widget. |
| 5 | Pinakamataas (Maximum) | Ipinapatupad ang buong listahan ng harang (maliban sa mga pangunahing social network). Ang ilang masalimuot na site ay maaaring mangailangan ng pagbubukod. |

💡 **Payo mula sa developer:** Kung hindi maayos ang pag-load ng isang website, ibaba lang ang filter nang isang antas o patayin ang switch sandali.

## Paano ito gumagana (Walang itim na mahika!)

Sa bawat oras na nais mag-load ng isang app o webpage, una nitong itinatanong ang IP address ng domain name (sa pamamagitan ng DNS query). Ang MuteAds ang tumatayong lokal mong bantay-pinto:

- Kung ang domain ay kabilang sa network ng ad o tracker, agad na sumasagot ang MuteAds: *"Hindi umiiral (NXDOMAIN)"*. Hindi kailanman naitatag ang koneksyon, kaya nakakatipid ng data at baterya.
- Kung ito ay lehitimong nilalaman na gusto mong makita, maayos na ipinapasa ang query sa karaniwang DNS server at maglo-load ang pahina nang buong bilis.

Sa Android, ginagawa ito sa pamamagitan ng isang **lokal na loopback VPN** na hindi nagpapadala ng trapiko sa labas ng iyong telepono. Sa PC, ang app ay nagiging lokal na DNS resolver. Sa browser, ginagamit ng extension ang opisyal na napakabilis na engine na `declarativeNetRequest`.

## Privacy ang una: Ayaw namin sa iyong datos

- **Walang account, walang pag-login**: Wala kaming form sa pagpaparehistro at walang sentral na database ng gumagamit.
- **100% sa iyong aparato**: Ang pagsasala ay lokal na tumatakbo. Wala kaming mga server na nagmamasid sa mga binibisita mong site.
- **Malinis na update**: Ang tanging awtomatikong aktibidad sa network ay ang pag-download ng mga na-update na listahan ng domain halos linggu-linggo.
- **Kaunting pahintulot lamang**: Hinihiling lamang ng extension ang mga pahintulot na talagang kailangan para harangan ang mga kahilingan, i-save ang mga setting, at asikasuhin ang `youtube.com`.

## Mabuting malaman

- **Para sa mga gumagamit ng Android:** Tiyaking i-off ang *Private DNS* sa mga setting ng network ng iyong telepono, kundi ay lalampasan ng Android ang lokal na filter. Huwag ding kalimutang i-off ang battery optimization para sa MuteAds.
- **Mga ad mula sa parehong domain:** Ang purong DNS filtering ay hindi makakatanggal ng mga ad na nagmumula sa parehong domain ng pangunahing nilalaman. Kaya ang aming browser extension ay may nakalaang module para sa YouTube.
- **Laro ng pusa at daga sa YouTube:** Madalas baguhin ng mga platform ng video ang kanilang paraan ng paghahatid ng ad. Kung may lumusot na patalastas, tiyaking na-update mo ang extension sa pinakabagong bersyon.

## Feedback at Komunidad

May nakitang sirang pahina o makulit na ad na nakalusot? Magbukas ng [Issue](../../issues) kalakip ang address ng pahina at antas ng filter na gamit mo. Ang bawat tulong mo ay lubos naming pinahahalagahan!

## Lisensya at Pasasalamat

Ang Android app at standalone DNS proxy ay binuo mula sa kahanga-hangang open-source na proyektong [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) ni Ingo Zenz, inilabas sa ilalim ng GNU General Public License v2 o mas bago. Buong pusong ibinabahagi para sa mas malinis na internet.
