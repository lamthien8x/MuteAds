<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Tắt sạch quảng cáo và theo dõi trên điện thoại, máy tính và trình duyệt của bạn.<br>Chỉ một công tắc, 5 mức lọc linh hoạt, không tài khoản, 100% xử lý tại máy.
</p>

<p align="center">
  <a href="README.md">English</a> · <b>Tiếng Việt</b> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## MuteAds sinh ra vì điều gì?

Chúng mình cũng như bạn: phát mệt vì mỗi lần mở web hay app là banner quảng cáo đập vào mắt, pin tụt không phanh, và các script theo dõi âm thầm ghi lại từng cú nhấp chuột. MuteAds được làm ra với một mục tiêu duy nhất: chặn đứng quảng cáo và tracker ngay từ gốc bằng cách từ chối kết nối tới tên miền của chúng trước khi chúng kịp xuất hiện trên màn hình.

Không cần root máy. Không cần đăng ký hay tạo tài khoản. Và quan trọng nhất: **không một byte dữ liệu duyệt web nào rời khỏi thiết bị của bạn**. Toàn bộ quá trình lọc diễn ra 100% nội bộ trên chính máy của bạn.

- **Chặn quảng cáo & tracker triệt để theo tên miền**: Bảo vệ toàn diện trên mọi ứng dụng (Android, máy tính) hoặc ngay trong trình duyệt quen thuộc của bạn (extension).
- **5 cấp độ lọc thông minh**: Từ "Cơ bản" (an toàn tuyệt đối, không sợ chặn nhầm trang làm việc) tới "Tối đa" (lá chắn quyền riêng tư thép). Mặc định là Mức 3 — điểm cân bằng hoàn hảo cho mọi nhu cầu.
- **Chặn quảng cáo YouTube tích hợp sẵn**: Có mặt ngay trong extension trình duyệt. Gạt công tắc là thưởng thức video mượt mà, không còn cảnh chờ 5 giây khó chịu.
- **Chỉ một công tắc bật/tắt**: Cuộc sống đã đủ phức tạp rồi. Khi cần tạm tắt để test trang web? Một cú nhấp là xong, mọi thứ lập tức trở về như cũ.
- **DNS mã hóa hiện đại**: Hỗ trợ đầy đủ DNS-over-HTTPS (DoH) và DNS-over-TLS (DoT) trên Android và máy tính, tránh bị nhà mạng hay mạng công cộng theo dõi thói quen duyệt web.
- **Toàn quyền kiểm soát**: Dễ dàng thêm quy tắc cá nhân với danh sách cho phép (allowlist), danh sách chặn (blocklist) và ánh xạ IP riêng biệt, hỗ trợ ký tự đại diện `*`.

## Tải về & Trải nghiệm

> MuteAds hiện đang ở phiên bản phát hành sớm (v0.1). Tụi mình đang tích cực hoàn thiện các bản đóng gói và gửi duyệt lên các cửa hàng chính thức. Bạn đã có thể tải trực tiếp file cài đặt tại trang [Releases](../../releases).

| Nền tảng | Cơ chế hoạt động | Tình trạng |
| --- | --- | --- |
| **Android** | VPN cục bộ lọc DNS ngay trên máy. Không cần root. Android 4.2+ | Tải APK tại [Releases](../../releases) |
| **Windows** | Bộ lọc DNS cục bộ cho toàn bộ hệ điều hành (x64, ARM64) | Có sẵn tại [Releases](../../releases) |
| **macOS** | Bộ lọc DNS cục bộ cho toàn hệ thống máy Mac | Có sẵn tại [Releases](../../releases) |
| **Linux** | DNS proxy độc lập cho máy cá nhân hoặc cả mạng nội bộ (cần Java) | Có sẵn tại [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extension trình duyệt MV3 siêu nhẹ, tối ưu hiệu năng | Đang chuẩn bị lên Chrome Web Store |
| **Firefox 128+** | Extension trình duyệt hiện đại | Đang chuẩn bị lên Firefox Add-ons |

## Các mức lọc

| Mức | Tên gọi | Phạm vi chặn |
| --- | --- | --- |
| 1 | Cơ bản | Chỉ chặn các mạng quảng cáo và theo dõi ưu tiên cao nhất. Hầu như không bao giờ chặn nhầm. |
| 2 | Cân bằng | Mở rộng độ phủ thêm nhiều nền tảng phân tích và thu thập số liệu phổ biến. |
| 3 | Mở rộng | Độ phủ toàn diện cho lướt web hàng ngày. **Mặc định khuyến nghị.** |
| 4 | Nghiêm ngặt | Lọc quyết liệt. Thỉnh thoảng có thể ảnh hưởng tới các widget nhúng từ bên thứ ba. |
| 5 | Tối đa | Áp dụng toàn bộ danh sách chặn (trừ mạng xã hội chính). Vài trang web phức tạp có thể cần đưa vào allowlist. |

💡 **Mẹo nhỏ từ dev:** Nếu một trang web nào đó hiển thị thiếu nội dung, bạn chỉ cần hạ mức lọc xuống một nấc hoặc tắt tạm công tắc trong chốc lát nhé.

## Cơ chế hoạt động (Không có phép thuật đen nào ở đây cả!)

Mỗi khi một ứng dụng hay trang web muốn tải thứ gì đó từ internet, việc đầu tiên nó làm là gửi truy vấn hỏi địa chỉ IP của tên miền đó (qua DNS). MuteAds đóng vai trò người gác cổng tin cậy ngay tại máy:

- Nếu tên miền đó nằm trong danh sách máy chủ quảng cáo/theo dõi, MuteAds trả lời ngay: *"Tên miền không tồn tại"*. Nhờ đó quảng cáo không bao giờ được tải về — tiết kiệm băng thông và nhẹ gánh CPU.
- Nếu đó là tên miền nội dung sạch mà bạn muốn truy cập, yêu cầu được chuyển tiếp tức thì tới máy chủ DNS tiêu chuẩn và tải vù vù như bình thường.

Trên Android, điều này được thực hiện qua **VPN cục bộ (Local VPN)** chạy hoàn toàn khép kín trên máy — không có giọt lưu lượng nào bị đẩy ra máy chủ ngoài. Trên máy tính, MuteAds đóng vai trò máy chủ DNS nội bộ. Còn trên trình duyệt, extension tận dụng API hiệu năng cao của trình duyệt (`declarativeNetRequest`) với cùng bộ danh sách đó.

## Cam kết quyền riêng tư: Tụi mình không muốn dữ liệu của bạn

- **Không tài khoản, không đăng nhập**: Tụi mình không hề có form đăng ký và không có bất kỳ cơ sở dữ liệu người dùng nào.
- **100% trên thiết bị**: Toàn bộ quá trình lọc chạy nội bộ. Tụi mình không vận hành máy chủ trung gian nào có thể nhìn thấy các trang web bạn truy cập.
- **Cập nhật sạch sẽ**: Dữ liệu mạng duy nhất mà app tự động tải về là danh sách tên miền chặn được làm mới định kỳ khoảng 1 tuần/lần.
- **Quyền tối thiểu**: Extension trình duyệt chỉ xin những quyền thật sự cần: chặn truy vấn mạng, lưu cấu hình cá nhân, hẹn giờ làm mới danh sách, và quyền trên `youtube.com` để xử lý quảng cáo video.

## Vài điều lưu ý bỏ túi

- **Dành cho Android:** Hãy nhớ tắt tính năng *Private DNS (DNS riêng tư)* trong cài đặt mạng của điện thoại nhé, nếu không Android sẽ tự ý đi đường vòng và bỏ qua bộ lọc. Đồng thời, nhớ tắt chế độ tối ưu hóa pin cho MuteAds để không bị hệ thống tắt ngầm.
- **Quảng cáo cùng tên miền:** Chặn theo DNS không thể can thiệp vào các quảng cáo phát từ chính tên miền của nội dung gốc (ví dụ trong một số ứng dụng di động). Đó là lý do tại sao bản extension trình duyệt được trang bị thêm bộ xử lý chuyên biệt cho YouTube.
- **Trò chơi mèo vờn chuột trên YouTube:** YouTube liên tục thử nghiệm các thuật toán chèn quảng cáo mới. Nếu bạn thấy quảng cáo lọt qua, hãy ghé kiểm tra và cập nhật extension lên bản mới nhất nhé!

## Góp ý & Cùng nhau hoàn thiện

Bạn phát hiện một trang web bị lỗi hiển thị hay một quảng cáo cứng đầu lọt lưới? Hãy mở một [Issue](../../issues) kèm theo đường dẫn trang và mức lọc bạn đang dùng nhé. Tụi mình đọc từng góp ý và rất biết ơn sự đồng hành của bạn!

## Giấy phép & Lời cảm ơn

Ứng dụng Android và DNS proxy độc lập kế thừa và phát triển từ nền tảng mã nguồn mở tuyệt vời [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) của tác giả Ingo Zenz, phát hành theo GNU General Public License v2 hoặc mới hơn. Dự án được chia sẻ hoàn toàn mở với mong muốn mang lại trải nghiệm internet trong lành cho mọi người.
