# 🎬 쿠팡 숏폼 자동 영상 생성기

> 쿠팡파트너스 링크 하나로 **유튜브 쇼츠 / 인스타 릴스 / 틱톡** 영상을 자동 생성하는 AI 툴

[![React](https://img.shields.io/badge/React-18-blue?logo=react)](https://reactjs.org)
[![Claude API](https://img.shields.io/badge/Claude-Sonnet_4-purple?logo=anthropic)](https://anthropic.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## ✨ 주요 기능

| 기능 | 설명 |
|------|------|
| 🔗 파트너스 링크 | 쿠팡파트너스 링크를 영상 + 블로그에 자동 삽입 |
| 🤖 AI 스크립트 | Claude AI가 후크 → 공감 → 소개 → 신뢰 → CTA 5단계 스크립트 자동 생성 |
| 🎥 해외영상 합성 | Pexels/Pixabay MP4 링크를 Canvas에 합성 후 한국어 자막 오버레이 |
| 🔊 한국어 TTS | 브라우저 내장 음성으로 각 장면 대사 자동 낭독 (속도·높이 조절) |
| ⬇ 영상 다운로드 | Canvas 녹화 → WebM 파일 다운로드 |
| 📝 맘카페 블로그 | AI가 맘카페 말투로 SEO 블로그 리뷰 자동 작성 |

---

## 🚀 빠른 시작

### 1. 저장소 복제
```bash
git clone https://github.com/YOUR_USERNAME/coupang-shorts-generator.git
cd coupang-shorts-generator
```

### 2. 패키지 설치
```bash
npm install
```

### 3. 개발 서버 실행
```bash
npm start
```
브라우저에서 `http://localhost:3000` 열기

---

## 📦 GitHub Pages 배포 (무료)

### 1. `package.json`의 `homepage` 수정
```json
"homepage": "https://YOUR_USERNAME.github.io/coupang-shorts-generator"
```

### 2. 빌드 & 배포
```bash
npm run deploy
```

배포 완료 후 `https://YOUR_USERNAME.github.io/coupang-shorts-generator` 에서 접근 가능

---

## 🌐 Vercel 배포 (추천, 더 빠름)

```bash
npm install -g vercel
vercel --prod
```

또는 [vercel.com](https://vercel.com) → GitHub 저장소 연결 → 자동 배포

---

## 📁 프로젝트 구조

```
coupang-shorts-generator/
├── public/
│   └── index.html
├── src/
│   ├── App.js              # 메인 앱 (3단계 폼)
│   ├── index.js            # React 진입점
│   ├── constants.js        # 상수 (플랫폼, 씬, API 설정)
│   ├── components/
│   │   ├── PhonePreview.js # 폰 프리뷰 + 재생 + 녹화 + 블로그
│   │   └── ui.js           # 공통 UI 컴포넌트
│   └── utils/
│       ├── api.js          # Claude API 호출 (스크립트, 블로그)
│       ├── canvas.js       # Canvas 영상 합성 & 자막 렌더링
│       └── tts.js          # 웹 TTS 유틸리티
├── package.json
└── README.md
```

---

## 🛠 사용 방법

### Step 1 — 상품 정보 입력
1. **쿠팡파트너스 링크** 입력 (`link.coupang.com/a/...`)
2. 상품명, 가격, 핵심 특징 입력
3. 플랫폼 선택 (유튜브쇼츠 / 인스타릴스 / 틱톡)
4. 영상 길이 (15초 / 30초 / 60초), 후크 스타일 선택

### Step 2 — 영상 & 음성 설정
1. (선택) Pexels/Pixabay MP4 직접 링크 붙여넣기
2. 한국어 TTS 음성 클릭하여 미리듣기 후 선택
3. 말하기 속도 / 목소리 높이 조절

### Step 3 — 영상 생성 & 활용
1. **▶ 미리보기 + 음성** — 폰 화면에서 영상 + TTS 동시 재생
2. **⬇ 영상 저장** — WebM 파일 다운로드
3. **📝 맘카페 블로그 리뷰** — 파트너스 링크 포함 블로그 글 자동 생성

---

## 💡 무료 영상 소스

| 사이트 | 링크 | 특징 |
|--------|------|------|
| Pexels | https://www.pexels.com/videos/ | 고품질, 저작권 FREE |
| Pixabay | https://pixabay.com/videos/ | 다양한 카테고리 |
| Coverr | https://coverr.co | 라이프스타일 영상 |

> MP4 직접 링크(`.mp4`로 끝나는 URL)를 복사해서 입력하세요.

---

## ⚠️ 중요 안내

- **TTS 음성**은 브라우저 보안 정책으로 인해 다운로드 파일에 포함되지 않습니다
- 음성 포함 최종 영상: **Vrew** (무료) → 파일 열기 → AI 목소리 → MP4 내보내기
- 영상 합성은 CORS 허용 직접 링크만 가능합니다
- Claude API는 claude.ai 계정을 통해 자동 인증됩니다 (별도 키 불필요)

---

## 📋 쿠팡파트너스 필수 고지

> ※ 이 도구로 생성된 콘텐츠에는 쿠팡 파트너스 활동 관련 고지가 자동 삽입됩니다.
> "이 포스팅은 쿠팡 파트너스 활동의 일환으로, 이에 따른 일정액의 수수료를 제공받습니다."

---

## 📄 라이선스

MIT License — 자유롭게 사용, 수정, 배포 가능

---

## 🙏 기여

PR 환영합니다! Issues에 버그 리포트나 기능 제안을 남겨주세요.
