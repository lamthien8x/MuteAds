<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds Logo">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Schluss mit Werbung und Trackern auf Smartphone, PC und im Browser.<br>Ein Schalter, fünf Filterstufen, kein Account, 100% lokal auf deinem Gerät.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <b>Deutsch</b> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Warum wir MuteAds gebaut haben

Genau wie du hatten wir die Nase voll vom modernen Internet: blinkende Banner an jeder Ecke, Schnüffel-Skripte, die jeden Mausklick aufzeichnen, rasant schrumpfende Akkulaufzeiten und überladene Werbeblocker, die das System ausbremsen oder heimlich Daten verkaufen. Wir haben MuteAds mit einem klaren Ziel entwickelt: Werbung und Tracker direkt an der Wurzel kappen, indem Verbindungen zu deren Domains blockiert werden, bevor sie überhaupt deinen Bildschirm erreichen.

Kein Root erforderlich. Kein Account, keine Registrierung. Und das Wichtigste: **kein einziges Byte deines Surfverhaltens verlässt dein Gerät**. Die gesamte Filterung findet vollständig und lokal auf deiner eigenen Hardware statt.

- **Zuverlässige DNS-Blockierung**: Stoppt Werbung und Tracker systemweit über alle Apps hinweg (Android, Desktop) oder direkt im Webbrowser (Erweiterung).
- **5 fein abgestufte Filterlevel**: Von „Basis“ (äußerst vorsichtig, bricht keine Arbeitsportale) bis „Maximum“ (kompromissloser Schutz). Stufe 3 ist unser perfekt ausbalancierter Standard.
- **Integrierter YouTube-Werbeblocker**: Direkt in der Browser-Erweiterung integriert. Einfach einschalten und Videos ohne lästige Werbeunterbrechungen genießen.
- **Ein einziger Hauptschalter**: Das Leben ist schon kompliziert genug. Musst du den Filter kurz ausschalten, um eine Website zu testen? Ein Klick genügt, und alles ist sofort wieder im Ursprungszustand.
- **Modernes verschlüsseltes DNS**: Vollständige Unterstützung für DNS-over-HTTPS (DoH) und DNS-over-TLS (DoT) unter Android und Desktop zum Schutz vor neugierigen Internetanbietern.
- **Volle Kontrolle über eigene Regeln**: Eigene Whitelists, Blacklists und benutzerdefinierte IP-Zuordnungen mit Wildcard-Unterstützung (`*`).

## Downloads & Entwicklungsstand

> MuteAds befindet sich derzeit in der Early-Release-Phase (Version 0.1). Wir arbeiten mit Hochdruck an den offiziellen Store-Listings. In der Zwischenzeit stehen direkte Installationsdateien auf der Seite [Releases](../../releases) bereit.

| Plattform | Funktionsweise | Status |
| --- | --- | --- |
| **Android** | Lokales Loopback-VPN filtert DNS direkt auf dem Gerät. Kein Root nötig. Android 4.2+ | APK direkt unter [Releases](../../releases) |
| **Windows** | Lokaler DNS-Filterdienst für den gesamten PC (x64, ARM64) | Verfügbar unter [Releases](../../releases) |
| **macOS** | Lokaler systemweiter DNS-Filter | Verfügbar unter [Releases](../../releases) |
| **Linux** | Eigenständiger DNS-Proxy für PC oder das gesamte Heimnetzwerk (benötigt Java) | Verfügbar unter [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Schlanke, hochperformante MV3-Browser-Erweiterung | Store-Einreichung in Vorbereitung |
| **Firefox 128+** | Schnelle deklarative Browser-Erweiterung | Add-on-Einreichung in Vorbereitung |

## Filterstufen im Überblick

| Stufe | Profil | Was blockiert wird |
| --- | --- | --- |
| 1 | Basis (Basic) | Ausschließlich bekannte Werbe- und Tracking-Server höchster Priorität. Nahezu keine Fehlalarme. |
| 2 | Ausgewogen (Balanced) | Erweiterte Abdeckung gängiger Web-Analyse- und Telemetriedienste. |
| 3 | Erweitert (Extended) | Umfassender Schutz für den täglichen Gebrauch. **Standardempfehlung.** |
| 4 | Strikt (Strict) | Sehr aggressive Filterung. Kann vereinzelt externe Widgets beeinträchtigen. |
| 5 | Maximum (Maximum) | Die vollständige Sperrliste (außer wesentlichen sozialen Netzen). Manche komplexen Webseiten erfordern Ausnahmen. |

💡 **Entwickler-Tipp:** Wenn eine Website unvollständig lädt, stelle den Filter einfach eine Stufe niedriger oder schalte ihn kurzzeitig aus.

## So funktioniert es (Keine Zauberei!)

Jedes Mal, wenn eine App oder Webseite Inhalte nachladen will, fragt sie zuerst nach der IP-Adresse der jeweiligen Domain (DNS-Abfrage). MuteAds fungiert dabei als dein persönlicher Pförtner:

- Gehört die Domain zu einem Werbe- oder Tracking-Dienst, antwortet MuteAds sofort mit: *„Existiert nicht (NXDOMAIN)“*. Die Verbindung kommt gar nicht erst zustande – das spart Datenvolumen und Akku.
- Handelt es sich um die eigentlichen Webseiten-Inhalte, wird die Anfrage reibungslos an den Upstream-DNS-Server weitergeleitet und die Seite lädt blitzschnell wie gewohnt.

Unter Android geschieht dies über ein **lokales Loopback-VPN**, das niemals Daten ins Internet leitet. Auf dem Desktop arbeitet MuteAds als lokaler DNS-Server deines Computers. Im Browser nutzt die Erweiterung die native Hochgeschwindigkeits-Engine `declarativeNetRequest`.

## Datenschutz: Deine Daten gehören dir

- **Kein Konto, kein Login**: Wir betreiben keine Registrierungsformulare und keine zentrale Nutzerdatenbank.
- **100% lokal auf deinem Gerät**: Die Filterung findet ausschließlich lokal statt. Wir betreiben keine Server, die deine besuchten Webseiten mitloggen könnten.
- **Transparente Updates**: Die einzige eigenständige Netzwerkaktivität der App ist das wöchentliche Herunterladen der aktualisierten Domain-Sperrlisten.
- **Minimale Berechtigungen**: Die Browser-Erweiterung fordert nur zwingend notwendige Berechtigungen an: Anfragen blockieren, Einstellungen speichern, wöchentlicher Wecker und Zugriff auf `youtube.com`.

## Wichtige Hinweise & Tipps

- **Android-Hinweis:** Schalte in den Netzwerkeinstellungen deines Smartphones unbedingt *Privates DNS* aus, da Android sonst lokale Filter umgeht. Deaktiviere zudem die Akku-Optimierung für MuteAds.
- **First-Party-Werbung:** Reine DNS-Filterung kann keine Werbung blockieren, die von derselben Domain wie die Hauptinhalte ausgeliefert wird. Aus diesem Grund besitzt unsere Browser-Erweiterung ein eigenes YouTube-Modul.
- **Katz-und-Maus-Spiel bei YouTube:** Videoplattformen ändern ihre Auslieferungstechniken regelmäßig. Sollten Werbeclips durchrutschen, aktualisiere die Erweiterung einfach auf die neueste Version.

## Feedback & Community

Eine fehlerhafte Website entdeckt oder ist eine hartnäckige Anzeige durchgeschlüpft? Erstelle gerne ein [Issue](../../issues) mit der URL und der verwendeten Filterstufe. Wir freuen uns über jeden Beitrag!

## Lizenz & Danksagung

Die Android-App und der eigenständige DNS-Proxy basieren auf dem großartigen Open-Source-Projekt [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) von Ingo Zenz und stehen unter der GNU General Public License v2 oder neuer. Ein Projekt für ein sauberes, freies Internet.
