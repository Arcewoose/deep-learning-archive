# TIL (Today I Learned)

## 1. Core Concepts
- **MediaPipe 아키텍처**: 경량 파이프라인 기반 실시간 컴퓨터 비전 프레임워크
- **Face Landmark Detection**: 얼굴 영역 내 6개 주요 랜드마크(양안, 코, 입, 양이) 좌표 추정 및 정규화 좌표계 변환 원리
- **Eye Tracking**: 눈 영역 ROI(Region of Interest) 추출 및 시선 추적 좌표 매핑

## 2. Practical Implementation
- **사용 도구**: `mediapipe`, `OpenCV (cv2)`, `numpy`, `matplotlib.pyplot`
- **구현 내용**:
  - `mp.solutions.face_detection` 모듈을 활용한 정적 이미지 및 비디오 프레임 내 얼굴 바운딩 박스 검출
  - 검출된 얼굴 영역의 6개 키포인트 좌표 추출 및 `cv2.circle`, `cv2.rectangle` 오버레이 렌더링
  - 동공 및 눈 영역 ROI 크롭 후 이진화 처리를 통한 시선 변화 트래킹

## 3. Technical Notes
- OpenCV(`BGR`)와 MediaPipe(`RGB`) 간 색상 채널 포맷 차이에 따른 `cv2.cvtColor` 변환 필수
- 정규화된 랜드마크 좌표($0.0 \sim 1.0$)를 원본 이미지 해상도(Width, Height)와 곱하여 픽셀 정수 좌표로 역변환 수행
