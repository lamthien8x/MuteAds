<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Sigla MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Oprește reclamele și trackerii pe telefon, calculator și în browser.<br>Un singur comutator, cinci niveluri de filtrare, fără cont, 100% local pe dispozitiv.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <b>Română</b><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## De ce am creat MuteAds

La fel ca tine, ne-am săturat de internetul modern: bannere orbitoare care acoperă ecranul, scripturi de urmărire care monitorizează fiecare clic, baterie descărcată rapid și extensii greoaie care încetinesc sistemul sau vând datele utilizatorilor. Am creat MuteAds cu un obiectiv clar: oprirea reclamelor și a trackerilor direct de la sursă prin refuzul conexiunilor către domeniile lor înainte de a ajunge pe ecran.

Fără root. Fără conturi sau înregistrare. Și cel mai important: **niciun octet din istoricul tău de navigare nu părăsește vreodată dispozitivul**. Toată filtrarea are loc 100% local pe hardware-ul tău.

- **Blocare la nivel de domeniu eficientă**: Funcționează pentru toate aplicațiile din sistem (Android, desktop) sau direct în browserul tău preferat (extensie).
- **5 niveluri flexibile de filtrare**: De la nivelul „De bază” (extrem de sigur, nu afectează site-urile de serviciu) până la „Maxim”. Nivelul 3 este setarea implicită echilibrată.
- **Blocare integrată a reclamelor YouTube**: Inclusă direct în extensia de browser. Pornește comutatorul și vizionează clipuri fără întreruperi neplăcute.
- **Un singur comutator principal**: Viața e deja suficient de complicată. Vrei să oprești temporar filtrarea pentru a testa un site? Un clic și totul revine instantaneu la normal.
- **DNS criptat modern**: Suport complet pentru DNS-over-HTTPS (DoH) și DNS-over-TLS (DoT) pe Android și desktop pentru protecție împotriva furnizorilor de internet curioși.
- **Control deplin al regulilor**: Liste de permisiuni (allowlist), liste de blocare (blocklist) și mapări IP personalizate cu suport pentru caractere wildcard `*`.

## Descărcare și Stare

> MuteAds se află în faza inițială de lansare (v0.1). Pregătim publicarea în magazinele oficiale. În acest timp, kiturile de instalare sunt disponibile direct pe pagina [Releases](../../releases).

| Platformă | Cum funcționează | Stare |
| --- | --- | --- |
| **Android** | VPN local loopback care filtrează DNS pe dispozitiv. Fără root. Android 4.2+ | APK pe pagina [Releases](../../releases) |
| **Windows** | Serviciu local de filtrare DNS pentru întreg PC-ul (x64, ARM64) | Disponibil pe [Releases](../../releases) |
| **macOS** | Filtru DNS local pentru întregul sistem Mac | Disponibil pe [Releases](../../releases) |
| **Linux** | Proxy DNS autonom pentru un PC sau întreaga rețea locală (necesită Java) | Disponibil pe [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extensie de browser MV3 ultra-ușoară și rapidă | Pregătire pentru publicare în magazin |
| **Firefox 128+** | Extensie declarativă modernă și rapidă | Pregătire pentru publicare în magazin |

## Niveluri de Filtrare

| Nivel | Profil | Ce este blocat |
| --- | --- | --- |
| 1 | De bază (Basic) | Doar rețelele publicitare și de urmărire cu prioritate maximă. Risc minim de alarme false. |
| 2 | Echilibrat (Balanced) | Acoperire extinsă, inclusiv platforme comune de analiză și telemetrie. |
| 3 | Extins (Extended) | Protecție completă pentru navigarea zilnică. **Recomandat implicit.** |
| 4 | Strict (Strict) | Filtrare agresivă. Poate afecta ocazional widget-uri externe integrate. |
| 5 | Maxim (Maximum) | Aplică întreaga listă de blocare (cu excepția rețelelor sociale majore). Unele site-uri pot necesita excepții. |

💡 **Sfat de la dezvoltatori:** Dacă un site nu se încarcă corect, coboară nivelul de filtrare cu o treaptă sau oprește comutatorul pentru câteva secunde.

## Cum funcționează (Fără trucuri magice!)

De fiecare dată când o aplicație sau o pagină web dorește să încarce conținut, întreabă mai întâi care este adresa IP a numelui de domeniu (printr-o interogare DNS). MuteAds acționează ca portarul tău de încredere:

- Dacă domeniul aparține unei rețele publicitare sau de urmărire, MuteAds răspunde instantaneu: *„Inexistent (NXDOMAIN)”*. Conexiunea nu se inițiază niciodată, economisind date și baterie.
- Dacă este conținut legitim solicitat de tine, interogarea este trimisă fără întârziere către serverul DNS upstream și pagina se încarcă cu viteză maximă.

Pe Android, acest lucru se realizează printr-un **VPN local loopback** care nu trimite date în afara telefonului. Pe computer, devine rezolvitorul DNS local al sistemului. În browser, extensia utilizează motorul nativ ultra-rapid `declarativeNetRequest`.

## Confidențialitatea pe primul loc: Nu dorim datele tale

- **Fără cont, fără autentificare**: Nu avem formulare de înregistrare și nicio bază de date cu utilizatori.
- **100% pe dispozitivul tău**: Filtrarea se desfășoară exclusiv local. Nu operăm servere care să îți urmărească obiceiurile de navigare.
- **Actualizări transparente**: Singura comunicare automată a aplicației este descărcarea periodică a listelor actualizate de domenii, aproximativ o dată pe săptămână.
- **Permisiuni minime**: Extensia solicită doar permisiunile strict necesare pentru blocarea cererilor, salvarea setărilor, temporizatorul săptămânal și gestionarea `youtube.com`.

## Bine de știut

- **Pentru utilizatorii Android:** Asigură-te că dezactivezi *DNS Privat* în setările de rețea ale telefonului, altfel Android va ocoli filtrul local. Dezactivează și optimizarea agresivă a bateriei.
- **Reclame din același domeniu:** Filtrarea DNS pură nu poate bloca reclamele distribuite de pe același domeniu cu conținutul principal. Din acest motiv, extensia noastră include un modul dedicat pentru YouTube.
- **Jocul de-a șoarecele și pisica pe YouTube:** Platformele video își modifică periodic mecanismele de livrare a reclamelor. Dacă scapă vreo reclamă, actualizează extensia la cea mai recentă versiune.

## Feedback și Comunitate

Ai găsit un site cu probleme de afișare sau o reclamă care a trecut de filtru? Deschide un [Issue](../../issues) menționând adresa paginii și nivelul de filtrare folosit. Fiecare mesaj contează mult pentru noi!

## Licență și Mulțumiri

Aplicația Android și proxy-ul DNS autonom au la bază excelentul proiect open-source [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) creat de Ingo Zenz și sunt distribuite sub licența GNU GPL v2 sau ulterioară. Creat cu pasiune pentru un internet mai curat.
