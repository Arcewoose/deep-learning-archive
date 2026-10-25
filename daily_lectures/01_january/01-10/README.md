# TIL (Today I Learned)

## 1. Core Concepts
- **정규표현식(Regex) 기반 텍스트 정제**: 패턴 매칭(`re.sub`)을 통한 불필요한 특수문자 및 공백 제거 원리
- **DataFrame 구조화**: 비정형 텍스트 데이터를 2차원 배열 및 행/열(Field/Record) 구조의 테이블로 변환하는 기초 메커니즘

## 2. Practical Implementation
- **사용 도구**: `Python`, `re`, `pandas`, `numpy`
- **구현 내용**:
  - 줄바꿈(`\n`) 및 공백 제거를 위한 다중 정규식 전처리 파이프라인 구성
  - 한글 이외의 문자 필터링(`[^ㄱ-ㅎ가-힣]+`)을 통한 텍스트 토큰 추출
  - 1차원 문자열 데이터를 2차원 리스트로 분할 후 Pandas DataFrame으로 적재

## 3. Technical Notes
- `str.replace` 단순 치환 대비 `re.sub`를 활용한 정규식 복합 패턴 처리의 유연성
- 중첩 리스트(`nameList.append([])`) 구조를 활용한 동적 2차원 데이터 적재 패턴
