# 천안시 청년정책 — 인터랙티브 웹 프레젠테이션

원본: `cheonan_youth_policy_2026_minimal(1).pptx` (10장)

## 파일 구조

- `index.html` — 화면 구성, 상단 목차, 이전·다음 버튼, 접근성 정보 패널
- `style.css` — 반응형 디자인과 화면 전환 애니메이션
- `script.js` — 슬라이드 내비게이션, 스크롤/키보드/터치 제어
- `slides.json` — 원본 PPT에서 추출한 슬라이드별 텍스트
- `assets/slides/*.jpg` — 원본 슬라이드 렌더링 이미지 (10장)
- `assets/thumbs/*.jpg` — 전체 목차용 슬라이드 썸네일 (10장)

## GitHub Pages 게시

1. 새 GitHub 저장소를 만듭니다.
2. 이 폴더 내부의 모든 파일과 `assets` 폴더를 저장소 최상위 경로에 업로드합니다. (`index.html`이 루트에 있어야 합니다.)
3. 저장소 Settings > Pages > Build and deployment > Deploy from a branch를 선택합니다.
4. Branch `main`, folder `/(root)`을 선택 후 Save를 클릭합니다.
5. 게시된 `https://사용자명.github.io/저장소명/` 경로에서 접속합니다.

### 로컬 미리보기

`slides.json`을 읽는 `fetch()` 기능 때문에 일부 브라우저에서 파일을 직접 더블클릭(`file://`)하면 텍스트/목차가 로드되지 않을 수 있습니다. 폴더에서 `python -m http.server 8000` 명령으로 임시 서버를 실행한 뒤 `http://localhost:8000`으로 확인하거나 GitHub Pages에 게시하세요. 게시 후에는 별도 서버 또는 데이터베이스가 필요 없습니다.

## 조작법

- 이전/다음 버튼, 화살표 키, Page Up/Down, 스페이스바
- 휠 스크롤 및 모바일 좌우 스와이프
- 상단 목차 / 전체 목차 / 텍스트 확인 / 복사 / 전체화면
- `#slide-4` 같은 URL로 개별 슬라이드 링크 공유 가능

## 원본 보존 안내

PPT 슬라이드를 JPG로 렌더링해 배치하여 원본 그래픽과 일러스트, 도표의 시각적 구성을 보존했습니다. 슬라이드 내부 도형·차트를 웹에서 별도로 조작하거나 편집할 수 있는 구조는 아닙니다. 슬라이드 텍스트는 검색·복사 가능한 별도 패널로 제공합니다. 외부 CDN, 웹폰트, 서버, DB 의존성이 없습니다.
