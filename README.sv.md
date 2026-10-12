<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds logotyp">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Tysta reklam och spårare på din telefon, dator och i din webbläsare.<br>En enda knapp, fem filternivåer, inga konton, 100% lokalt på din enhet.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <b>Svenska</b> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Varför vi skapade MuteAds

Precis som du var vi trötta på dagens internet: skrikiga banners som blinkar överallt, spårningsskript som kartlägger varje klick, batterier som laddar ur på nolltid och klumpiga reklamblockerare som gör datorn seg eller säljer användardata. Vi byggde MuteAds med ett enda tydligt mål: stoppa reklam och spårare direkt vid källan genom att vägra ansluta till deras domäner innan de ens når skärmen.

Inget krav på root. Inget konto eller inloggning. Och framför allt: **inte en enda byte av din webbhistorik lämnar någonsin din enhet**. All filtrering sker 100% lokalt på din egen hårdvara.

- **Effektiv blockering på domännivå**: Skyddar alla appar i systemet (Android, PC/Mac) eller direkt inuti din webbläsare (tillägg).
- **5 genomtänkta filternivåer**: Från „Grundläggande“ (supersäkert, slår inte sönder jobbsidor) till „Maximalt“ (kompromisslöst integritetsskydd). Nivå 3 är vårt rekommenderade standardläge.
- **Inbyggd YouTube-reklamblockering**: Ingår direkt i webbläsartillägget. Slå på brytaren och njut av videor utan frustrerande avbrott.
- **En enda huvudströmbrytare**: Livet är redan tillräckligt krångligt. Behöver du stänga av filtret tillfälligt för att testa en sida? Ett klick räcker, allt återgår genast till det vanliga.
- **Moderna krypterade DNS-protokoll**: Fullt stöd för DNS-over-HTTPS (DoH) och DNS-over-TLS (DoT) på Android och dator för att skydda mot snokande internetleverantörer.
- **Full kontroll över egna regler**: Skapa egna vitlistor (allowlist), svartlistor (blocklist) och anpassade IP-kopplingar med stöd för jokertecken `*`.

## Nedladdningar & Status

> MuteAds är för närvarande i tidig förhandsversion (v0.1). Vi finjusterar apparna och förbereder lansering i de officiella butikerna. Under tiden finns installationsfiler direkt tillgängliga på sidan [Releases](../../releases).

| Plattform | Hur det fungerar under huven | Status |
| --- | --- | --- |
| **Android** | Lokalt loopback-VPN som filtrerar DNS på enheten. Inget root. Android 4.2+ | APK på [Releases](../../releases) |
| **Windows** | Lokal DNS-filtertjänst för hela datorn (x64, ARM64) | Tillgänglig på [Releases](../../releases) |
| **macOS** | Lokalt systemövergripande DNS-filter för Mac | Tillgänglig på [Releases](../../releases) |
| **Linux** | Fristående DNS-proxy för en maskin eller hela hemnätverket (kräver Java) | Tillgänglig på [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Lättviktigt och blixtsnabbt MV3-webbläsartillägg | Granskning för webbutiken förbereds |
| **Firefox 128+** | Modernt deklarativt webbläsartillägg | Granskning för tilläggsbutiken förbereds |

## Filternivåer

| Nivå | Profil | Vad som blockeras |
| --- | --- | --- |
| 1 | Grundläggande (Basic) | Endast välkända reklam- och spårningsservrar med högsta prioritet. Minimal risk för falska larm. |
| 2 | Balanserad (Balanced) | Bredare täckning inklusive vanliga analys- och telemetritjänster. |
| 3 | Utökad (Extended) | Omfattande blockering anpassad för dagligt surfande. **Rekommenderad standard.** |
| 4 | Strikt (Strict) | Aggressiv filtrering. Kan ibland störa externa inbäddade moduler. |
| 5 | Maximalt (Maximum) | Tillämpar hela spärrlistan (utom grundläggande sociala medier). Vissa komplexa sidor kan behöva undantag. |

💡 **Utvecklartips:** Om en webbplats inte laddas som den ska, sänk filtret ett steg eller stäng av knappen en kort stund.

## Hur det fungerar (Ingen svart magi!)

Varje gång en app eller webbsida vill hämta något från nätet, frågar den först efter IP-adressen bakom domännamnet (via en DNS-förfrågan). MuteAds fungerar som din lokala dörrvakt:

- Om domänen tillhör ett reklam- eller spårningsnätverk svarar MuteAds direkt: *„Finns inte (NXDOMAIN)“*. Anslutningen upprättas aldrig, vilket sparar datamängd och batteri.
- Om det rör sig om legitimt innehåll skickas förfrågan vidare till din vanliga DNS-server och sidan laddas blixtsnabbt som vanligt.

På Android sker detta genom ett **lokalt loopback-VPN** som aldrig skickar trafik utanför telefonen. På datorn fungerar appen som en lokal DNS-server. I webbläsaren utnyttjar tillägget webbläsarens officiella motor `declarativeNetRequest`.

## Integritet först: Vi vill inte ha din data

- **Inget konto, ingen inloggning**: Vi har inga registreringsformulär och ingen användardatabas.
- **100% på din enhet**: All filtrering sker uteslutande lokalt. Vi driver inga servrar som kan se vad du besöker.
- **Rena uppdateringar**: Den enda självständiga nätverksaktiviteten är att hämta uppdaterade spärrlistor ungefär en gång i veckan.
- **Minimala behörigheter**: Tillägget ber endast om de behörigheter som krävs för att blockera förfrågningar, spara inställningar, hantera veckouppdateringar och hantera `youtube.com`.

## Bra att veta

- **För Android-användare:** Stäng av *Privat DNS* i telefonens nätverksinställningar, annars kringgår Android det lokala filtret. Undanta även MuteAds från batterioptimering.
- **Förstapartsannonser:** Ren DNS-filtrering kan inte stoppa annonser som levereras från samma domän som själva innehållet. Därför har vårt webbläsartillägg en särskild modul för YouTube.
- **Katt-och-råtta-leken på YouTube:** Videoplattformar uppdaterar sina reklamskript regelbundet. Om en annons slinker igenom, se till att uppdatera tillägget till den senaste versionen.

## Synpunkter & Gemenskap

Har du hittat en trasig webbsida eller en envis annons som slapp igenom? Öppna gärna ett [Issue](../../issues) med sidans adress och den filternivå du använde. Vi uppskattar all feedback!

## Licens & Tack

Android-appen och den fristående DNS-proxyn bygger på det fantastiska öppen källkod-projektet [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) av Ingo Zenz och distribueras under GNU General Public License v2 eller senare. Skapat med omsorg för ett renare internet.
