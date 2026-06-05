# 🤖 AI 챗봇 어시스턴트

Microsoft Copilot Studio 기반의 AI 챗봇을 임베드한 웹 인터페이스입니다.

---

## 📌 프로젝트 개요

이 프로젝트는 Microsoft Copilot Studio로 제작된 챗봇을 외부 웹페이지에 손쉽게 임베드하기 위한 단일 HTML 파일입니다. 다크 테마의 사이버펑크 스타일 UI를 제공하며, 별도의 빌드 도구나 서버 없이 바로 실행할 수 있습니다.

---

## ✨ 주요 기능

- **Microsoft Copilot Studio 챗봇 임베드** — iframe을 통해 Copilot Studio 웹챗을 직접 연결
- **다크 테마 UI** — 사이버펑크 컨셉의 그리드 배경 및 글로우 효과
- **애니메이션 효과** — 헤더 슬라이드인, 카드 페이드업, 상태 표시 펄스 등 CSS 애니메이션 적용
- **실시간 온라인 상태 표시** — 깜빡이는 닷 배지로 봇 활성 상태 시각화
- **반응형 레이아웃** — 최대 너비 1100px 기준의 중앙 정렬 그리드 레이아웃
- **마이크 접근 권한** — 음성 입력을 위한 마이크 허용 설정 포함

---

## 🛠 기술 스택

| 구분 | 내용 |
|------|------|
| 언어 | HTML5, CSS3 |
| 폰트 | Noto Sans KR, DM Mono (Google Fonts) |
| 챗봇 플랫폼 | Microsoft Copilot Studio |
| 임베드 방식 | iframe |

---

## 📁 파일 구조

```
├── chatbot.html    # 메인 챗봇 UI (단일 파일)
└── README.md
```

---

## 🚀 실행 방법

별도의 설치나 빌드가 필요 없습니다.

1. 이 저장소를 클론합니다.
   ```bash
   git clone https://github.com/{username}/{repository}.git
   ```

2. `chatbot.html` 파일을 브라우저에서 직접 열거나, 웹 서버를 통해 서빙합니다.
   ```bash
   # 간단한 로컬 서버 예시 (Python)
   python -m http.server 8000
   ```

3. 브라우저에서 `http://localhost:8000/chatbot.html` 로 접속합니다.

---

## ⚙️ 챗봇 교체 방법

다른 Copilot Studio 봇으로 교체하려면 `chatbot.html` 내 iframe의 `src` 값을 수정합니다.

```html
<iframe
  src="https://copilotstudio.microsoft.com/environments/{환경ID}/bots/{봇ID}/webchat?__version__=2"
  allow="microphone"
  title="AI 챗봇 어시스턴트"
></iframe>
```

Copilot Studio 포털에서 봇을 선택한 뒤 **설정 > 채널 > 웹사이트에 게시** 메뉴에서 임베드 URL을 확인할 수 있습니다.

---

## 🎨 UI 커스터마이징

CSS 변수를 수정하여 테마 색상을 손쉽게 변경할 수 있습니다.

```css
:root {
  --bg:      #0b0f1a;   /* 배경색 */
  --surface: #111827;   /* 카드 배경 */
  --border:  #1e2d40;   /* 테두리 */
  --accent:  #00c2ff;   /* 주요 강조색 */
  --accent2: #7b61ff;   /* 보조 강조색 */
  --text:    #e2e8f0;   /* 본문 텍스트 */
  --muted:   #64748b;   /* 보조 텍스트 */
}
```

---

## 📄 라이선스

이 프로젝트는 [MIT License](LICENSE)를 따릅니다.
