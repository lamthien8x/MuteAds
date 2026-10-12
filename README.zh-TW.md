<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds 標誌">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  為您的手機、電腦與瀏覽器帶來徹底的寧靜，告別廣告與隱私追蹤。<br>單一開關，五段過濾等級，無需帳號，完全本機運算。
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <b>繁體中文</b> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## 我們為什麼打造 MuteAds

和大家一樣，我們厭倦了喧囂的網路環境：刺眼的橫幅廣告、無處不在的追蹤程式碼、無端耗損的電池電力，以及那些逐漸臃腫、甚至出賣用戶資料的阻擋擴充功能。我們打造 MuteAds 的核心初衷非常單純：在最底層拒絕與廣告和追蹤網域建立連線，在它們抵達螢幕之前就乾淨俐落地阻截。

無需 Root 權限，無需註冊任何帳號，更重要的是：**您的任何瀏覽活動資料絕不會離開您的裝置**。所有解析與過濾，100% 在您的本機硬體上獨立運作。

- **網域層級的深層阻截**：跨越全系統應用程式生效（Android、電腦桌面端），亦可直接於瀏覽器內運行（擴充功能）。
- **五段精準過濾等級**：從極度溫和的「基礎級」（絕不誤殺工作頁面）到銅牆鐵壁的「極限級」。預設第 3 級是兼顧潔淨與穩定的最佳平衡點。
- **內建 YouTube 影片廣告阻擋**：深度整合於瀏覽器擴充功能中，開啟開關即可享受流暢無中斷的影音體驗。
- **極簡單一開關**：生活已足夠繁複，無需多餘設定。需要暫時排除網頁異常？輕按一下即可停用，隨時一鍵恢復。
- **原生加密 DNS 支援**：Android 與電腦端完整支援 DNS-over-HTTPS (DoH) 及 DNS-over-TLS (DoT)，有效阻絕電信業者與公共 Wi-Fi 的窺探。
- **自主規則掌控**：自由建立自訂允許清單、封鎖清單與專屬 IP 映射，原生支援 `*` 萬用字元比對。

## 下載與最新動態

> MuteAds 目前處於早期預覽階段（v0.1）。我們正全力優化各平台體驗並籌備官方商店上架。在此期間，您可直接前往 [Releases](../../releases) 頁面下載安裝檔。

| 作業平台 | 底層運作機制 | 目前狀態 |
| --- | --- | --- |
| **Android** | 本機環回 VPN 於裝置內過濾 DNS，免 Root，支援 Android 4.2+ | 前往 [Releases](../../releases) 下載 APK |
| **Windows** | 全系統本機 DNS 過濾服務（支援 x64、ARM64） | 已發佈於 [Releases](../../releases) |
| **macOS** | 全系統本機 DNS 解析過濾工具 | 已發佈於 [Releases](../../releases) |
| **Linux** | 獨立 DNS 代理服務，支援單機或全區域網路（需具備 Java） | 已發佈於 [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | 超輕量高性能 MV3 瀏覽器擴充功能 | 商店審核準備中 |
| **Firefox 128+** | 現代化高效率瀏覽器擴充功能 | 商店審核準備中 |

## 過濾等級說明

| 等級 | 設定檔名稱 | 阻擋策略與範疇 |
| --- | --- | --- |
| 1 | 基礎 (Basic) | 僅針對威脅最高的核心廣告與追蹤網域，極低誤判率。 |
| 2 | 平衡 (Balanced) | 擴大阻擋範圍，涵蓋常見的分析統計平台與遙測伺服器。 |
| 3 | 延伸 (Extended) | 全方位的日常阻截方案。**預設推薦等級。** |
| 4 | 嚴格 (Strict) | 強力防禦模式，極少數仰賴第三方外掛元件的網站可能受影響。 |
| 5 | 極限 (Maximum) | 套用完整阻擋清單（排除主要社交平台）。部分精密網站可能需加入白名單。 |

💡 **開發者秘訣：** 若遇特定網頁無法正常載入，只需將等級稍微調低一階，或暫時切換開關即可。

## 核心運作原理（絕無黑魔法）

每當應用程式或瀏覽器嘗試連線時，第一步皆是向系統查詢網域名稱對應的 IP 位址（DNS 查詢）。MuteAds 在本機扮演忠誠的守門人：

- 若該網域屬於廣告商、行為追蹤或遙測伺服器，MuteAds 立即回覆：*「查無此網域 (NXDOMAIN)」*。連線根本不會建立，省下寶貴的頻寬與電池電力。
- 若屬於您正常存取的潔淨內容網域，查詢會順暢轉發至標準上游 DNS 伺服器，頁面原速流暢載入。

在 Android 上，這是透過系統的**本機端 VPN** 達成，絕無封包傳輸至外部伺服器；在電腦端，MuteAds 成為電腦的本機 DNS 解析器；在瀏覽器內，擴充功能運用瀏覽器高效的 `declarativeNetRequest` 引擎嚴格執行規則。

## 隱私承諾：我們絕不收集您的資料

- **無註冊機制、免登入**：我們完全沒有會員註冊表單，亦無中央伺服器資料庫。
- **完全本機運作**：所有防護均在您的設備上完成。我們沒有設立任何能監視或記錄您上網軌跡的中繼伺服器。
- **純粹定期更新**：程式唯一自動執行的網路動作，約為每週一次自官方同步更新網域黑名單。
- **遵循最小權限**：瀏覽器擴充功能僅索取執行阻擋、儲存個人設定、每週更新排程以及 `youtube.com` 專屬之必要權限。

## 實用小貼士與注意事項

- **Android 使用者：** 請確認已至手機網路設定中關閉 *私人 DNS (Private DNS)*，否則系統會略過本機過濾。亦建議將 MuteAds 排除於系統電池最佳化之外。
- **同源廣告限制：** 純 DNS 阻擋無法攔截與本文內容位於相同主網域的廣告（如部分手機 App 內嵌廣告）。這也是為何瀏覽器擴充功能特別為 YouTube 開發專屬模組的原因。
- **YouTube 攻防更新：** 影音平台常動態調整廣告投放技術。若偶有廣告漏網，請隨時將擴充功能更新至最新版本。

## 意見回饋與社群交流

發現某個網站版面跑版，或是抓到了頑固漏網的廣告？歡迎前往 [Issues](../../issues) 提交回報，請附上網址與當時所設定的過濾等級。您的每份回饋都是我們持續進步的動力！

## 授權協議與致謝

Android 應用程式與獨立 DNS 代理是基於 Ingo Zenz 優秀的開源專案 [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) 進一步研發，遵循 GNU General Public License v2 或後續版本發佈。本專案完全以開源精神分享，不提供任何明示或暗示之擔保。
