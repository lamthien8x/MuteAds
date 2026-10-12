<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds logó">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Némítsd el a hirdetéseket és nyomkövetőket telefonodon, számítógépeden és böngésződben.<br>Egyetlen kapcsoló, öt szűrési szint, nincs fiók, 100% helyi működés.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <b>Magyar</b> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Miért készítettük el a MuteAds-ot?

Hozzád hasonlóan nekünk is elegünk lett a mai internetből: villogó reklámbannerek mindenhol, nyomkövető szkriptek, amelyek minden kattintást naplóznak, gyorsan merülő akkumulátor és lomha reklámblokkolók, amelyek lelassítják a gépet vagy eladják a felhasználói adatokat. A MuteAds-ot egyetlen tiszta céllal hoztuk létre: a hirdetések és nyomkövetők gyökerénél elvágni a kapcsolatot, megtagadva a doménjeikhez fűződő hozzáférést még mielőtt elérnék a képernyőt.

Nincs szükség root jogokra. Nincs regisztráció vagy fiókkészítés. És ami a legfontosabb: **a böngészési előzményeidből egyetlen bájt sem hagyja el az eszközödet**. Minden szűrés 100%-ban helyben, a saját hardvereden történik.

- **Hatékony doménszintű blokkolás**: Működik a rendszer összes alkalmazásában (Android, asztali gép) vagy közvetlenül a kedvenc böngésződben (bővítmény).
- **5 testreszabott szűrési szint**: Az „Alap” szinttől (nagyon biztonságos, nem rontja el a munkahelyi oldalakat) a „Maximális” szintig (sziklaszilárd adatvédelem). A 3. szint a finomhangolt alapértelmezett.
- **Beépített YouTube reklámblokkolás**: Közvetlenül a böngészőbővítménybe építve. Kapcsold be a kapcsolót, és élvezd a videókat megszakítások nélkül.
- **Egyetlen főkapcsoló**: Az élet már amúgy is elég bonyolult. Ideiglenesen ki kell kapcsolnod a szűrést egy oldal teszteléséhez? Egy kattintás, és minden azonnal visszaáll a régibe.
- **Korszerű titkosított DNS**: Teljes körű DNS-over-HTTPS (DoH) és DNS-over-TLS (DoT) támogatás Androidon és asztali gépen a szolgáltatók kíváncsiskodása ellen.
- **Saját szabályok teljes irányítása**: Egyéni engedélyezési listák (allowlist), tiltólisták (blocklist) és egyéni IP-hozzárendelések támogatása `*` helyettesítő karakterekkel.

## Letöltések és Állapot

> A MuteAds jelenleg korai kiadási fázisban van (v0.1). Gőzerővel dolgozunk a hivatalos áruházi megjelenéseken. Addig is a közvetlen telepítők elérhetők a [Releases](../../releases) oldalon.

| Platform | Belső működés | Állapot |
| --- | --- | --- |
| **Android** | Helyi loopback VPN, amely magán az eszközön szűri a DNS-t. Root nélkül. Android 4.2+ | APK a [Releases](../../releases) oldalon |
| **Windows** | Helyi DNS-szűrő szolgáltatás az egész számítógépre (x64, ARM64) | Elérhető a [Releases](../../releases) oldalon |
| **macOS** | Helyi rendszerszintű DNS-szűrő Macre | Elérhető a [Releases](../../releases) oldalon |
| **Linux** | Önálló DNS-proxy egy gépre vagy az egész otthoni hálózatra (Java szükséges) | Elérhető a [Releases](../../releases) oldalon |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Könnyű és villámgyors MV3 böngészőbővítmény | Áruházi elbírálás előkészületben |
| **Firefox 128+** | Gyors deklaratív böngészőbővítmény | Kiegészítő elbírálás előkészületben |

## Szűrési szintek

| Szint | Profil | Mit blokkol |
| --- | --- | --- |
| 1 | Alap (Basic) | Kizárólag a legmagasabb prioritású reklám- és nyomkövető szervereket. Minimális téves riasztás. |
| 2 | Kiegyensúlyozott (Balanced) | Szélesebb lefedettség, beleértve a gyakori analitikai és telemetriai platformokat. |
| 3 | Kiterjesztett (Extended) | Átfogó védelem a mindennapi böngészéshez. **Ajánlott alapértelmezett.** |
| 4 | Szigorú (Strict) | Agresszív szűrés. Alkalmanként befolyásolhatja a beágyazott külső widgeteket. |
| 5 | Maximális (Maximum) | A teljes tiltólistát alkalmazza (a főbb közösségi oldalak kivételével). Egyes összetett oldalak kivételt igényelhetnek. |

💡 **Fejlesztői tipp:** Ha egy weboldal nem töltődik be rendesen, egyszerűen vedd lejjebb a szűrést egy szinttel, vagy kapcsold ki a gombot egy pillanatra.

## Hogyan működik (Nincs fekete mágia!)

Amikor egy alkalmazás vagy weboldal le akar tölteni valamit, először lekérdezi a doménnév mögötti IP-címet (DNS-kérésen keresztül). A MuteAds a saját helyi kapuőrödként lép fel:

- Ha a domén reklám- vagy nyomkövető hálózathoz tartozik, a MuteAds azonnal válaszol: *„Nem létezik (NXDOMAIN)”*. A kapcsolat létre sem jön, ami adatforgalmat és akkumulátort takarít meg.
- Ha valós, általad kért tartalomról van szó, a kérés zökkenőmentesen továbbítódik a szokásos felsőbb DNS-kiszolgálóhoz, és az oldal villámgyorsan betöltődik.

Androidon ez egy **helyi loopback VPN**-en keresztül fut, amely soha nem küld adatot a telefonon kívülre. Számítógépen a gép helyi DNS-feloldójává válik. A böngészőben a kiegészítő a hivatalos, szélsebes `declarativeNetRequest` motort használja.

## Adatvédelem mindenekelőtt: Nem kérünk az adataidból

- **Nincs fiók, nincs bejelentkezés**: Nincsenek regisztrációs űrlapjaink és nincs központi felhasználói adatbázisunk.
- **100% az eszközödön**: A szűrés kizárólag helyben fut. Nem üzemeltetünk olyan szervereket, amelyek látnák az általad meglátogatott oldalakat.
- **Tiszta frissítések**: Az alkalmazás egyetlen önálló hálózati művelete a frissített tiltólisták letöltése nagyjából hetente egyszer.
- **Minimális jogosultságok**: A bővítmény csak a legszükségesebb engedélyeket kéri a kérések blokkolásához, beállítások mentéséhez, heti időzítőhöz és a `youtube.com` kezeléséhez.

## Jó tudni

- **Android felhasználóknak:** Feltétlenül kapcsold ki a *Privát DNS* beállítást a telefon hálózati beállításaiban, különben az Android megkerüli a helyi szűrőt. Kapcsold ki az akkumulátor-optimalizálást is a MuteAds számára.
- **Azonos doménről érkező reklámok:** A tiszta DNS-szűrés nem képes kiszűrni azokat a hirdetéseket, amelyeket magáról a tartalom saját doménjéről szolgálnak ki. Ezért tartalmaz böngészőbővítményünk külön modult a YouTube-hoz.
- **Macska-egér játék a YouTube-on:** A videóplatformok rendszeresen módosítják hirdetéskiszolgáló mechanizmusaikat. Ha egy hirdetés átcsusszan, frissítsd a bővítményt a legújabb verzióra.

## Visszajelzés és Közösség

Találtál egy hibásan betöltődő oldalt vagy egy makacs reklámot, ami átjutott? Nyiss bátran egy [Issue](../../issues) hibajegyet az oldal címével és a használt szűrési szinttel. Nagyon hálásak vagyunk minden segítségért!

## Licenc és Köszönetnyilvánítás

Az Android alkalmazás és az önálló DNS-proxy Ingo Zenz nagyszerű nyílt forráskódú [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) projektjén alapul, és a GNU General Public License v2 vagy újabb verziója alatt érhető el. Szenvedéllyel fejlesztve egy tisztább internetért.
