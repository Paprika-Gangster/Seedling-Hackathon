# MVP 방법론 - Team 파프리카 갱스터

## 1. 아이디어 브리프 및 요구 사항 정의

### 📄 브리프
노인들이 누군가와 대화하듯이 즐겁게 일기를 작성할 수 있도록 도와주는 AI 서비스

### 🌟 핵심 기능 정의
- **🤖 챗봇을 이용한 맞춤형 질문 제공**
- **🖼️ DALL·E API를 이용한 다이어리 작성**
- **📚 피드 열람 (사용자 자신과 다른 사용자의 다이어리 피드)**

## 2. 사용할 노코딩 툴
**🛠️ bubble.io**

## 3. 데이터베이스 설계

### 👤 사용자
- 이메일
- 비밀번호
- 성별

### ❓ 하루에 대한 질문
- 질문 내용 (절기, 기념일, 랜덤 등)

### 📓 일기
- 사용자 ID
- 날짜
- 일기 텍스트
    - 직접 입력된 텍스트
    - STT를 통해 변환된 텍스트
- 생성된 이미지

## 4. UI 디자인
전체적인 요소를 큼직하게 설계

### 🖥️ 페이지 설계
- **🏠 메인페이지**: 기억력 자극 질문, 오늘 날짜와 정보 확인, 일기 작성 요청 버튼, 연속 일기 작성 일수
- **✍️ 일기 작성 페이지**: 현재 날짜/요일 표기, 대화형 일기 작성 영역, 이미지 첨부 버튼, 텍스트 입력 버튼, 음성 입력 버튼
- **📅 캘린더 페이지**: 현재 달력 표기, 해당 날짜의 간단한 일기 표기, 자세한 일기 보기 버튼, 해당 날짜 날씨 표기, 해당 날짜의 정보 표기
- **📝 작성된 일기 페이지**: AI가 작성한 일기와 추출한 이미지 영역, 일기 저장하기 버튼
- **🌐 커뮤니티 페이지**: 다른 사람이 작성한 페이지 표기, 좋아요 버튼
- **👤 마이페이지**: 사용자 정보, 프로필 사진, 총 작성 일기 수, 연속 일기 작성 일수, 일기 관리 기능

## 5. 워크 플로우 설정

### 1) 사용자 등록 및 프로필 설정
- 사용자 정보 입력: 이름, 나이, 성별 등

### 2) 메인화면
- 오늘의 질문을 보면서 기억 복기
- 오늘의 일기 작성 페이지로 연결

### 3) 일기 작성 페이지
- **🗣️ 음성 입력**: 사용자가 대화형 AI와 오늘의 하루에 대해서 대화, 대화 내용은 음성 인식 기술을 통해 텍스트로 변환해 AI와 채팅형식으로 보여줌
- **⌨️ 텍스트 입력**: 사용자가 직접 키보드로 텍스트로 입력해 AI와 대화할 수도 있음
- **📷 이미지 입력**: 사진 촬영 또는 갤러리에서 이미지를 선택하여 이미지 첨부

### 4) 작성된 일기 페이지
- AI가 분석한 음성, 텍스트, 이미지 데이터를 바탕으로 일기의 이미지와 내용 자동 생성
- 저장 버튼으로 AI가 작성해준 일기 저장

### 5) 캘린더 페이지
- 원하는 월의 달력을 확인할 수 있고, 날짜를 클릭하면 그날의 일기를 간단하게 보여줌
- 자세한 일기를 보고 싶으면 일기 보기 버튼을 통해 해당 날짜의 일기를 빠르게 확인 가능

### 6) 커뮤니티 페이지
- 사용자는 다양한 사용자의 공개된 일기를 탐색하고 교류할 수 있음

## 6. 테스트 및 피드백 수집

### 🧪 테스트
노인 사용자 중 우선적으로 디지털 기기 사용에 익숙한 60대 사용자 30명을 모집하여 베타 테스트 진행

### 📋 피드백 수집
설문조사, 인터뷰, 피드백 폼을 통해 지속적으로 피드백을 수집

## 7. 배포 및 유지보수

### 🚀 배포
- bubble 플랫폼의 호스팅을 이용한 배포
- 배포 후 사용자들로부터 초기 피드백을 수집하여 수정 사항 파악
- 배포 후 서버 상태, 오류 로그, 사용자 행동을 모니터링하고 문제를 즉시 발견하여 대응

### 🛠️ 유지보수
- 서버와 데이터베이스의 상태를 정기적으로 점검하고 백업을 수행
- 사용자의 피드백을 통해 발견된 오류를 수정하고, 새로운 기능을 추가하거나 기능 개선을 시도함
