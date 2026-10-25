# TIL (Today I Learned)

## 1. Core Concepts
- **CSS Selector 기반 요소 탐색**:
  - 태그 경로(`html head title`), 클래스(`.class`), ID(`#id`) 및 자식/자손 선택자 문법
  - `find`/`find_all` 대비 CSS Selector(`select`, `select_one`)의 구조적 장점
- **웹 데이터 구조화 및 JSON 직렬화**: 수집된 텍스트와 메타데이터의 Key-Value 매핑 및 JSON 내보내기

## 2. Practical Implementation
- **사용 도구**: `requests`, `BeautifulSoup`, `json`, `Python`
- **구현 내용**:
  - 언론사 뉴스 페이지 타깃 HTTP 요청 및 HTML 파싱
  - CSS Selector를 활용한 기사 제목, 본문, 작성 일자 필터링
  - 수집 데이터 정제 후 `json.dump`를 통한 `all_data.json` 저장

## 3. Technical Notes
- `select()` 반환값은 리스트이므로 단일 요소 추출 시 인덱싱(`[0]`) 또는 `select_one()` 활용
- 인라인 태그(`span`, `a` 등) 제거 및 `get_text(strip=True)`를 통한 공백 제거 텍스트 정제
