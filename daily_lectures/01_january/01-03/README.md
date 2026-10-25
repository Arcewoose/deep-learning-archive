# TIL (Today I Learned)

## 1. Core Concepts
- **JSON 데이터 계층 구조**: Key-Value 구조 및 리스트 기반 다차원 데이터셋 파싱 원리
- **통계 집계 방식**: 다중 지역 시계열 데이터의 축(Axis) 기준 데이터 분할 및 합산

## 2. Practical Implementation
- **사용 도구**: `json`, `numpy`, `matplotlib.pyplot`
- **구현 내용**:
  - `weatherData.json`에서 서울, 부산, 제주 3개 지역의 일자별 기온 및 강수량 데이터 로드
  - 강수량 결측값(`""`) 필터링 및 문자열 수치 데이터의 `float` 형변환
  - `numpy.sum`을 활용한 지역별 1월 강수량 합계 산출
  - `matplotlib.pyplot.bar`를 이용한 지역별 강수량 통계 막대그래프 시각화

## 3. Technical Notes
- `zip()` 함수를 활용하여 서로 다른 리스트(`name`, `date`, `max`, `min`, `rain`)를 하나의 2차원 레코드로 병합 처리
- 한글 폰트 미설정 환경에서 Matplotlib 차트 타이틀 렌더링 시 Glyph 경고 발생 확인
