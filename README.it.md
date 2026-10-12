<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Silenzia pubblicità e tracker su smartphone, computer e browser.<br>Un solo interruttore, cinque livelli di filtraggio, nessun account, 100% sul tuo dispositivo.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <b>Italiano</b> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Perché abbiamo creato MuteAds

Proprio come te, eravamo stufi del web moderno: banner lampeggianti e invasivi, script di tracciamento che registrano ogni tocco, batteria che si prosciuga e ad-blocker pesanti che rallentano il computer o rivendono i dati degli utenti. Abbiamo creato MuteAds con un obiettivo chiaro: tagliare pubblicità e tracker alla radice, rifiutando qualsiasi connessione ai loro domini prima ancora che appaiano sul tuo schermo.

Nessun root necessario. Nessun account, nessuna registrazione. E soprattutto: **nemmeno un singolo byte della tua navigazione lascia mai il tuo dispositivo**. Tutto viene elaborato localmente sul tuo hardware.

- **Blocco a livello DNS impeccabile**: Funziona su tutte le app del sistema (Android, computer) o direttamente all'interno del tuo browser preferito (estensione).
- **5 livelli di filtraggio su misura**: Dal livello "Base" (sicurissimo, non danneggia siti di lavoro o home banking) fino al livello "Massimo". Il livello 3 è il punto di equilibrio ideale per tutti i giorni.
- **Blocco pubblicità YouTube integrato**: Già presente nell'estensione per browser. Basta accendere l'interruttore e guardare i video senza continue interruzioni.
- **Un unico interruttore centrale**: La vita è già abbastanza complicata. Vuoi disattivare temporaneamente il blocco per testare un sito? Un clic e tutto torna subito come prima.
- **DNS crittografato moderno**: Supporto nativo per DNS-over-HTTPS (DoH) e DNS-over-TLS (DoT) su Android e desktop, al riparo da occhi indiscreti di provider e reti pubbliche.
- **Totale libertà di personalizzazione**: Supporto completo per liste consentite (allowlist), liste bloccate (blocklist) e mappature IP personalizzate con caratteri jolly `*`.

## Download e Versioni

> MuteAds è attualmente in fase di rilascio preliminare (v0.1). Stiamo perfezionando le build in vista dei negozi ufficiali. Nel frattempo, i pacchetti di installazione sono disponibili sulla pagina [Releases](../../releases).

| Piattaforma | Come funziona all'interno | Stato |
| --- | --- | --- |
| **Android** | VPN locale in loopback che filtra i DNS sul dispositivo. Senza root. Android 4.2+ | APK su [Releases](../../releases) |
| **Windows** | Filtro DNS locale per l'intero sistema (x64, ARM64) | Disponibile su [Releases](../../releases) |
| **macOS** | Filtro DNS locale per tutto il sistema operativo Mac | Disponibile su [Releases](../../releases) |
| **Linux** | Proxy DNS autonomo per un computer o l'intera rete locale (richiede Java) | Disponibile su [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Estensione browser MV3 leggera e ultra performante | In preparazione per lo store |
| **Firefox 128+** | Estensione dichiarativa moderna e veloce | In preparazione per i componenti aggiuntivi |

## Livelli di Filtraggio

| Livello | Profilo | Cosa viene bloccato |
| --- | --- | --- |
| 1 | Base (Basic) | Soltanto i server pubblicitari e di tracciamento a più alta priorità. Rischio di falsi positivi quasi nullo. |
| 2 | Bilanciato (Balanced) | Copertura estesa che include piattaforme diffuse di statistica e telemetria. |
| 3 | Esteso (Extended) | Protezione completa per la navigazione quotidiana. **Consigliato (Predefinito).** |
| 4 | Rigoroso (Strict) | Filtraggio aggressivo. Può occasionalmente interferire con alcuni widget esterni. |
| 5 | Massimo (Maximum) | Applica l'intera lista di blocco eccetto i principali social network. Alcuni siti complessi potrebbero richiedere eccezioni. |

💡 **Consiglio dello sviluppatore:** Se un sito non viene caricato correttamente, basta abbassare il filtro di un livello o spegnere l'interruttore per qualche istante.

## Come funziona (Nessuna magia nera!)

Ogni volta che un'app o una pagina web vuole scaricare qualcosa da internet, deve prima chiedere l'indirizzo IP del dominio corrispondente (tramite query DNS). MuteAds agisce da fidato guardiano locale:

- Se il dominio appartiene a una rete pubblicitaria o di tracciamento, MuteAds risponde istantaneamente: *"Non esiste (NXDOMAIN)"*. La connessione non viene mai stabilita, risparmiando traffico dati e batteria.
- Se si tratta di contenuto legittimo che vuoi consultare, la richiesta viene inoltrata normalmente ai server DNS standard e la pagina si carica a piena velocità.

Su Android, questo avviene tramite una **VPN locale interna** che non invia mai il traffico all'esterno. Su computer, MuteAds funge da server DNS locale della tua macchina. Nel browser, l'estensione sfrutta la velocissima API nativa `declarativeNetRequest`.

## Privacy prima di tutto: I tuoi dati non ci interessano

- **Nessun account, nessun login**: Non abbiamo form di registrazione né database centralizzati degli utenti.
- **100% sul tuo dispositivo**: Il filtraggio avviene esclusivamente sulla tua macchina. Non abbiamo server intermedi che possano osservare le tue attività sul web.
- **Aggiornamenti trasparenti**: L'unico contatto di rete periodico effettuato dall'app è il download delle liste di domini aggiornate, circa una volta a settimana.
- **Permessi minimi**: L'estensione richiede solo i permessi strettamente necessari per bloccare le richieste, salvare le impostazioni, programmare l'aggiornamento e agire su `youtube.com`.

## Consigli utili da ricordare

- **Utenti Android:** Ricordati di disattivare l'opzione *DNS Privato* nelle impostazioni di rete del telefono, altrimenti Android aggirerà il filtro locale. Disattiva anche l'ottimizzazione aggressiva della batteria.
- **Pubblicità dallo stesso dominio:** Il blocco tramite DNS non può intervenire sugli annunci serviti dallo stesso dominio del contenuto principale. Ecco perché la nostra estensione include un modulo specializzato per YouTube.
- **Il gioco del gatto e del topo con YouTube:** Le piattaforme video aggiornano spesso i loro script di erogazione. Se un annuncio dovesse riapparire, controlla di avere installato l'ultima versione dell'estensione.

## Feedback e Community

Hai notato un sito con errori grafici o una pubblicità ostinata che è riuscita a passare? Apri una [Issue](../../issues) indicando l'indirizzo della pagina e il livello di filtraggio utilizzato. Ogni segnalazione ci aiuta a migliorare!

## Licenza e Ringraziamenti

L'app Android e il proxy DNS autonomo si basano sullo straordinario progetto open source [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) di Ingo Zenz, distribuito sotto licenza GNU General Public License v2 o successiva. Realizzato con passione per un web più pulito.
