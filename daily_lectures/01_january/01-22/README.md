# TIL (Today I Learned)

## 1. Core Concepts
- **Flask 마이크로 웹 프레임워크 기초**:
  - 라우팅 데코레이터(`@app.route`)를 통한 URL 엔드포인트 매핑
  - HTTP 요청 메서드(`GET`, `POST`) 분기 처리 구조
  - Jinja2 템플릿 엔진을 통한 백엔드 데이터와 HTML 뷰 연동

## 2. Practical Implementation
- **사용 도구**: `Flask`, `Python`, `HTML`
- **구현 내용**:
  - `Flask` 인스턴스 생성 및 로컬 개발 서버 실행 환경 구축
  - 클라이언트 HTML 폼(`form`) 입력값 파싱 (`request.form`)
  - 합산 연산 결과 데이터를 템플릿 변수로 주입하여 `render_template` 렌더링

## 3. Technical Notes
- 폼 입력 데이터는 기본 문자열(`str`)로 전달되므로 수치 연산 시 `float()` 명시적 형변환 필요
- Flask 기본 템플릿 디렉터리 경로 구조(`templates/`) 준수 필수
