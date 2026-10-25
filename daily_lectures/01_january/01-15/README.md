# TIL (Today I Learned)

## 1. Core Concepts
- **통계적 가설 검정**:
  - 귀무가설(Null Hypothesis)과 대립가설(Alternative Hypothesis) 설정
  - 유의수준($p$-value < 0.05) 기준 가설 기각/채택 원리
  - 검정 기법 구분: T-test(연속형 변수 평균 비교), Chi-Square test(범주형 변수 독립성/적합도 검정)
  - 자유도(Degrees of Freedom)의 정의 및 표본 크기와의 관계
- **객체 지향 프로그래밍(OOP) 기초**:
  - 클래스(`class`) 정의, 생성자(`__init__`), 인스턴스 변수 및 메서드 캡슐화

## 2. Practical Implementation
- **사용 도구**: `Python`, `scipy.stats`, `pandas`, `numpy`
- **구현 내용**:
  - `scipy.stats.ttest_ind`, `scipy.stats.chisquare`를 활용한 가설 검정 실습
  - 반복적인 통계 계산 로직을 수행하는 커스텀 파이썬 클래스 및 함수 모듈화 구현

## 3. Technical Notes
- 단일 표본, 독립 표본, 대응 표본 등 데이터 수집 조건에 따른 올바른 검정 통계량 함수 선택 필요
- 클래스 내부 메서드 선언 시 첫 번째 인자로 `self`를 전달하여 인스턴스 바인딩 유지
