<p align="center">
  <img src="assets/logo.svg" width="96" height="96" alt="MuteAds 로고">
</p>

<h1 align="center">MuteAds</h1>

<p align="center">
  스마트폰, 컴퓨터, 브라우저에서 광고와 추적기를 완벽히 잠재우세요.<br>원클릭 스위치, 5단계 맞춤 필터, 계정 불필요, 100% 로컬 기기 처리.
</p>

<p align="center">
  <a href="README.md">English</a> · <a href="README.vi.md">Tiếng Việt</a> · <a href="README.zh-CN.md">简体中文</a> · <a href="README.zh-TW.md">繁體中文</a> · <a href="README.ja.md">日本語</a> · <b>한국어</b> · <a href="README.id.md">Bahasa Indonesia</a> · <a href="README.ms.md">Bahasa Melayu</a> · <a href="README.es.md">Español</a> · <a href="README.fr.md">Français</a><br>
  <a href="README.de.md">Deutsch</a> · <a href="README.pt.md">Português</a> · <a href="README.it.md">Italiano</a> · <a href="README.nl.md">Nederlands</a> · <a href="README.pl.md">Polski</a> · <a href="README.sv.md">Svenska</a> · <a href="README.ru.md">Русский</a> · <a href="README.uk.md">Українська</a> · <a href="README.cs.md">Čeština</a> · <a href="README.ro.md">Română</a><br>
  <a href="README.hu.md">Magyar</a> · <a href="README.el.md">Ελληνικά</a> · <a href="README.tr.md">Türkçe</a> · <a href="README.ar.md">العربية</a> · <a href="README.fa.md">فارسی</a> · <a href="README.he.md">עברית</a> · <a href="README.hi.md">हिन्दी</a> · <a href="README.bn.md">বাংলা</a> · <a href="README.th.md">ไทย</a> · <a href="README.fil.md">Filipino</a>
</p>

---

## 우리가 MuteAds를 만든 이유

저희 역시 여러분처럼 피로감을 느꼈습니다. 화면을 뒤덮는 깜빡이는 배너, 클릭 하나하나를 감시하는 추적 스크립트, 줄줄 새는 배터리, 그리고 어느새 무거워지고 개인정보를 팔아넘기는 광고 차단 확장 프로그램들까지 말이죠. 그래서 MuteAds를 만들었습니다. 광고와 트래커 도메인으로 향하는 연결 자체를 화면에 닿기도 전에 원천 차단하는 것입니다.

루팅(Root)이 필요 없습니다. 회원가입이나 계정도 필요 없습니다. 그리고 가장 중요한 점은, **여러분의 브라우징 기록과 데이터는 단 1바이트도 기기 밖으로 나가지 않습니다**. 모든 필터링은 여러분의 기기 내부에서 100% 처리됩니다.

- **도메인 레벨의 깔끔한 원천 차단**: 기기 내 모든 앱(Android, PC 데스크톱) 또는 브라우저 내부(확장 프로그램)에서 강력하게 작동합니다.
- **섬세한 5단계 필터 레벨**: 업무용 사이트가 깨지지 않는 안전한 '기본(Basic)'부터 강력한 '최대(Maximum)'까지. 기본값인 3단계가 가장 쾌적합니다.
- **YouTube 광고 차단 내장**: 브라우저 확장 프로그램에 기본 탑재되어 스위치를 켜는 즉시 중간 광고 없이 영상을 감상할 수 있습니다.
- **간편한 원스위치 제어**: 인생은 이미 충분히 복잡합니다. 일시적으로 차단을 해제해야 할 때도 스위치 하나만 끄면 즉시 원래대로 돌아옵니다.
- **최신 암호화 DNS 지원**: Android 및 데스크톱에서 DNS-over-HTTPS (DoH)와 DNS-over-TLS (DoT)를 완벽 지원하여 통신사 도청을 방지합니다.
- **완전한 사용자 커스텀 규칙**: 허용 목록(Allowlist), 차단 목록(Blocklist), 사용자 지정 IP 매핑과 `*` 와일드카드를 자유롭게 지원합니다.

## 다운로드 및 출시 안내

> MuteAds는 현재 초기 공개 단계(v0.1)입니다. 공식 앱 스토어 등록을 준비 중이며, 현재는 [Releases](../../releases) 페이지에서 직접 설치 파일을 바로 다운로드하실 수 있습니다.

| 플랫폼 | 내부 작동 방식 | 상태 |
| --- | --- | --- |
| **Android** | 기기 내 로컬 루프백 VPN 기반 DNS 필터링. 루팅 불필요. Android 4.2+ | [Releases](../../releases)에서 APK 다운로드 |
| **Windows** | PC 전체를 커버하는 로컬 DNS 필터링 서비스 (x64, ARM64) | [Releases](../../releases)에서 이용 가능 |
| **macOS** | Mac 전체 시스템을 위한 로컬 DNS 필터 | [Releases](../../releases)에서 이용 가능 |
| **Linux** | 단일 PC 또는 홈 네트워크 전체를 위한 독립형 DNS 프록시 (Java 필요) | [Releases](../../releases)에서 이용 가능 |
| **Chrome, Edge, Brave, Opera, Vivaldi, Arc** | 초경량 고성능 MV3 브라우저 확장 프로그램 | 스토어 등록 심사 준비 중 |
| **Firefox 128+** | 빠르고 가벼운 브라우저 확장 프로그램 | 부가기능 등록 심사 준비 중 |

## 필터 레벨 안내

| 단계 | 프로필 | 차단 범위 |
| --- | --- | --- |
| 1 | 기본 (Basic) | 핵심 광고 및 악성 트래커 도메인만 선별 차단. 오작동 위험이 가장 적습니다. |
| 2 | 균형 (Balanced) | 일반적인 분석 통계 및 텔레메트리 도메인까지 범위를 확장합니다. |
| 3 | 확장 (Extended) | 일상적인 웹서핑에 최적화된 포괄적 차단. **추천 기본값.** |
| 4 | 엄격 (Strict) | 강력한 차단 모드. 외부 위젯을 임베드한 일부 웹페이지에 영향이 갈 수 있습니다. |
| 5 | 최대 (Maximum) | 주요 SNS를 제외한 전체 차단 목록 적용. 일부 복잡한 사이트는 예외 처리가 필요할 수 있습니다. |

💡 **개발자의 꿀팁:** 만약 특정 사이트가 올바르게 작동하지 않는다면, 필터 단계를 1단계 낮추거나 스위치를 잠시 꺼보세요.

## 동작 원리 (마술이 아닌 순수한 DNS 기술!)

앱이나 웹페이지가 인터넷에서 무언가를 가져오려고 할 때, 가장 먼저 하는 일은 해당 도메인의 IP 주소를 묻는 DNS 질의입니다. MuteAds는 여러분 기기의 똑똑한 문지기가 됩니다:

- 요청한 도메인이 광고나 감시 트래커 목록에 있다면, MuteAds는 즉시 *"존재하지 않음 (NXDOMAIN)"*이라고 응답합니다. 연결 자체가 시도되지 않아 데이터와 배터리를 크게 아낍니다.
- 정상적인 콘텐츠 도메인이라면 질의를 상위 DNS 서버로 자연스럽게 전달하여 웹페이지가 원래 속도대로 빠르게 열립니다.

Android에서는 외부로 트래픽을 보내지 않는 **로컬 루프백 VPN**을 통해 기기 내부에서만 돌며, PC에서는 로컬 DNS 서버로 작동합니다. 브라우저 확장 프로그램은 브라우저 자체의 초고속 `declarativeNetRequest` 엔진을 활용합니다.

## 개인정보 보호 원칙: 우리는 당신의 데이터에 관심이 없습니다

- **회원가입 없음, 계정 없음**: 저희는 사용자 계정 시스템이나 중앙 데이터베이스 자체를 운영하지 않습니다.
- **100% 기기 내 처리**: 필터링은 순수하게 사용자의 장치에서 실행됩니다. 여러분이 방문하는 웹사이트를 엿보는 중간 서버가 전혀 없습니다.
- **투명한 업데이트**: 앱이 자동으로 외부와 통신하는 유일한 동작은 일주일에 한 번 차단 도메인 목록을 갱신하는 것뿐입니다.
- **최소한의 권한 요구**: 브라우저 확장 프로그램은 네트워크 요청 차단, 로컬 설정 저장, 주간 갱신 알람, 그리고 `youtube.com` 광고 처리에 필요한 최소 권한만 요청합니다.

## 알아두면 유용한 팁

- **Android 사용자 필수 체크:** 휴대폰 네트워크 설정에서 *개인 DNS (Private DNS)* 옵션을 꺼주세요(켜져 있으면 시스템이 로컬 필터를 우회합니다). 또한 배터리 최적화에서 제외해 주세요.
- **퍼스트 파티 광고:** 원본 콘텐츠와 동일한 도메인에서 송출되는 광고는 순수 DNS 차단만으로는 걸러내기 어렵습니다. 브라우저 확장에서 YouTube 전용 처리 엔진을 별도로 탑재한 이유입니다.
- **YouTube와의 숨바꼭질:** 동영상 플랫폼은 광고 스크립트를 수시로 바꿉니다. 만약 광고가 다시 나타난다면 확장 프로그램을 최신 버전으로 업데이트해 주세요.

## 피드백 및 커뮤니티

페이지가 깨지거나 교묘하게 빠져나가는 광고를 발견하셨나요? 사용 중인 필터 레벨과 페이지 주소를 적어 [Issues](../../issues)에 등록해 주세요. 여러분의 피드백 하나하나가 프로젝트에 큰 힘이 됩니다!

## 라이선스 및 크레딧

Android 앱과 독립형 DNS 프록시는 Ingo Zenz 님의 훌륭한 오픈소스 프로젝트 [personalDNSfilter](https://github.com/IngoZenz/personalDNSfilter)를 바탕으로 개발되었으며, GNU GPL v2 이상 라이선스를 따릅니다. 더 쾌적한 인터넷 환경을 위해 오픈소스로 제공됩니다.
