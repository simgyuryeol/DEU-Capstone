# DEU-Capstone
동의대 캡스톤

## 주제 야생동물 퇴치 시스템
 ##### 개요 : 아프리카 돼지 열병에 걸린 동물들의 개체를 총기로 제거하거나 울타리를 관리를 진행하지만 동물들을 완전히 가둘 수 없으며 사람이 모든 것을 관리하기에는 무리가 있다. 이를 관리하기 위해 개발
  ##### 아이디어 : 캠을 이용하여 실시간으로 야생동물을 인식하면 웹 서버를 이용하여 데이터를 보내 아두이노로 받아서 퇴치 도구 실행
  
  #####  window 환경에서 YOLO v3 사용 
 

 
 #### 빌드 방법
 
 * 사전 프로그램 설치
  Visual Studio (2019 설치)
  NVIDIA CUDA (10.2 설치)
  NVIDIA cuDNN (CUDA에 맞게 10.2 설치)
  OpenCV 2.4 이상 (4.2 설치)
  Darknet
  
 * Darknet 빌드
  1. Visual Studio 구동
  2. 플랫폼 도구 집합 변경
  3. 사용자 정의 빌드 확인
  4. 헤더 파일 경로 추가
  5. 라이브러리 경로 추가
  6. Code Generation 수정
  7. OpenCv관련 DLL 복사
  8. 빌드
  
  
   [window 10 Darknet 빌드 참고자료(1)](https://m.blog.naver.com/estern/221828977313)
 
   [window 10 Darknet 빌드 참고자료(2)](https://ctkim.tistory.com/81)
   
   
   * YOLO 테스트
   1. weights 파일 다운로드
   [weights파일 다운](https://pjreddie.com/darknet/yolo/)
   2. cmd 화면에서 명령어 실행
   
   
    darknet detect cfg/yolov3.cfg yolov3.weights (yolo v3.weights파일 실행 -> 오류 원본 사진 그대로 출력됨)
   ![image](https://user-images.githubusercontent.com/66519915/128015190-4d00a20f-3802-4956-b713-69be107eeabb.png)

    darknet detect cfg/yolov3-tiny.cfg yolov3-tiny.weights data/dog.jpg (yolo v3 tiny.weights파일 실행 -> 객체 검출)
   ![image](https://user-images.githubusercontent.com/66519915/128015308-9f39465e-69fd-4916-bfee-68ad0c759d9b.png)

 
 

