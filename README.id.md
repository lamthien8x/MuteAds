<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Hentikan iklan dan pelacak di ponsel, komputer, dan browser Anda.<br>Satu sakelar, lima level filter, tanpa akun, 100% lokal di perangkat Anda.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <b>Bahasa Indonesia</b> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## Mengapa kami membuat MuteAds

Sama seperti Anda, kami lelah dengan internet modern: spanduk iklan yang mengganggu, skrip pelacak yang memata-matai setiap ketukan, baterai boros, serta pemblokir iklan berat yang memperlambat sistem atau menjual data pengguna. MuteAds lahir dengan satu tujuan sederhana: memotong iklan dan pelacak langsung dari akarnya dengan menolak koneksi ke domain mereka sebelum sempat muncul di layar.

Tanpa perlu root. Tanpa perlu registrasi akun. Dan yang paling penting: **tidak ada satu bita pun riwayat penelusuran Anda yang dikirim ke luar perangkat**. Seluruh pemfilteran berlangsung 100% di perangkat Anda sendiri.

- **Pemblokiran berbasis domain yang andal**: Bekerja di semua aplikasi sistem (Android, desktop) atau langsung di dalam browser favorit Anda (ekstensi).
- **5 level filter fleksibel**: Dari level "Dasar" (sangat aman, tidak merusak web pekerjaan) hingga level "Maksimum". Level 3 adalah bawaan yang seimbang untuk sehari-hari.
- **Blokir iklan YouTube terintegrasi**: Tertanam langsung di ekstensi browser. Cukup nyalakan sakelar dan nikmati video tanpa interupsi.
- **Satu sakelar utama**: Hidup sudah cukup rumit. Perlu menonaktifkan filter sejenak? Sekali klik selesai, semua kembali seperti semula seketika.
- **DNS terenkripsi modern**: Dukungan penuh untuk DNS-over-HTTPS (DoH) dan DNS-over-TLS (DoT) di Android dan desktop agar terlindung dari intipan ISP.
- **Kendali aturan di tangan Anda**: Dukungan penuh daftar izin (allowlist), daftar blokir (blocklist), dan pemetaan IP kustom dengan wildcard `*`.

## Unduhan & Rilis Awal

> MuteAds saat ini berada dalam tahap rilis awal (v0.1). Kami sedang mempersiapkan pendaftaran di toko ekstensi resmi. Untuk saat ini, penginstal langsung tersedia di halaman [Releases](../../releases).

| Platform | Cara kerja internal | Status |
| --- | --- | --- |
| **Android** | VPN lokal loopback menyaring DNS di perangkat. Tanpa root. Android 4.2+ | APK di [Releases](../../releases) |
| **Windows** | Filter DNS lokal untuk seluruh komputer (x64, ARM64) | Tersedia di [Releases](../../releases) |
| **macOS** | Filter DNS lokal untuk seluruh sistem Mac | Tersedia di [Releases](../../releases) |
| **Linux** | Proksi DNS mandiri untuk PC atau seluruh jaringan lokal (butuh Java) | Tersedia di [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Ekstensi browser MV3 yang ringan dan efisien | Persiapan peninjauan toko |
| **Firefox 128+** | Ekstensi browser deklaratif berkecepatan tinggi | Persiapan peninjauan toko |

## Tingkat Filter

| Tingkat | Profil | Cakupan Blokir |
| --- | --- | --- |
| 1 | Dasar (Basic) | Hanya domain iklan dan pelacak prioritas tertinggi. Risiko salah blokir paling rendah. |
| 2 | Seimbang (Balanced) | Cakupan lebih luas termasuk platform analitik populer. |
| 3 | Diperluas (Extended) | Perlindungan komprehensif untuk penggunaan harian. **Bawaan disarankan.** |
| 4 | Ketat (Strict) | Penyaringan agresif. Mungkin memengaruhi widget pihak ketiga di beberapa situs. |
| 5 | Maksimum (Maximum) | Menerapkan seluruh daftar kecuali media sosial utama. Beberapa situs rumit mungkin perlu izin manual. |

💡 **Tips pengembang:** Jika sebuah situs bermasalah, cukup turunkan satu level atau matikan sakelar untuk sesaat.

## Cara kerja (Tanpa sihir hitam!)

Setiap kali aplikasi atau halaman web ingin memuat sesuatu, hal pertama yang dilakukannya adalah menanyakan alamat IP dari nama domain tersebut (melalui kueri DNS). MuteAds bertindak sebagai penjaga gerbang lokal Anda:

- Jika domain tersebut milik jaringan iklan atau pelacak, MuteAds langsung menjawab: *"Tidak ada / NXDOMAIN"*. Sambungan tidak pernah terjadi, menghemat kuota data dan daya baterai.
- Jika itu adalah konten bersih yang Anda inginkan, kueri diteruskan dengan mulus ke server DNS hulu standar dan halaman terbuka secepat kilat.

Di Android, ini berjalan melalui **VPN loopback lokal** yang tidak pernah mengirim lalu lintas ke luar ponsel. Di komputer, aplikasi menjadi resolver DNS lokal mesin Anda. Di browser, ekstensi menggunakan API resmi berkecepatan tinggi `declarativeNetRequest`.

## Privasi: Kami tidak menginginkan data Anda

- **Tanpa akun, tanpa masuk**: Kami tidak memiliki formulir pendaftaran dan tidak memiliki basis data pengguna terpusat.
- **100% di perangkat Anda**: Pemfilteran berjalan lokal. Kami tidak mengoperasikan server perantara yang dapat melihat situs yang Anda kunjungi.
- **Pembaruan transparan**: Satu-satunya unduhan otomatis yang dilakukan aplikasi adalah daftar domain blokir baru sekitar seminggu sekali.
- **Izin minimal**: Ekstensi browser hanya meminta izin yang mutlak diperlukan untuk memblokir permintaan, menyimpan setelan, timer mingguan, dan akses `youtube.com`.

## Hal penting yang perlu diketahui

- **Pengguna Android:** Pastikan untuk mematikan fitur *Private DNS* di pengaturan jaringan ponsel Anda, agar sistem tidak melewati filter lokal. Jangan lupa kecualikan MuteAds dari penghemat baterai.
- **Iklan pihak pertama:** Pemblokiran berbasis DNS murni tidak dapat menyaring iklan yang disajikan dari domain yang sama dengan konten utama. Oleh karena itu, ekstensi browser kami memiliki modul khusus untuk YouTube.
- **Kucing dan tikus di YouTube:** Platform video sering memperbarui skrip penayangan iklannya. Jika iklan muncul kembali, pastikan Anda memperbarui ekstensi ke versi terbaru.

## Masukan & Komunitas

Menemukan situs yang tampil rusak atau iklan yang lolos dari filter? Buka [Issue](../../issues) dengan menyertakan alamat web dan level filter yang Anda gunakan. Setiap masukan dari Anda sangat berarti!

## Lisensi & Ucapan Terima Kasih

Aplikasi Android dan proksi DNS mandiri dibangun berdasarkan proyek sumber terbuka yang hebat [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) oleh Ingo Zenz, dirilis di bawah lisensi GNU General Public License v2 atau lebih baru. Didistribusikan secara bebas untuk internet yang lebih bersih.
