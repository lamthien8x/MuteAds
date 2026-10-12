<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Sekat iklan dan penjejak pada telefon, komputer dan pelayar anda.<br>Satu suis, lima tahap penapis, tanpa akaun, 100% diproses dalam peranti.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <b>Bahasa Melayu</b> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Mengapa kami membina MuteAds

Sama seperti anda, kami bosan dengan internet moden: iklan sepanduk yang mengganggu, skrip penjejak yang memerhatikan setiap klik, bateri cepat habis, serta penyekat iklan berat yang memperlahankan sistem atau menjual data pengguna. MuteAds dibina dengan satu matlamat mudah: menyekat iklan dan penjejak terus dari akarnya dengan menolak sambungan ke domain mereka sebelum sempat dipaparkan.

Tanpa perlu root. Tanpa perlu mendaftar akaun. Dan paling utama: **tiada satu bait pun sejarah pelayaran anda yang keluar dari peranti anda**. Semua penapisan berlaku 100% secara setempat pada peranti anda sendiri.

- **Sekatan peringkat domain yang berkesan**: Berfungsi merentasi semua aplikasi pada sistem (Android, desktop) atau terus di dalam pelayar anda (sambungan).
- **5 tahap penapis fleksibel**: Dari tahap "Asas" (sangat selamat, tidak merosakkan laman kerja) hingga "Maksimum". Tahap 3 ialah pilihan lalai yang paling seimbang.
- **Sekatan iklan YouTube terbina dalam**: Hadir sedia dalam sambungan pelayar. Hidupkan suis dan tonton video tanpa gangguan iklan.
- **Satu suis utama yang ringkas**: Hidup ini sudah cukup rumit. Perlu mematikan sekatan seketika untuk menguji laman? Satu klik sahaja dan semuanya kembali normal.
- **DNS disulitkan moden**: Sokongan penuh untuk DNS-over-HTTPS (DoH) dan DNS-over-TLS (DoT) pada Android dan desktop bagi mengelakkan intipan pembekal internet.
- **Kawalan peraturan milik anda**: Kebebasan penuh menambah senarai dibenarkan (allowlist), senarai sekat (blocklist), dan pemetaan IP tersuai dengan wildcard `*`.

## Muat Turun & Status Rilis

> MuteAds kini dalam fasa rilis awal (v0.1). Kami sedang giat menyiapkan penyerahan ke gedung rasmi. Buat masa ini, pemasang terus boleh didapati di laman [Releases](../../releases).

| Platform | Mekanisme operasi dalaman | Status |
| --- | --- | --- |
| **Android** | VPN setempat menapis DNS dalam peranti. Tanpa root. Android 4.2+ | APK di [Releases](../../releases) |
| **Windows** | Penapis DNS setempat untuk seluruh komputer (x64, ARM64) | Tersedia di [Releases](../../releases) |
| **macOS** | Penapis DNS setempat untuk seluruh sistem Mac | Tersedia di [Releases](../../releases) |
| **Linux** | Proksi DNS mandiri untuk PC atau seluruh rangkaian rumah (memerlukan Java) | Tersedia di [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Sambungan pelayar MV3 yang pantas dan ringan | Penyediaan semakan gedung |
| **Firefox 128+** | Sambungan pelayar pantas dan moden | Penyediaan semakan gedung |

## Tahap Penapis

| Tahap | Profil | Skop Sekatan |
| --- | --- | --- |
| 1 | Asas (Basic) | Hanya domain iklan dan penjejak berkeutamaan tertinggi. Risiko salah sekat paling minima. |
| 2 | Seimbang (Balanced) | Liputan lebih meluas merangkumi platform analitik dan telemetri popular. |
| 3 | Lanjutan (Extended) | Perlindungan menyeluruh untuk kegunaan harian. **Lalai disyorkan.** |
| 4 | Ketat (Strict) | Penapisan agresif. Mungkin memberi kesan kepada widget pihak ketiga di sesetengah laman. |
| 5 | Maksimum (Maximum) | Menggunakan seluruh senarai sekatan kecuali media sosial utama. Sesetengah laman mungkin memerlukan senarai putih. |

💡 **Tip pembangun:** Jika sesebuah laman mengalami masalah paparan, turunkan tahap penapis satu takuk atau matikan suis untuk seketika.

## Cara ia berfungsi (Tiada sihir hitam!)

Setiap kali aplikasi atau halaman web ingin memuatkan sesuatu dari internet, ia akan menghantar pertanyaan bagi mendapatkan alamat IP domain tersebut (melalui DNS). MuteAds bertindak sebagai pengawal pintu setempat anda:

- Sekiranya domain tersebut berada dalam senarai iklan atau penjejak, MuteAds serta-merta menjawab: *"Tidak wujud (NXDOMAIN)"*. Sambungan tidak pernah dibuat, menjimatkan kuota data dan bateri.
- Sekiranya ia domain kandungan bersih biasa, pertanyaan dihantar dengan lancar ke pelayan DNS hulu standard dan laman dimuatkan seperti biasa dengan pantas.

Pada Android, ini dilaksanakan melalui **VPN setempat (Local VPN)** yang tidak pernah menghantar trafik ke pelayan luar. Pada komputer, MuteAds bertindak sebagai penyelesai DNS setempat. Dalam pelayar, sambungan memanfaatkan API rasmi berprestasi tinggi `declarativeNetRequest`.

## Privasi Diutamakan: Kami tidak inginkan data anda

- **Tiada akaun, tiada daftar masuk**: Kami tidak mempunyai borang pendaftaran dan tiada pangkalan data pengguna pusat.
- **100% dalam peranti**: Penapisan berjalan sepenuhnya pada peranti anda. Kami tidak mengendalikan sebarang pelayan yang dapat melihat sejarah pelayaran anda.
- **Kemas kini telus**: Satu-satunya aktiviti rangkaian automatik yang dilakukan oleh aplikasi adalah memuat turun senarai sekatan baharu kira-kira seminggu sekali.
- **Kebenaran minima**: Sambungan pelayar hanya meminta kebenaran yang benar-benar diperlukan untuk menyekat permintaan, menyimpan tetapan, pemasa mingguan, dan akses `youtube.com`.

## Perkara berguna untuk diketahui

- **Pengguna Android:** Pastikan untuk mematikan fungsi *Private DNS* dalam tetapan rangkaian telefon anda, jika tidak sistem akan memintas penapis setempat. Pastikan juga MuteAds dikecualikan daripada pengoptimuman bateri.
- **Iklan pihak pertama:** Sekatan DNS tidak dapat menapis iklan yang dihantar terus daripada domain yang sama dengan kandungan utama. Itulah sebabnya sambungan pelayar kami dilengkapi modul khas untuk YouTube.
- **Permainan kejar-mengejar YouTube:** Platform video sentiasa mengemas kini cara paparan iklan mereka. Jika iklan terlepas, pastikan sambungan anda dikemas kini ke versi terkini.

## Maklum Balas & Komuniti

Menjumpai laman yang ralat atau iklan yang terlepas? Sila buka [Issue](../../issues) dengan menyatakan alamat laman web dan tahap penapis yang anda gunakan. Setiap maklum balas anda amat kami hargai!

## Lesen & Penghargaan

Aplikasi Android dan proksi DNS mandiri dibina berasaskan projek sumber terbuka [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) oleh Ingo Zenz, dikeluarkan di bawah GNU General Public License v2 atau lebih baharu. Dikongsi secara terbuka untuk internet yang lebih bersih bagi semua.
