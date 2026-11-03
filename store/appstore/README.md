# App Store 출시 준비

등록 문구는 `listing-ko.md`(기본 언어), `listing-en.md`에 있다. 아래는 App Store Connect에서 채우거나 결정해야 하는 것들이다.

앱 화면은 한국어만 있다. 영어 리스팅은 스토어 소개 문구다.

공개 출시(App Store 심사에 올리는 것)는 하지 않는다. 배포는 `testflight-*` 태그로 TestFlight 내부 테스트까지다. 방송 녹음의 저작권 검토 전에는 이 범위를 넘기지 않는다.

## 앱 개인정보 보호 (Nutrition Label)

개인정보처리방침(`store/legal/privacy-policy-ko.md`)과 같은 내용으로 신고한다. Play 데이터 보안 표(`store/play/README.md`)와도 어긋나면 안 된다.

개발자가 수집하는 데이터는 없다. 충돌 데이터, 성능 데이터, 제품 상호작용, 기기 ID, 연락처, 위치, 사진을 수집하지 않는다. 추적(Tracking)은 전부 '아니요'다. 광고 식별자를 쓰지 않으므로 `NSUserTrackingUsageDescription`과 ATT 동의창이 필요 없다.

네트워크는 방송국 검색용 radio-browser.info, 사용자가 재생하는 스트림 주소, 적어 둔 로고 주소, 그리고 글꼴을 처음 받을 때의 Google Fonts에만 나간다. 그 접속은 개발자 서버로 모이지 않는다. 방송국 정보는 radio-browser.info에서 제공받는다.

## 연령 등급

앱 화면에는 폭력·선정성·도박·약물·불쾌한 표현이 없다. 다만 사용자가 아무 스트림 주소나 재생할 수 있고, 처음 들어 있는 채널도 실시간 방송이다. 설문에서 '없음'으로 단정하기 전에, 사용자 제공 오디오를 어떻게 답할지 확인한다.

## 수출 규정

`ios/Runner/Info.plist`에 `ITSAppUsesNonExemptEncryption = false`가 들어 있다. HTTPS 외의 암호화를 쓰지 않으므로 빌드마다 질문이 뜨지 않는다. 암호화 코드를 추가하면 이 값을 다시 보라.

## 스크린샷

**없음. 공개 출시를 하게 되면 반드시 필요하다.** `TARGETED_DEVICE_FAMILY = "1,2"`라 iPhone과 iPad를 모두 올린다. 최소는 6.9"(또는 6.7") iPhone 세로와 13" iPad다.

찍을 장면: 채널 목록, 재생 중인 플레이어, 녹음 중, 새 테이프(길이·색깔), 보관함, 테이프 재생.

## 심사 노트에 적을 것

- 계정·로그인·결제가 없어 심사용 데모 계정이 필요 없다.
- 재생과 녹음은 스트림 주소로 직접 접속한다. 인터넷이 없으면 이미 담아 둔 테이프 재생만 된다.
- 테이프는 앱 밖으로 보내지 않는다.

## 개인정보 매니페스트 (PrivacyInfo.xcprivacy)

앱 타깃에는 아직 없다. 업로드 뒤 Apple이 `ITMS-91053`(필수 사유 API 미신고) 메일을 보내면 앱 타깃에 `PrivacyInfo.xcprivacy`를 추가하고 해당 API의 사유를 적어야 한다. 그 메일이 오기 전에는 추측으로 적지 않는다.

## 막힌 것

- 스크린샷 (위)
- 공개 출시 — 저작권 검토 전. 개인정보처리방침 URL은 Pages 기준 https://nicejhkim.github.io/mixtape_docs/ko/privacy/ (EN: `/en/privacy/`)
