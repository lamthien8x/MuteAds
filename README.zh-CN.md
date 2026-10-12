<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds 图标">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  让手机、电脑和浏览器彻底告别广告与隐私追踪。<br>一个开关，五级过滤，无需注册账户，纯本地运行。
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <b>简体中文</b> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <a href="README.ko.md">한국어</a> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## 我们为什么打造 MuteAds

和大家一样，我们受够了如今充斥着喧嚣的互联网：闪烁刺眼的横幅广告、暗中记录一举一动的追踪脚本、电量飞速消耗，以及那些逐渐变得臃肿甚至出卖用户数据的拦截插件。我们怀着最纯粹的初衷打造了 MuteAds：在网络连接的最底层，将广告和追踪域名彻底拒之门外，甚至不给它们下载到屏幕上的机会。

无需 Root 权限，无需注册任何账号，更重要的是：**您的任何浏览历史与网络数据绝不会离开您的设备**。所有的过滤解析，100% 在您的本地硬件上独立完成。

- **基于域名的底层拦截**：跨越全系统所有应用生效（Android、电脑桌面端），或直接在主流浏览器内运行（扩展程序）。
- **五级精细化过滤档位**：从轻量温和的“基础级”（绝不误杀工作页面与企业内网）到严密防御的“极限级”。默认第 3 档（扩展级）是日常使用的黄金平衡点。
- **内置 YouTube 视频广告拦截**：浏览器扩展深度集成，打开开关即可享受清爽视频体验，告别烦人的插播广告。
- **极简单开关设计**：生活已经足够复杂，无需繁琐设置。临时排查网页问题？轻拨开关即可暂停，随时一键恢复。
- **原生加密 DNS 支持**：Android 与桌面端完整支持 DNS-over-HTTPS (DoH) 和 DNS-over-TLS (DoT)，有效阻断运营商及公共 Wi-Fi 的窥探。
- **掌控权完全在您手中**：支持自定义白名单、黑名单以及 IP 映射规则，原生支持 `*` 通配符匹配。

## 下载与版本动态

> MuteAds 目前处于早期发布阶段（v0.1）。我们正在全力打磨各平台体验并推进官方应用商店上架。在此期间，您可以直接在 [Releases](../../releases) 页面下载独立安装包。

| 平台 | 底层运行机制 | 当前状态 |
| --- | --- | --- |
| **Android** | 本地回环 VPN 拦截 DNS 查询，无需 Root 权限，支持 Android 4.2+ | 在 [Releases](../../releases) 下载 APK |
| **Windows** | 全系统本地 DNS 过滤服务（支持 x64、ARM64） | 已发布于 [Releases](../../releases) |
| **macOS** | 全系统本地 DNS 解析过滤程序 | 已发布于 [Releases](../../releases) |
| **Linux** | 独立 DNS 代理程序，支持单机或局域网全网防护（需 Java 环境） | 已发布于 [Releases](../../releases) |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | 轻量级高性能 MV3 浏览器扩展 | 商店审核筹备中 |
| **Firefox 128+** | 现代化高效浏览器扩展 | 商店审核筹备中 |

## 过滤级别说明

| 级别 | 档位名称 | 拦截策略与范围 |
| --- | --- | --- |
| 1 | 基础 (Basic) | 仅拦截危害最高的核心广告与追踪网络，几乎零误报风险。 |
| 2 | 平衡 (Balanced) | 拓展覆盖常见的大众统计平台与广告分发节点。 |
| 3 | 扩展 (Extended) | 覆盖全面的综合拦截方案，适合日常长期开启。**默认推荐档位。** |
| 4 | 严格 (Strict) | 强力阻断策略，极少数依赖第三方统计组件的站点可能偶发异常。 |
| 5 | 极限 (Maximum) | 启用全部拦截规则库（不含核心社交网络）。部分复杂网页可能需要手动加白。 |

💡 **开发者建议：** 若遇到某个特定网站页面加载不全，只需随手调低一级档位，或临时关闭开关片刻即可。

## 核心工作原理（绝无黑魔法）

每当应用程序或网页试图请求网络内容时，首先会向系统询问该域名对应的真实 IP 地址（即 DNS 查询）。MuteAds 在本地担任严密的门卫角色：

- 如果该域名属于广告网络、埋点追踪或遥测服务，MuteAds 会瞬间响应：*“该域名不存在 (NXDOMAIN)”*。数据连接自始至终不会建立，省流又省电。
- 如果是您主动访问的健康内容域名，查询将平滑透传给上游标准 DNS 服务器，页面即刻以原速飞快加载。

在 Android 上，这是通过系统内置的**本地回环 VPN** 实现的，绝不把任何流量送往外部服务器；在电脑端，应用成为系统专属的本地 DNS 解析器；在浏览器中，扩展利用浏览器原生高效的 `declarativeNetRequest` 引擎执行规则。

## 隐私承诺：我们不需要、也不收集您的任何数据

- **无账号体系，无登录要求**：我们没有注册表单，更没有中央用户数据库。
- **100% 运行于本地**：过滤纯粹发生在您的设备内部，我们没有运营任何会记录您访问历史的中间服务器。
- **透明更新机制**：程序唯一的对外静默网络动作，是大约每周一次从源站同步更新过滤规则库。
- **最小权限原则**：浏览器扩展仅申请网络拦截、本地配置持久化、每周更新定时器，以及对 `youtube.com` 的针对性必要权限。

## 使用贴士与常见注意事项

- **Android 用户提醒：** 请务必在系统网络设置中关闭 *私密 DNS (Private DNS)*，否则系统可能会绕过本地拦截。同时建议将 MuteAds 加入电池优化白名单。
- **第一方同源广告：** 纯 DNS 拦截无法剥离与正文共用同一主域名的广告（例如某些手机 App 的内置推广）。这也正是我们浏览器扩展专门为 YouTube 配备专属处理模块的原因。
- **YouTube 猫鼠博弈：** 视频平台的反拦截代码更迭频繁。若发现偶有广告漏网，请及时跟进并更新扩展至最新版。

## 反馈与交流

遇到了页面布局异常，或抓到了溜过封锁线的漏网之鱼？欢迎提交 [Issue](../../issues)，附上故障网址和您当时使用的过滤级别。每一个 issue 都是我们前行的动力！

## 开源协议与致谢

Android 客户端与独立 DNS 代理基于 Ingo Zenz 杰出的开源项目 [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter) 衍生开发，遵循 GNU General Public License v2 或更高版本开源协议。怀着对纯净互联网的追求，本项目免费且无担保向社区开放。
