<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Utište reklamy a sledovací skripty na telefonu, počítači i v prohlížeči.<br>Jeden přepínač, pět úrovní filtrování, žádný účet, 100% lokálně ve vašem zařízení.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <b>Čeština</b> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Proč jsme vytvořili MuteAds

Stejně jako vám, i nám vadil dnešní internet: blikající reklamní bannery, sledovací skripty zaznamenávající každé kliknutí, rychle se vybíjející baterie a těžkopádné blokátory, které zpomalují počítač nebo potají prodávají data uživatelů. Vytvořili jsme MuteAds s jediným posláním: utnout reklamy a trackery přímo u kořene odmítnutím spojení s jejich doménami dříve, než se vůbec dostanou na vaši obrazovku.

Bez nutnosti rootu. Bez zakládání účtů. A to nejdůležitější: **ani jediný bajt vaší historie procházení nikdy neopustí vaše zařízení**. Veškeré filtrování probíhá 100% lokálně na vašem vlastním hardwaru.

- **Spolehlivé blokování na úrovni domén**: Chrání všechny aplikace v systému (Android, desktop) nebo přímo ve vašem oblíbeném prohlížeči (rozšíření).
- **5 promyšlených úrovní filtrování**: Od „Základní“ (zcela bezpečné, nerozbije pracovní weby) po „Maximální“ (nekompromisní štít soukromí). Výchozí úroveň 3 je vyladěný zlatý střed.
- **Integrované blokování reklam na YouTube**: Součást přímo v rozšíření prohlížeče. Zapněte přepínač a sledujte videa bez otravných přestávek.
- **Jeden hlavní vypínač**: Život je už tak dost složitý. Potřebujete filtr dočasně vypnout pro otestování webu? Jedno kliknutí a vše funguje jako dřív.
- **Moderní šifrované DNS**: Plná podpora DNS-over-HTTPS (DoH) a DNS-over-TLS (DoT) na Androidu i počítači proti slídění poskytovatelů internetu.
- **Plná kontrola nad pravidly**: Vlastní seznamy povolených (allowlist), blokovaných (blocklist) a vlastní mapování IP s podporou zástupných znaků `*`.

## Ke stažení a stav projektu

> MuteAds je v rané verzi (v0.1). Připravujeme zařazení do oficiálních obchodů s doplňky. Mezitím jsou přímé instalační balíčky k dispozici na stránce [Releases](../../releases).

| Platforma | Jak funguje uvnitř | Stav |
| --- | --- | --- |
| **Android** | Místní loopback VPN filtrující DNS přímo v zařízení. Bez rootu. Android 4.2+ | APK na stránce [Releases](../../releases) |
| **Windows** | Místní služba DNS filtru pro celé PC (x64, ARM64) | K dispozici na [Releases](../../releases) |
| **macOS** | Místní celosystémový DNS filtr pro Mac | K dispozici na [Releases](../../releases) |
| **Linux** | Samostatné DNS proxy pro jeden počítač nebo celou domácí síť (vyžaduje Javu) | K dispozici na [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Lehké a bleskurychlé rozšíření MV3 | Příprava na schválení v obchodě |
| **Firefox 128+** | Moderní deklarativní rozšíření prohlížeče | Příprava na schválení v doplňcích |

## Úrovně filtrování

| Úroveň | Profil | Co se blokuje |
| --- | --- | --- |
| 1 | Základní (Basic) | Pouze reklamní a sledovací sítě nejvyšší priority. Minimální riziko planých poplachů. |
| 2 | Vyvážená (Balanced) | Širší pokrytí včetně běžných analytických a telemetrických platforem. |
| 3 | Rozšířená (Extended) | Komplexní ochrana pro každodenní surfování. **Doporučený výchozí stav.** |
| 4 | Přísná (Strict) | Agresivní filtrování. Může občas ovlivnit vložené widgety třetích stran. |
| 5 | Maximální (Maximum) | Uplatňuje kompletní seznam blokací (mimo hlavní sociální sítě). Některé složité stránky mohou vyžadovat výjimku. |

💡 **Vývojářský tip:** Pokud se některá stránka nenačte správně, jednoduše snižte úroveň o jeden stupeň nebo na chvíli vypněte přepínač.

## Jak to funguje (Žádná kouzla!)

Kdykoli chce aplikace nebo web načíst obsah, nejprve se dotáže na IP adresu doménového jména (DNS dotaz). MuteAds funguje jako váš osobní vrátný:

- Pokud doména patří reklamní síti nebo sledovacímu systému, MuteAds okamžitě odpoví: *„Neexistuje (NXDOMAIN)“*. Ke spojení vůbec nedojde, což šetří data i baterii.
- Pokud jde o legitimní obsah, dotaz je hladce předán běžnému upstream DNS serveru a stránka se načte okamžitě plnou rychlostí.

Na Androidu to zajišťuje **místní loopback VPN**, která nikdy neposílá data ven. Na počítači funguje MuteAds jako místní DNS resolver. V prohlížeči rozšíření využívá nativní rychlé rozhraní `declarativeNetRequest`.

## Soukromí na prvním místě: Vaše data nechceme

- **Bez účtů a přihlašování**: Nemáme registrační formuláře ani žádnou centrální databázi uživatelů.
- **100% ve vašem zařízení**: Filtrování probíhá výhradně lokálně. Neprovozujeme žádné servery, které by sledovaly navštívené stránky.
- **Transparentní aktualizace**: Jedinou automatickou síťovou aktivitou je stažení aktualizovaného seznamu blokovaných domén přibližně jednou týdně.
- **Minimální oprávnění**: Rozšíření žádá pouze o to, co je nezbytné pro blokování požadavků, ukládání nastavení, týdenní časovač a obsluhu `youtube.com`.

## Užitečné informace

- **Pro uživatele Androidu:** Nezapomeňte v nastavení sítě telefonu vypnout *Soukromé DNS*, jinak Android místní filtr obejde. Vypněte také optimalizaci baterie pro MuteAds.
- **Reklamy ze stejné domény:** Samotné DNS filtrování nedokáže zablokovat reklamy šířené ze stejné domény jako hlavní obsah. Proto naše rozšíření obsahuje speciální modul pro YouTube.
- **Hra na kočku a myš na YouTube:** Videoplatformy pravidelně upravují kód pro vkládání reklam. Pokud reklama projde, ujistěte se, že máte nejnovější verzi rozšíření.

## Zpětná vazba a komunita

Narazili jste na poškozenou stránku nebo reklamu, která proklouzla? Otevřete [Issue](../../issues) a uveďte URL adresu a použitou úroveň filtru. Každá vaše zpráva nám pomáhá!

## Licence a poděkování

Aplikace pro Android a samostatné DNS proxy jsou postaveny na skvělém open-source projektu [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) od Ingo Zenze a jsou šířeny pod licencí GNU General Public License v2 nebo novější. Vytvořeno s péčí pro čistší internet.
