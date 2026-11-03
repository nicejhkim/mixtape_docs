# mixtape_docs

Old Mix Tape 스토어·법적 문서용 GitHub Pages 저장소.

공개 주소:

- 사이트: https://nicejhkim.github.io/mixtape_docs/
- 개인정보처리방침 (KO): https://nicejhkim.github.io/mixtape_docs/ko/privacy/
- Privacy Policy (EN): https://nicejhkim.github.io/mixtape_docs/en/privacy/

## 구조

| 경로 | 역할 |
|------|------|
| `_includes/legal/` | 방침 **원본** (KO/EN). 여기만 고치면 된다. |
| `store/legal/` | 원본으로의 심볼릭 링크 (스토어·검토용). |
| `store/appstore/`, `store/play/` | 스토어 리스팅·이미지·체크리스트. 사이트에 올리지 않음. |
| `ko/`, `en/` | 언어별 permalink 래퍼. |
| `_layouts/`, `assets/` | 공통 레이아웃·스타일. |

## 방침 수정

1. `_includes/legal/privacy-policy-ko.md` / `privacy-policy-en.md` 수정
2. 시행일(Effective) 갱신
3. `main`에 푸시 → Pages 반영. 스토어 Console URL은 그대로 둔다.

이용약관 등이 필요하면 `_includes/legal/`에 마크다운을 추가하고, `ko/`·`en/`에 래퍼만 만들면 된다.
# mixtape_docs
