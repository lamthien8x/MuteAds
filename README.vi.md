<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="Logo MuteAds">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  Chặn quảng cáo và trình theo dõi trên điện thoại, máy tính và trình duyệt.<br>
  Một nút bật/tắt, năm mức lọc, không cần tài khoản.
</p>

<p align="center">
  <a href="README.md">English</a> · <b>Tiếng Việt</b>
</p>

---

## MuteAds làm gì

MuteAds chặn quảng cáo và trình theo dõi bằng cách từ chối kết nối tới các tên miền phát ra chúng. Không cần root, không cần tài khoản, và không gửi lịch sử duyệt web của bạn đi đâu: việc lọc diễn ra ngay trên thiết bị của bạn.

- **Chặn quảng cáo và trình theo dõi theo tên miền**, cho mọi ứng dụng trên máy (Android, máy tính) hoặc trong trình duyệt (extension).
- **Năm mức lọc**, từ "Cơ bản" (ít chặn nhầm nhất) tới "Tối đa" (chặn nhiều nhất, một số trang có thể lỗi). Mặc định là mức 3.
- **Chặn quảng cáo YouTube** trong extension trình duyệt, có tác dụng ngay khi bật nút nguồn.
- **Một nút bật/tắt.** Tắt đi là mọi thứ trở lại như cũ.
- **DNS mã hoá**: hỗ trợ DNS-over-HTTPS và DNS-over-TLS trên Android và máy tính.
- **Quy tắc riêng**: danh sách cho phép, danh sách chặn và ánh xạ IP tuỳ chỉnh, có ký tự đại diện `*`.

## Tải về

> MuteAds đang ở giai đoạn phát hành sớm (phiên bản 0.1). File cài được đăng ở trang [Releases](../../releases) khi sẵn sàng. Bản trên các cửa hàng extension đang được chuẩn bị.

| Nền tảng | Cách hoạt động | Tình trạng |
| --- | --- | --- |
| **Android** | VPN cục bộ lọc DNS ngay trên máy. Không cần root. Android 4.2 trở lên | APK ở [Releases](../../releases) |
| **Windows** | Bộ lọc DNS cục bộ cho cả máy tính (x64, ARM64) | Ở [Releases](../../releases) |
| **macOS** | Bộ lọc DNS cục bộ cho cả máy tính | Ở [Releases](../../releases) |
| **Linux** | DNS proxy cho một máy hoặc cả mạng nội bộ (cần Java) | Ở [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | Extension trình duyệt | Đang chuẩn bị đưa lên cửa hàng |
| **Firefox** 128 trở lên | Extension trình duyệt | Đang chuẩn bị đưa lên cửa hàng |

## Các mức lọc

| Mức | Tên | Chặn những gì |
| --- | --- | --- |
| 1 | Cơ bản | Chỉ nhóm tên miền ưu tiên cao nhất. Ít chặn nhầm nhất. |
| 2 | Cân bằng | Mở rộng phạm vi chặn. |
| 3 | Mở rộng | Phạm vi chặn rộng. **Mặc định.** |
| 4 | Nghiêm ngặt | Phủ rất rộng. Bắt đầu có nguy cơ chặn nhầm. |
| 5 | Tối đa | Toàn bộ danh sách, trừ mạng xã hội. Một số trang có thể hiển thị lỗi. |

Nếu một trang web không chạy, hãy hạ mức lọc hoặc tắt nút nguồn một lúc.

## Cách hoạt động

Mỗi khi một ứng dụng hay trang web muốn tải thứ gì đó, trước tiên nó hỏi địa chỉ của một tên miền. MuteAds tự trả lời câu hỏi đó:

- Nếu tên miền nằm trong danh sách chặn, MuteAds trả lời "không có", và quảng cáo hay trình theo dõi không bao giờ được tải.
- Nếu không, câu hỏi được chuyển tới máy chủ DNS bình thường và trang tải như mọi khi.

Trên Android, việc này chạy qua một VPN cục bộ nằm ngay trên máy; không có lưu lượng nào được gửi tới máy chủ của MuteAds. Trên máy tính, ứng dụng trở thành máy chủ DNS của chính máy bạn. Extension trình duyệt dùng API chặn có sẵn của trình duyệt (`declarativeNetRequest`) với cùng danh sách.

## Quyền riêng tư

- Không tài khoản, không đăng ký.
- Việc lọc chạy trên thiết bị của bạn. MuteAds không có máy chủ nào nhìn thấy các trang bạn truy cập.
- Thứ duy nhất ứng dụng tự tải về là danh sách chặn, làm mới khoảng mỗi tuần một lần.
- Extension trình duyệt chỉ xin những quyền nó dùng: chặn yêu cầu, lưu cài đặt, hẹn giờ làm mới hằng tuần, và truy cập `youtube.com` để chặn quảng cáo YouTube.

## Nên biết

- **Android:** tắt *Private DNS* trong cài đặt mạng, nếu không bộ lọc sẽ bị bỏ qua. Cho phép ứng dụng chạy nền không bị tối ưu hoá pin.
- Chặn theo tên miền không gỡ được quảng cáo phát từ cùng tên miền với nội dung (ví dụ trong một số ứng dụng di động). Vì vậy extension trình duyệt xử lý riêng YouTube.
- YouTube thay đổi thường xuyên. Nếu quảng cáo quay lại, hãy cập nhật bản mới nhất.

## Góp ý

Gặp trang bị lỗi, hoặc quảng cáo lọt qua? Hãy mở một [issue](../../issues), kèm địa chỉ trang và mức lọc bạn đang dùng.

## Giấy phép

Ứng dụng Android và DNS proxy độc lập được phát triển từ [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter), phát hành theo GNU General Public License phiên bản 2 hoặc mới hơn. Chương trình được cung cấp không kèm bất kỳ bảo đảm nào.
