<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Wycisz reklamy i skrypty śledzące na telefonie, komputerze i w przeglądarce.<br>Jeden przełącznik, pięć poziomów filtracji, zero kont, 100% lokalnie.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <b>Polski</b> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Dlaczego stworzyliśmy MuteAds

Dokładnie tak jak Ty mieliśmy serdecznie dość współczesnego internetu: migających banerów zasłaniających treść, wszechobecnych trackerów rejestrujących każde kliknięcie, baterii znikającej w oczach oraz ociężałych wtyczek, które zamulają system albo sprzedają dane użytkowników. Stworzyliśmy MuteAds z jednym jasnym założeniem: odcinać reklamy i trackery u samego źródła poprzez odrzucanie połączeń z ich domenami, zanim w ogóle trafią na ekran.

Bez roota. Bez rejestracji i kont. A co najważniejsze: **ani jeden bajt Twojej historii przeglądania nigdy nie opuszcza Twojego urządzenia**. Całe filtrowanie odbywa się w 100% lokalnie na Twoim sprzęcie.

- **Niezawodne blokowanie na poziomie domen**: Działa we wszystkich aplikacjach w systemie (Android, komputer) lub bezpośrednio w przeglądarce (rozszerzenie).
- **5 przemyślanych poziomów filtracji**: Od „Podstawowego” (bezpieczny, nie psuje portali pracowniczych czy bankowości) po „Maksymalny” (żelazna tarcza prywatności). Domyślny poziom 3 to idealny złoty środek.
- **Wbudowane blokowanie reklam na YouTube**: Zintegrowane w rozszerzeniu przeglądarki. Włącz przełącznik i oglądaj wideo bez irytujących przerw reklamowych.
- **Jeden główny przełącznik**: Życie jest wystarczająco skomplikowane. Chcesz na chwilę wyłączyć filtrowanie, aby coś sprawdzić? Jedno kliknięcie i wszystko natychmiast wraca do normy.
- **Nowoczesny szyfrowany DNS**: Pełne wsparcie dla DNS-over-HTTPS (DoH) i DNS-over-TLS (DoT) na Androidzie i komputerze, chroniące zapytania przed wścibskimi dostawcami internetu.
- **Pełna swoboda reguł**: Obsługa własnych list dozwolonych (allowlist), list blokowanych (blocklist) oraz reguł mapowania IP z obsługą masek `*`.

## Pobieranie i stan projektu

> MuteAds znajduje się obecnie we wczesnej fazie wydań (v0.1). Aktywnie dopracowujemy kompilacje i przygotowujemy zgłoszenia do oficjalnych sklepów. W międzyczasie instalatory są dostępne bezpośrednio na stronie [Releases](../../releases).

| Platforma | Zasada działania | Status |
| --- | --- | --- |
| **Android** | Lokalny loopback VPN filtrujący zapytania DNS na urządzeniu. Bez roota. Android 4.2+ | Pobierz APK w [Releases](../../releases) |
| **Windows** | Lokalna usługa filtrowania DNS dla całego systemu (x64, ARM64) | Dostępne w [Releases](../../releases) |
| **macOS** | Lokalny filtr DNS dla całego systemu Mac | Dostępne w [Releases](../../releases) |
| **Linux** | Samodzielne proxy DNS dla komputera lub całej sieci domowej (wymaga Javy) | Dostępne w [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Lekkie i szybkie rozszerzenie przeglądarki MV3 | Przygotowanie do publikacji w sklepie |
| **Firefox 128+** | Wydajne deklaratywne rozszerzenie przeglądarki | Przygotowanie do publikacji w dodatkach |

## Poziomy filtracji

| Poziom | Profil | Zakres blokowania |
| --- | --- | --- |
| 1 | Podstawowy (Basic) | Tylko domeny reklamowe i śledzące o najwyższym priorytecie. Znikome ryzyko fałszywych alarmów. |
| 2 | Zrównoważony (Balanced) | Szerszy zasięg, obejmujący popularne platformy analityczne i telemetryczne. |
| 3 | Rozszerzony (Extended) | Wszechstronna ochrona na co dzień. **Zalecany domyślny.** |
| 4 | Rygorystyczny (Strict) | Agresywne filtrowanie. Może czasami wpłynąć na osadzone widżety zewnętrzne. |
| 5 | Maksymalny (Maximum) | Zastosowanie pełnej listy blokad (z wyjątkiem głównych sieci społecznościowych). Niektóre zaawansowane strony mogą wymagać dodania do wyjątków. |

💡 **Wskazówka programisty:** Jeśli dana strona nie wyświetla się poprawnie, po prostu obniż poziom o jeden stopień lub wyłącz na chwilę przełącznik.

## Jak to działa (Zero czarnej magii!)

Za każdym razem, gdy aplikacja lub strona internetowa chce pobrać jakiekolwiek zasoby, najpierw pyta o adres IP kryjący się za nazwą domeny (zapytanie DNS). MuteAds działa jak Twój lokalny strażnik:

- Jeżeli domena należy do sieci reklamowej lub telemetrycznej, MuteAds natychmiast odpowiada: *„Nie istnieje (NXDOMAIN)”*. Połączenie w ogóle nie dochodzi do skutku, oszczędzając transfer i baterię.
- Jeżeli jest to właściwa treść, o którą prosiłeś, zapytanie jest błyskawicznie przekazywane do standardowego serwera DNS i strona ładuje się z pełną prędkością.

Na Androidzie odbywa się to za pośrednictwem **lokalnego pętlowego VPN-a**, który nigdy nie wysyła ruchu na zewnątrz. Na komputerze MuteAds działa jako lokalny resolver DNS Twojego systemu. W przeglądarce rozszerzenie wykorzystuje ultraszybki natywny silnik `declarativeNetRequest`.

## Prywatność na pierwszym miejscu: Nie chcemy Twoich danych

- **Bez kont i logowania**: Nie posiadamy formularzy rejestracyjnych ani centralnej bazy użytkowników.
- **100% na Twoim urządzeniu**: Filtrowanie odbywa się wyłącznie na Twoim sprzęcie. Nie utrzymujemy żadnych serwerów podglądających przeglądane strony.
- **Przejrzyste aktualizacje**: Jedyną automatyczną aktywnością sieciową aplikacji jest pobieranie zaktualizowanych list blokowanych domen około raz w tygodniu.
- **Minimalne uprawnienia**: Rozszerzenie przeglądarki wymaga wyłącznie uprawnień niezbędnych do blokowania żądań, zapisu konfiguracji, cotygodniowego odświeżania oraz obsługi `youtube.com`.

## Warto wiedzieć

- **Dla użytkowników Androida:** Pamiętaj o wyłączeniu opcji *Prywatny DNS* w ustawieniach sieci telefonu, w przeciwnym razie system pominie lokalny filtr. Wyłącz także optymalizację baterii dla aplikacji.
- **Reklamy z tej samej domeny:** Filtrowanie DNS nie jest w stanie wyciąć reklam serwowanych bezpośrednio z tej samej domeny co treść główna. Dlatego nasze rozszerzenie przeglądarki posiada dedykowany moduł dla YouTube.
- **Zabawa w kotka i myszkę z YouTube:** Platformy wideo regularnie modyfikują skrypty reklamowe. Jeśli jakaś reklama się przedostanie, upewnij się, że masz najnowszą wersję rozszerzenia.

## Opinie i społeczność

Znalazłeś stronę, która wyświetla się błędnie, albo reklamę, która się przedarła? Otwórz [Issue](../../issues), podając adres strony i używany poziom filtru. Każde zgłoszenie jest dla nas ogromną pomocą!

## Licencja i podziękowania

Aplikacja na Androida i samodzielne proxy DNS bazują na świetnym projekcie open source [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) autorstwa Ingo Zenza i są udostępniane na warunkach licencji GNU General Public License v2 lub nowszej. Tworzone z pasją dla czystszego internetu.
