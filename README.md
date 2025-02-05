```markdown
# 🍽️ 점심 메뉴 추천 웹앱

이 프로젝트는 사용자가 입력한 내용을 기반으로 AI가 점심 메뉴를 추천해주는 간단한 웹 애플리케이션입니다.  
두 가지 AI 모델(`gemini-1.5-flash`, `deepseek-r1`) 중 하나를 선택하여 추천을 받을 수 있습니다.

---

## 📌 주요 기능
- AI 모델을 선택하여 점심 메뉴 추천받기
- 추천 내역을 **로컬 스토리지**에 저장하여 유지
- 저장된 추천 내역 **삭제 기능** 제공
- **서버 요청을 통해 AI 응답 받기** (현재는 임시 API 사용)

---

## 🛠️ 기술 스택
- **HTML**: 기본적인 UI 구조
- **CSS**: (스타일은 최소화)
- **JavaScript**: 동작 구현
  - `fetch()`를 이용한 API 요청
  - `localStorage`를 활용한 데이터 저장
  - `Proxy` 객체를 이용한 상태 관리

---

## 🚀 실행 방법
1. 프로젝트 파일을 다운로드하거나 클론합니다.
   ```sh
   git clone https://github.com/your-repo/lunch-recommendation.git
   cd lunch-recommendation
   ```
2. `index.html` 파일을 브라우저에서 엽니다.

---

## 🔧 사용법
1. **메뉴 추천 요청하기**
   - 텍스트 입력란에 원하는 내용을 입력합니다.
   - AI 모델을 선택합니다.
   - "등록" 버튼을 누르면 추천 결과가 표시됩니다.

2. **저장된 추천 내역 관리**
   - 추천 결과는 `localStorage`에 저장됩니다.
   - "삭제" 버튼을 눌러 개별 추천을 삭제할 수 있습니다.
   - "저장된 데이터 리셋" 버튼을 눌러 모든 추천 내역을 초기화할 수 있습니다.

---

## 📡 API 요청 방식
- **AI 모델별 API 엔드포인트**
  - `gemini-1.5-flash` → `"https://productive-majestic-olivine.glitch.me/1"`
  - `deepseek-r1` → `"https://productive-majestic-olivine.glitch.me/2"`
- 요청 방식: `POST`
- 요청 본문 예시:
  ```json
  {
    "text": "오늘 뭐 먹을까?"
  }
  ```
- 응답 예시:
  ```json
  {
    "reply": "오늘은 김치찌개 어떠세요?"
  }
  ```

---

## 📌 개선 가능 사항
- **스타일 추가**: CSS를 추가하여 UI 개선
- **에러 처리 강화**: API 응답 실패 시 사용자 알림 추가
- **실제 AI API 연결**: 현재는 임시 API를 사용 중이므로, 실제 AI API 연결 필요

---
