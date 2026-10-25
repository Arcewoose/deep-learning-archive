# TIL (Today I Learned)

## 1. Core Concepts
- **MediaPipe Pose 랜드마크 추출**: 
  - 신체 관절 33개 키포인트의 3D 공간 좌표($x, y, z$) 실시간 추정 메커니즘
- **포즈 시퀀스 기반 동작 분류(Action Recognition)**:
  - 프레임별 관절 좌표 벡터를 특징량(Feature)으로 변환하여 신경망 분류기에 입력하는 파이프라인
  - 보행 상태(Walking vs Non-Walking) 구분을 위한 다층 퍼셉트론(MLP) 구조

## 2. Practical Implementation
- **사용 도구**: `mediapipe`, `OpenCV (cv2)`, `TensorFlow/Keras`, `numpy`, `scikit-learn`
- **구현 내용**:
  - `mp.solutions.pose.Pose`를 통한 보행 영상(`walking_all_02.mp4`) 프레임별 랜드마크 추출
  - Keras `Sequential` 기반 5계층 Dense 분류 모델 설계 및 `Adam` 옵티마이저 학습
  - 학습 완료 가중치 모델(`walk_estimation.h5`) 저장 및 웹캠 기반 실시간 추론(`walk_estimation_webcam.py`) 구현

## 3. Technical Notes
- 비디오 프레임 추출 시 `min_detection_confidence` 및 `min_tracking_confidence` 조정을 통한 키포인트 노이즈 제어
- 입력 텐서 형상(`(batch, 33, 3)`)에 맞춘 `Flatten` 레이어 선행 배치
