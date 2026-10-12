<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds-logo">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Blokkeer advertenties en trackers op je telefoon, computer en in je browser.<br>Eén knop, vijf filterstanden, geen account, 100% lokaal op je apparaat.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <b>Nederlands</b> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Waarom we MuteAds hebben gemaakt

Net als jij waren we het moderne internet zat: knipperende reclamebanners, opdringerige trackingscripts die elke muisklik vastleggen, een snel leeglopende batterij en zware adblockers die je computer vertragen of gebruikersdata doorverkopen. We hebben MuteAds gebouwd met één helder doel: advertenties en trackers direct bij de wortel afsnijden door verbindingen met hun domeinen te weigeren voordat ze je scherm bereiken.

Geen root nodig. Geen account of registratie. En het belangrijkste van alles: **geen enkele byte van je surfgedrag verlaat ooit je apparaat**. Alle filtering vindt 100% lokaal op je eigen hardware plaats.

- **Effectieve blokkering op domeinniveau**: Werkt voor elke app op je systeem (Android, desktop) of direct binnen je favoriete webbrowser (extensie).
- **5 doordachte filterstanden**: Van „Basis“ (uiterst veilig, breekt geen werkwebsites) tot „Maximaal“ (strikt privacyschild). Stand 3 is onze gebalanceerde standaard.
- **Ingebouwde YouTube-advertentieblokkering**: Direct meegeleverd in de browserextensie. Schakel de knop in en geniet van video's zonder onderbrekingen.
- **Eén centrale aan/uit-schakelaar**: Het leven is al ingewikkeld genoeg. Wil je de filter even uitschakelen om een website te testen? Eén klik en alles werkt direct weer normaal.
- **Moderne versleutelde DNS**: Volledige ondersteuning voor DNS-over-HTTPS (DoH) en DNS-over-TLS (DoT) op Android en pc om nieuwsgierige internetproviders buiten de deur te houden.
- **Volledige controle over eigen regels**: Beheer je eigen allowlists, blocklists en aangepaste IP-toewijzingen met wildcard-ondersteuning (`*`).

## Downloads & Status

> MuteAds bevindt zich in de vroege releasefase (versie 0.1). We leggen de laatste hand aan de officiële store-vermeldingen. In de tussentijd kun je installatiebestanden direct downloaden via de pagina [Releases](../../releases).

| Platform | Onderliggende werking | Status |
| --- | --- | --- |
| **Android** | Lokale loopback-VPN die DNS op het apparaat filtert. Geen root. Android 4.2+ | APK op [Releases](../../releases) |
| **Windows** | Lokale DNS-filterservice voor de hele pc (x64, ARM64) | Beschikbaar op [Releases](../../releases) |
| **macOS** | Lokaal DNS-filter voor het hele Mac-systeem | Beschikbaar op [Releases](../../releases) |
| **Linux** | Zelfstandige DNS-proxy voor één pc of het hele thuisnetwerk (vereist Java) | Beschikbaar op [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Lichtgewicht en snelle MV3-browserextensie | Voorbereiding voor Chrome Web Store |
| **Firefox 128+** | Moderne declaratieve browserextensie | Voorbereiding voor Firefox Add-ons |

## Filterstanden

| Stand | Profiel | Wat wordt geblokkeerd |
| --- | --- | --- |
| 1 | Basis (Basic) | Alleen de meest opdringerige advertentie- en trackerdomeinen. Vrijwel geen kans op foutieve blokkades. |
| 2 | Gebalanceerd (Balanced) | Bredere dekking inclusief populaire analyse- en telemetrieplatformen. |
| 3 | Uitgebreid (Extended) | Uitgebreide bescherming voor dagelijks internetgebruik. **Aanbevolen standaard.** |
| 4 | Strikt (Strict) | Agressieve filtering. Kan af en toe ingesloten externe widgets beïnvloeden. |
| 5 | Maximaal (Maximum) | Past de volledige blokkeerlijst toe (behalve belangrijke sociale media). Sommige complexe sites hebben mogelijk een uitzondering nodig. |

💡 **Ontwikkelaarstip:** Als een website niet goed laadt, zet de filter dan één stand lager of zet de schakelaar even kort uit.

## Hoe het werkt (Geen tovertrucs!)

Telkens wanneer een app of webpagina iets van internet wil laden, vraagt deze eerst naar het IP-adres van het betreffende domein (via een DNS-query). MuteAds fungeert als je persoonlijke lokale portier:

- Behoort het domein tot een advertentie- of trackernetwerk, dan antwoordt MuteAds direct met: *„Bestaat niet (NXDOMAIN)“*. De verbinding komt nooit tot stand, wat mobiele data en batterij bespaart.
- Gaat het om normale inhoud die je daadwerkelijk wilt bezoeken, dan wordt het verzoek direct doorgestuurd naar de standaard upstream DNS-servers en laadt de pagina razendsnel.

Op Android gebeurt dit via een **lokale loopback-VPN** die nooit gegevens buiten je telefoon stuurt. Op de computer functioneert MuteAds als je lokale DNS-server. In de browser gebruikt de extensie de officiële snelle engine `declarativeNetRequest`.

## Privacy op de eerste plaats: Wij willen jouw gegevens niet

- **Geen account, geen registratie**: We hebben geen aanmeldformulieren en geen centrale gebruikersdatabase.
- **100% lokaal op je toestel**: De filtering vindt uitsluitend plaats op je eigen apparaat. We beheren geen servers die kunnen zien welke sites je bezoekt.
- **Heldere updates**: De enige zelfstandige netwerkactie van de app is het ongeveer wekelijks ophalen van bijgewerkte domeinlijsten.
- **Minimale machtigingen**: De browserextensie vraagt alleen rechten die strikt noodzakelijk zijn om netwerkverzoeken te blokkeren, instellingen op te slaan, de wekelijkse timer te beheren en YouTube-advertenties aan te pakken.

## Handig om te weten

- **Voor Android-gebruikers:** Schakel *Privé-DNS* uit in de netwerkinstellingen van je telefoon, anders omzeilt Android de lokale filter. Schakel ook batterijoptimalisatie uit voor de app.
- **Advertenties van hetzelfde domein:** Pure DNS-filtering kan geen advertenties tegenhouden die vanaf hetzelfde domein als de hoofdinhoud worden geserveerd. Daarom bevat onze browserextensie een speciale module voor YouTube.
- **Het kat-en-muisspel op YouTube:** Videoplatforms passen hun advertentiescripts regelmatig aan. Als er advertenties doorglippen, zorg er dan voor dat je de nieuwste versie van de extensie gebruikt.

## Feedback & Community

Heb je een pagina gevonden die niet goed laadt of een advertentie die doorglipt? Open gerust een [Issue](../../issues) met de URL en het gebruikte filterniveau. We waarderen elke melding enorm!

## Licentie & Erkenning

De Android-app en zelfstandige DNS-proxy zijn gebaseerd op het fantastische open-sourceproject [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) van Ingo Zenz en vallen onder de GNU General Public License v2 of nieuwer. Met liefde gemaakt voor een schoner internet.
