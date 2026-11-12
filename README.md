# 온기 ONGI — 카페 랜딩 페이지

동네 로스터리 카페를 위한 단일 페이지 랜딩 사이트입니다.
의존성 없는 정적 HTML 한 장이라 빌드 과정이 필요 없습니다.

## 구성

| 섹션 | 내용 |
|---|---|
| Hero | 브랜드 한 줄 메시지와 CTA |
| Signature | 시그니처 메뉴 3종 카드 |
| About | 가게 소개 2단 레이아웃 |
| Visit | 주소 · 영업시간 · 연락처 |

## 실행

```bash
# 파일을 그대로 브라우저에서 열거나
start index.html

# 또는 로컬 서버로
python -m http.server 8000
```

## 기술 메모

- 외부 의존성은 Google Fonts(Noto Serif KR / Noto Sans KR)뿐입니다
- 라이트/다크 모드를 `prefers-color-scheme`로 자동 전환합니다
- 색상은 `:root`의 CSS 변수로 모아 두었으니 브랜드 컬러는 거기서 바꾸면 됩니다
- 스크롤 등장 효과는 `IntersectionObserver` 기반이며, 미지원 브라우저에서는 전부 표시됩니다
- `prefers-reduced-motion`을 존중합니다

## 교체가 필요한 플레이스홀더

- 주소 / 전화번호 (`#visit` 섹션)
- About 섹션의 이미지 자리 (`.figure` — 현재 그라디언트 + 이모지)
- 푸터의 Instagram · Naver Map 링크
