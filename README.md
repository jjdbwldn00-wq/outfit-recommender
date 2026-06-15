# outfit-recommender
날씨 기반 AI 복장 추천 웹 서비스
# 오늘 뭐 입지? - 날씨 기반 AI 옷차림 추천 웹 서비스

![Service Demo](https://img.shields.io/badge/React-18-blue) ![TypeScript](https://img.shields.io/badge/TypeScript-5.5-blue) ![Vite](https://img.shields.io/badge/Vite-5.4-green) ![Tailwind CSS](https://img.shields.io/badge/Tailwind-3.4-38bdf8)

## 1. 프로젝트 소개

**"오늘 뭐 입지?"**는 사용자의 위치, 외출 시간대, 일정, 체감 성향을 입력받아 현재 날씨 정보와 함께 분석하고 최적의 옷차림을 AI가 추천해주는 웹 서비스입니다.

### 핵심 특징
- 🌤️ **정교한 날씨 분석**: 기온뿐만 아니라 체감온도, 습도, 풍속, 일교차, 강수 확률 등 다양한 요소 고려
- 🎯 **개인화된 추천**: 사용자의 체감 성향(더위/추위)과 스타일 선호도를 반영
- 📋 **상세한 정보 제공**: 추천 이유, 추가 팁, 시간대별 기온 정보 제시
- 📱 **반응형 디자인**: 모바일부터 데스크톱까지 최적화된 UI
- ✨ **샘플 데이터 지원**: API 키 없이도 즉시 테스트 가능

---

## 2. 주요 기능

### 2.1 사용자 입력 폼
- **위치**: 도시명 입력 (예: 서울, 부산, 제주)
- **외출 시간대**: 오전 / 오후 / 저녁 / 종일 선택
- **일정**: 학교 / 출근 / 운동 / 데이트 / 여행 / 약속 선택
- **체감 성향**: 더위를 많이 탐 / 추위를 많이 탐 / 보통 선택
- **스타일 선호**: 편한 스타일 / 단정한 스타일 / 활동적인 스타일 선택

### 2.2 날씨 정보 카드
- 현재 기온, 체감온도, 습도, 강수 확률, 풍속 표시
- 시간대별 기온(오전/오후/저녁) 및 일교차 시각화
- 날씨 상태 요약 (맑음/흐림/비 등)

### 2.3 AI 추천 결과
추천 대상:
- **상의**: 기온과 일정에 따른 최적 상의 추천
- **하의**: 활동성과 스타일을 고려한 하의 추천
- **겉옷**: 필요 여부 판단 및 추천 상품
- **신발**: 날씨와 활동 유형에 맞는 신발
- **액세서리**: 우산, 목도리, 장갑 등 필요 물품

### 2.4 추천 이유 및 팁
- **추천 이유**: 왜 이 옷차림을 추천했는지 상세 설명
  - 기온/체감온도 기준
  - 일교차 고려 사항
  - 습도, 강수 확률, 풍속 영향
  - 일정 및 스타일 반영 방식
- **추가 팁**: 계절/기후별 실용적인 조언
  - 옷감 선택 팁
  - 레이어링 방법
  - 자외선 차단 등

### 2.5 샘플 날씨 프리셋
테스트용 미리 정의된 날씨:
- 봄 (선선한 날씨)
- 여름 (무더위)
- 가을 (쌀쌀한 날씨)
- 겨울 (추위)
- 비 오는 날

---

## 3. 실행 전 준비 사항

### 3.1 시스템 요구사항
- **Node.js**: v16 이상 (v18 이상 권장)
- **npm**: v7 이상 또는 **yarn**, **pnpm** 등의 패키지 매니저
- **운영 체제**: Windows, macOS, Linux 모두 지원

### 3.2 소프트웨어 설치 확인
프로젝트를 실행하기 전에 다음을 확인하세요:

```bash
# Node.js 버전 확인
node --version
# v18.0.0 이상이어야 합니다

# npm 버전 확인
npm --version
# v9.0.0 이상 권장
```

---

## 4. 설치 방법

### 4.1 프로젝트 다운로드

#### 방법 1: Git을 이용한 다운로드
```bash
git clone <repository-url>
cd project
```

#### 방법 2: 압축 파일 다운로드
1. 제공된 압축 파일 다운로드
2. 압축 해제
3. 터미널에서 프로젝트 폴더로 이동
```bash
cd project
```

### 4.2 의존성 설치

프로젝트 루트 디렉토리에서 다음 명령어를 실행합니다:

```bash
# npm을 사용하는 경우 (권장)
npm install

# 또는 yarn 사용
yarn install

# 또는 pnpm 사용
pnpm install
```

**설치 완료 시**: 프로젝트 폴더에 `node_modules` 디렉토리가 생성됩니다.

---

## 5. 실행 방법

### 5.1 개발 서버 시작

프로젝트의 루트 디렉토리에서 다음 명령어를 입력합니다:

```bash
npm run dev
```

**예상 출력**:
```
VITE v5.4.2  ready in 1234 ms

➜  Local:   http://localhost:5173/
➜  press h to show help
```

### 5.2 브라우저에서 앱 열기

위 출력에서 제시된 URL(`http://localhost:5173/`)을 브라우저의 주소 표시줄에 복사하여 Enter를 누릅니다.

또는 아래 단계를 따릅니다:
1. 웹 브라우저 열기 (Chrome, Firefox, Safari 등 모두 가능)
2. 주소 표시줄에 `http://localhost:5173/` 입력
3. Enter 키 누름

**앱이 성공적으로 로드되면**:
- "오늘 뭐 입지?" 헤더가 표시
- 왼쪽에 입력 폼과 날씨 정보 표시
- 오른쪽에 AI 추천 결과 표시 (기본 샘플 데이터 기반)

### 5.3 앱 종료

개발 서버를 종료하려면 터미널에서 `Ctrl+C`를 누릅니다.

---

## 6. 환경변수 설정 방법

### 6.1 기본 설정 (선택사항)

프로젝트 루트에 `.env.local` 파일을 생성합니다:

```bash
# Linux/macOS
touch .env.local

# Windows (PowerShell)
New-Item .env.local
```

### 6.2 .env.local 파일 수정

텍스트 에디터(VSCode, Sublime, 메모장 등)로 `.env.local` 파일을 열고 다음을 추가합니다:

```
# 기본값: 이 파일이 없어도 앱은 정상 작동합니다
# VITE_WEATHER_API_KEY=your_key_here
# VITE_WEATHER_API_URL=https://api.openweathermap.org/data/2.5
# VITE_SUPABASE_URL=your_url
# VITE_SUPABASE_ANON_KEY=your_key
```

### 6.3 확인 방법

`.env.example` 파일을 참고하여 필요한 환경변수를 확인할 수 있습니다:

```bash
cat .env.example  # Linux/macOS
type .env.example # Windows
```

---

## 7. API 키 설정 방법

### 7.1 현재 상태

현재 앱은 **샘플 데이터로 동작**하므로 API 키가 필요하지 않습니다. 아무 설정 없이도 테스트할 수 있습니다.

### 7.2 실제 날씨 API 연동 (향후 추가 예정)

실제 날씨 API를 연동하려면 (예: OpenWeather API):

#### Step 1: OpenWeather 회원가입
1. https://openweathermap.org/api 방문
2. 회원가입 또는 로그인
3. API 키 생성 및 복사

#### Step 2: .env.local에 키 추가
```bash
VITE_WEATHER_API_KEY=your_actual_api_key
VITE_WEATHER_API_URL=https://api.openweathermap.org/data/2.5
```

#### Step 3: 재시작
```bash
npm run dev
```

**참고**: 현재 버전에서는 이 설정이 적용되지 않으며, 샘플 데이터로만 동작합니다.

---

## 8. 테스트 방법

### 8.1 기본 기능 테스트

#### 시나리오 1: 기본 추천 받기
1. 앱 접속: `http://localhost:5173/`
2. 왼쪽 입력 폼에서 기본값 유지
3. "오늘 옷차림 추천받기" 버튼 클릭
4. 오른쪽에 추천 결과 표시 확인

**기대 결과**: 
- 상의, 하의, 신발 등 추천 항목 표시
- 추천 이유 설명
- 추가 팁 제공

#### 시나리오 2: 다양한 입력값 테스트
각각의 옵션을 변경하며 추천 결과 변화 확인:

1. **외출 시간대 변경**: 오전 → 저녁 (기온 변화)
2. **일정 변경**: 학교 → 운동 (활동성 반영)
3. **체감 성향 변경**: 보통 → 추위를 많이 탐 (보온 강조)
4. **스타일 변경**: 편한 스타일 → 단정한 스타일 (추천 옷 변경)

#### 시나리오 3: 날씨 프리셋 테스트
1. "샘플 날씨 변경" 드롭다운 클릭
2. 각 계절/상황 선택 (여름/겨울/비 등)
3. 각 날씨별 추천이 달라지는지 확인

**예상 변화**:
- **여름(무더위)**: 반팔, 반바지, 샌들 추천
- **겨울(추위)**: 기모 옷, 코트, 부츠 추천
- **비 오는 날**: 우산, 방수 신발 추천

#### 시나리오 4: 반응형 디자인 테스트

**모바일 환경 테스트**:
1. 브라우저 개발자 도구 열기 (F12 또는 Cmd+Option+I)
2. 반응형 디자인 모드 활성화 (Ctrl+Shift+M)
3. iPhone 12 또는 일반 모바일 선택
4. 입력 폼과 결과가 한 열로 정렬되는지 확인
5. 각 버튼과 입력창이 터치 친화적인지 확인

### 8.2 빌드 및 배포 테스트

프로덕션 빌드 생성:
```bash
npm run build
```

빌드 결과 확인:
- `dist` 폴더 생성 확인
- 폴더 크기 적절한지 확인 (보통 200KB 미만)

빌드된 앱 미리보기:
```bash
npm run preview
```

---

## 9. 폴더 구조

```
project/
├── src/
│   ├── components/
│   │   ├── InputForm.tsx           # 사용자 입력 폼 컴포넌트
│   │   ├── WeatherCard.tsx         # 날씨 정보 표시 카드
│   │   ├── RecommendationCard.tsx  # AI 추천 결과 카드
│   │   ├── TipsCard.tsx            # 추천 이유 및 팁 카드
│   │   └── WeatherSelector.tsx     # 샘플 날씨 선택 드롭다운
│   ├── lib/
│   │   ├── types.ts                # TypeScript 타입 정의
│   │   ├── sampleData.ts           # 샘플 날씨 데이터
│   │   └── recommender.ts          # AI 추천 로직 핵심 엔진
│   ├── App.tsx                     # 메인 앱 컴포넌트
│   ├── main.tsx                    # 진입점
│   ├── index.css                   # 전역 스타일
│   └── vite-env.d.ts               # Vite 타입 정의
│
├── public/                          # 정적 자산
├── .env.example                     # 환경변수 템플릿
├── .env.local                       # 로컬 환경변수 (실제값)
├── .gitignore                       # Git 무시 파일 목록
├── package.json                     # 프로젝트 의존성 및 스크립트
├── package-lock.json                # 의존성 정확한 버전 기록
├── vite.config.ts                   # Vite 설정
├── tailwind.config.js               # Tailwind CSS 설정
├── tsconfig.json                    # TypeScript 설정
├── eslint.config.js                 # ESLint 설정
└── README.md                        # 이 파일

### 주요 디렉토리 설명

- **src/components/**: 재사용 가능한 React 컴포넌트들
  - 각 컴포넌트는 단일 책임 원칙 준수
  - Props를 통한 데이터 전달로 느슨한 결합 유지

- **src/lib/**: 비즈니스 로직 및 유틸리티
  - `recommender.ts`: AI 추천 알고리즘의 핵심
    - `getRecommendation()`: 입력값과 날씨 데이터를 받아 최적의 옷차림 반환
    - 기온, 습도, 풍속, 일교차 등 모든 요소를 고려한 정교한 로직
  - `sampleData.ts`: 테스트용 미리 정의된 날씨 데이터
  - `types.ts`: TypeScript 인터페이스 정의로 타입 안전성 보장

---

## 10. 실행 시 주의사항

### 10.1 포트 충돌 해결

개발 서버 기본 포트는 `5173`입니다. 이미 사용 중인 경우:

```bash
# 자동으로 다음 포트 사용
npm run dev -- --port 3000
```

### 10.2 캐시 문제

이전 버전이 캐시된 경우:

```bash
# 브라우저 하드 새로고침
# Windows/Linux: Ctrl+Shift+Delete
# macOS: Cmd+Shift+Delete

# 또는 터미널에서 캐시 삭제 후 재시작
rm -rf .vite dist node_modules/.vite
npm run dev
```

### 10.3 Node 버전 불일치

Node 버전이 낮으면:

```bash
# Node 버전 확인
node --version

# nvm을 사용하는 경우 (macOS/Linux)
nvm install 18
nvm use 18

# 또는 직접 설치
# https://nodejs.org/en/ 에서 LTS 버전 다운로드
```

### 10.4 의존성 문제

의존성 설치 중 오류 발생 시:

```bash
# 기존 node_modules 완전 삭제
rm -rf node_modules package-lock.json

# npm 캐시 삭제
npm cache clean --force

# 재설치
npm install

# 재시작
npm run dev
```

### 10.5 개발 서버가 시작되지 않는 경우

```bash
# 1. Node 버전 확인 (v16 이상 필요)
node --version

# 2. 프로젝트 루트에서 명령 실행 확인
pwd  # 프로젝트 폴더 경로 확인

# 3. 패키지 재설치
npm install

# 4. TypeScript 타입 체크
npm run typecheck

# 5. 빌드 테스트
npm run build

# 모든 것이 OK면 다시 시작
npm run dev
```

### 10.6 데이터 기반 선택

**중요**: 현재 앱은 완전히 프론트엔드에서 동작하며, 샘플 데이터만 사용합니다.
- 수정된 추천 내용을 저장할 수 없음 (저장 기능 미포함)
- 새로고침 시 모든 입력값 초기화됨
- 다중 사용자 데이터 저장 불가 (로컬 저장소 미지원)

---

## 빠른 시작 가이드 (5분)

```bash
# 1. 프로젝트로 이동
cd project

# 2. 의존성 설치
npm install

# 3. 개발 서버 시작
npm run dev

# 4. 브라우저에서 http://localhost:5173/ 열기

# 5. 테스트하기
# - 위치/시간/일정 선택
# - "오늘 옷차림 추천받기" 클릭
# - 오른쪽에 추천 결과 확인
# - "샘플 날씨 변경"으로 다양한 날씨 테스트
```

---

## 기술 스택

| 기술 | 버전 | 용도 |
|------|------|------|
| React | 18.3.1 | UI 프레임워크 |
| TypeScript | 5.5.3 | 정적 타입 검사 |
| Vite | 5.4.2 | 번들러 및 개발 서버 |
| Tailwind CSS | 3.4.1 | 유틸리티 CSS 프레임워크 |
| Lucide React | 0.344.0 | 아이콘 라이브러리 |

---

## 기여 및 라이선스

이 프로젝트는 대학 과제로 제출되었습니다.

---

## 문제 해결

### Q: 앱이 로드되지 않습니다
**A**: 브라우저 콘솔(F12)을 확인하고 에러 메시지를 읽어주세요. 대부분 포트 충돌이나 의존성 설치 실패입니다.

### Q: 날씨 정보를 실시간으로 받을 수 있나요?
**A**: 현재는 샘플 데이터만 제공합니다. 실제 날씨 API 연동은 향후 추가될 예정입니다.

### Q: 추천 결과를 저장할 수 있나요?
**A**: 현재 저장 기능은 없습니다. 스크린샷으로 저장하거나 메모해주세요.

### Q: 모바일에서도 사용할 수 있나요?
**A**: 네! 반응형 디자인으로 모든 기기에서 최적화되었습니다.

---

## 연락처 및 지원

문제가 발생하거나 피드백이 있으시면, 프로젝트 이슈 탭에서 보고해주세요.

**Happy Coding!** 👕⛅
