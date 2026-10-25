# TIL (Today I Learned)

## 1. Core Concepts
- **자료구조 - 해시 테이블(Hash Table)**:
  - 해시 함수(Hash Function)를 통한 Key-Index 매핑 및 평균 $O(1)$ 시간 복잡도
  - 해시 충돌(Hash Collision) 원인 및 해결 방식 (체이닝 vs 개방 주소법)
- **웹 스크래핑 및 HTML DOM 파싱**:
  - HTTP 요청/응답 주기 및 정적 HTML 문서 구조(DOM 트리) 이해
  - 태그, 클래스(`class`), 아이디(`id`), 속성(`attr`) 기반 타깃 데이터 탐색 원리

## 2. Practical Implementation
- **사용 도구**: `BeautifulSoup (bs4)`, `requests`, `Python`
- **구현 내용**:
  - `requests.get`을 통한 웹 페이지 HTML 소스코드 수집
  - `BeautifulSoup` 파서를 이용한 계층적 DOM 요소 접근 (`find`, `find_all`, CSS 선택자)
  - 텍스트 콘텐츠 추출 및 구조화 데이터프레임 적재

## 3. Technical Notes
- 태그 검색 시 `class` 예약어 충돌 방지를 위해 `class_` 파라미터 사용
- 대량 요청 시 서버 부하 방지를 위한 요청 딜레이(`time.sleep`) 및 응답 상태 코드(`response.status_code == 200`) 예외 처리 필수
