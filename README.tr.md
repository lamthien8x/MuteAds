<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds Logosu">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Telefonunuzda, bilgisayarınızda ve tarayıcınızda reklamları ve takipçileri susturun.<br>Tek anahtar, beş filtre seviyesi, hesap yok, %100 yerel cihazınızda.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <b>Türkçe</b> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## MuteAds'i Neden Geliştirdik

Tıpkı sizin gibi biz de modern internetten yorulduk: her köşede yanıp sönen reklam panoları, her tıklamayı kaydeden casus takip kodları, hızla tükenen bataryalar ve bilgisayarı hantallaştıran ya da kullanıcı verilerini pazarlayan ağır reklam engelleyiciler. MuteAds'i tek ve net bir hedefle geliştirdik: reklam ve takipçileri daha ekranınıza ulaşmadan, alan adlarına giden bağlantıları kökten keserek engellemek.

Root yetkisi gerekmez. Hesap açmak veya kayıt olmak gerekmez. Ve en önemlisi: **gezinme geçmişinizin tek bir baytı bile cihazınızın dışına çıkmaz**. Tüm filtreleme %100 yerel olarak kendi donanımınızda gerçekleşir.

- **Alan adı düzeyinde kusursuz engelleme**: Cihazınızdaki tüm uygulamalarda (Android, masaüstü PC) veya doğrudan tarayıcınızın içinde (uzantı) sorunsuz çalışır.
- **5 esnek filtre seviyesi**: İş sitelerini bozmayan son derece güvenli "Temel" seviyeden "Maksimum" seviyeye kadar. Varsayılan seviye 3 en ideal dengedir.
- **Yerleşik YouTube reklam engelleme**: Tarayıcı uzantısına doğrudan entegre edilmiştir. Anahtarı açın ve videoları sinir bozucu reklam araları olmadan izleyin.
- **Tek bir ana kontrol anahtarı**: Hayat zaten yeterince karmaşık. Bir siteyi test etmek için filtreyi geçici olarak kapatmak mı gerekiyor? Tek tıkla kapatın, her şey anında eski haline dönsün.
- **Modern şifreli DNS**: İnternet servis sağlayıcılarının gözetlemesini önlemek için Android ve masaüstünde tam DNS-over-HTTPS (DoH) ve DNS-over-TLS (DoT) desteği.
- **Tam kural hakimiyeti**: İzin verilenler listesi (allowlist), engellenenler listesi (blocklist) ve joker karakterli `*` özel IP eşlemeleri oluşturma özgürlüğü.

## İndirme ve Güncel Durum

> MuteAds şu anda erken erişim aşamasındadır (v0.1). Resmi mağaza yayınları hazırlanmaktadır. Bu süreçte doğrudan yükleyicileri [Releases](../../releases) sayfasından hemen indirebilirsiniz.

| Platform | İç çalışma mekanizması | Durum |
| --- | --- | --- |
| **Android** | Cihaz üzerinde DNS filtreleyen yerel loopback VPN. Root gerekmez. Android 4.2+ | [Releases](../../releases) sayfasında APK |
| **Windows** | Tüm bilgisayar için yerel DNS filtreleme hizmeti (x64, ARM64) | [Releases](../../releases) sayfasında mevcut |
| **macOS** | Mac sisteminin tamamı için yerel DNS filtresi | [Releases](../../releases) sayfasında mevcut |
| **Linux** | Tek bir PC veya tüm ev ağı için bağımsız DNS proxy (Java gerektirir) | [Releases](../../releases) sayfasında mevcut |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Hafif ve yüksek performanslı MV3 tarayıcı uzantısı | Mağaza incelemesi hazırlanıyor |
| **Firefox 128+** | Hızlı ve bildirimsel tarayıcı uzantısı | Eklenti incelemesi hazırlanıyor |

## Filtre Seviyeleri

| Seviye | Profil | Neler Engellenir |
| --- | --- | --- |
| 1 | Temel (Basic) | Yalnızca en yüksek öncelikli reklam ve takip alan adları. Yanlış engelleme riski neredeyse sıfırdır. |
| 2 | Dengeli (Balanced) | Yaygın analiz ve telemetri platformlarını da içeren daha geniş kapsam. |
| 3 | Genişletilmiş (Extended) | Günlük internet gezintisi için kapsamlı koruma. **Önerilen varsayılan.** |
| 4 | Katı (Strict) | Agresif filtreleme. Bazen üçüncü taraf gömülü bileşenleri etkileyebilir. |
| 5 | Maksimum (Maximum) | Temel sosyal ağlar hariç tüm engelleme listesini uygular. Bazı karmaşık sitelerde istisna eklemek gerekebilir. |

💡 **Geliştirici ipucu:** Bir web sitesi düzgün yüklenmezse, filtreyi bir kademe düşürün veya anahtarı birkaç saniyeliğine kapatın.

## Nasıl Çalışır (Sihirbazlık Değil!)

Bir uygulama veya web sayfası internetten bir şey yüklemek istediğinde, önce alan adının arkasındaki IP adresini sorgular (DNS sorgusu). MuteAds burada sizin yerel kapı bekçiniz olur:

- Alan adı bir reklam veya takip ağına aitse, MuteAds hemen yanıt verir: *"Mevcut değil (NXDOMAIN)"*. Bağlantı hiç kurulmaz, veri paketinizden ve pilinizden tasarruf edilir.
- Ziyaret etmek istediğiniz meşru bir içerikse, sorgu standart DNS sunucunuza sorunsuzca iletilir ve sayfa tam hızda açılır.

Android'de bu işlem, telefon dışına asla veri göndermeyen **yerel bir loopback VPN** üzerinden yürütülür. Bilgisayarda MuteAds sistemin yerel DNS çözücüsü haline gelir. Tarayıcıda ise uzantı resmi yüksek hızlı `declarativeNetRequest` motorunu kullanır.

## Önce Gizlilik: Verilerinizle İlgilenmiyoruz

- **Hesap yok, giriş yok**: Kayıt formumuz ve merkezi bir kullanıcı veritabanımız bulunmamaktadır.
- **%100 cihazınızda**: Filtreleme tamamen yerel olarak çalışır. Gezindiğiniz siteleri izleyen veya kaydeden hiçbir sunucu işletmiyoruz.
- **Şeffaf güncellemeler**: Uygulamanın otomatik olarak yaptığı tek ağ işlemi, haftada yaklaşık bir kez güncellenen alan adı listesini indirmektir.
- **Minimum izinler**: Tarayıcı uzantısı yalnızca istekleri engellemek, ayarları kaydetmek, haftalık zamanlayıcıyı çalıştırmak ve `youtube.com` üzerinde reklam engellemek için gereken izinleri ister.

## Faydalı Bilgiler

- **Android kullanıcıları için:** Telefonunuzun ağ ayarlarındaki *Özel DNS (Private DNS)* seçeneğini mutlaka kapatın, aksi takdirde Android yerel filtreyi atlar. Ayrıca MuteAds için pil optimizasyonunu devre dışı bırakın.
- **Aynı alan adından gelen reklamlar:** Saf DNS filtreleme, ana içerikle aynı alan adından sunulan reklamları ayıramaz. Bu nedenle tarayıcı uzantımızda YouTube için özel bir engelleyici motor yer alır.
- **YouTube ile kedi-fare oyunu:** Video platformları reklam yöntemlerini sık sık değiştirir. Bir reklam kaçarsa uzantıyı en son sürüme güncellediğinizden emin olun.

## Geri Bildirim & Topluluk

Bozuk bir sayfa veya filtreden kaçan inatçı bir reklam mı gördünüz? Sayfa adresini ve kullandığınız filtre seviyesini belirterek [Issues](../../issues) sayfasında bir konu açın. Her geri bildiriminiz bizim için çok değerlidir!

## Lisans & Teşekkür

Android uygulaması ve bağımsız DNS proxy'si, Ingo Zenz tarafından geliştirilen harika açık kaynaklı [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) projesine dayanır ve GNU GPL v2 veya üzeri lisansla dağıtılır. Daha temiz bir internet için sevgiyle üretilmiştir.
