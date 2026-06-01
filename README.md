# face-recognition-attendance-system
face recognition attendance system

※ 2023년 수행한 프로젝트로,
일부 웹 서버 코드 및 배포 환경 파일은 보존되지 않았습니다.
현재 저장소에는 핵심 얼굴 인식 모듈과 프로젝트 문서를 정리하였습니다.

얼굴 인식을 활용한 출결 체크 시스템


프로젝트 소개
기존의 수기 출석, 카드 태깅, 전자 출결번호 입력 방식에서 발생하는 대리 출석 문제와 출석 확인 시간 지연 문제를 해결하기 위해 얼굴 인식 기반 출결 체크 시스템을 개발하였다.

학생 얼굴 데이터를 학습한 후 실시간 웹캠 영상을 통해 사용자를 식별하고, 출석 여부를 Flask 웹 페이지에 자동으로 반영하는 시스템을 구현하였다.

개발 기간

2023.09 ~ 2023.12

사용 기술
언어 및 프레임워크
Python
Flask
라이브러리
face_recognition
dlib
OpenCV
scikit-learn
NumPy
하드웨어
Raspberry Pi 4
Webcam
주요 기능
얼굴 인식 모델 생성

학생별 얼굴 사진을 이용하여 얼굴 특징 벡터(Encoding)를 생성하고 저장

실시간 얼굴 인식

웹캠으로 입력되는 영상에서 얼굴을 탐지하고 등록된 사용자와 비교하여 신원을 식별

출석 정보 자동 반영

인식된 사용자 정보를 Flask 웹 서버에 전달하여 출석부를 자동 업데이트

수행 내용
1. 얼굴 인식 모델 비교

얼굴 인식 성능 향상을 위해 세 가지 모델을 구현하고 성능을 비교하였다.

Face Recognition 단독 모델
Face Recognition + KNN
Face Recognition + SVM
2. 성능 평가
모델	정확도
Face Recognition	100%
Face Recognition + KNN	87%
Face Recognition + SVM	87%

성능 비교 결과 Face Recognition 단독 모델이 가장 높은 정확도를 보여 최종 모델로 선정하였다.

3. 웹 기반 출석 시스템 구현

Flask를 이용하여 출석 현황을 확인할 수 있는 웹 페이지를 구현하였으며, 얼굴 인식 결과를 실시간으로 반영하도록 구성하였다.

결과
실시간 얼굴 인식 기능 구현
다중 사용자 동시 인식 성공
Flask 기반 출석부 연동 완료
대리 출석 방지 가능성 확인
사용자당 약 10장의 학습 이미지로 높은 인식 성능 확보
배운 점
얼굴 특징 벡터를 이용한 얼굴 인식 과정 이해
Face Recognition 라이브러리 활용 경험
SVM, KNN 등 머신러닝 분류 모델 비교 및 평가 경험
Flask 기반 웹 서비스 구현 경험
Raspberry Pi 환경에서 AI 시스템 구축 경험

