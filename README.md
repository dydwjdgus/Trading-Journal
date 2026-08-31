# Trading Journal

이 프로젝트는 거래 기록을 입력하고, 손익/리스크를 계산하며, 분석 화면에서 성과를 확인할 수 있는 학습용 Next.js 앱입니다.

실제 서비스처럼 보이는 기능을 구현하면서, 다음 내용을 연습하는 데 초점을 맞췄습니다.

- React 컴포넌트 구조 설계
- 상태 관리와 폼 입력 처리
- 계산 로직 분리와 함수 설계
- 필터/정렬/검색 UI 구현
- 차트와 대시보드 구성
- 브라우저 로컬 저장소 기반 데이터 관리
- TypeScript 타입 설계

## 프로젝트 목적

이 프로젝트는 단순한 거래 일지 앱이 아니라, 프론트엔드 학습을 위해 구성된 실전형 예제 프로젝트입니다.

주요 학습 포인트는 다음과 같습니다.

- Next.js App Router 구조 이해
- TypeScript 기반 컴포넌트 설계
- 사용자 입력 폼 유효성 검증
- 수치 계산 로직과 UI 연결
- 대시보드/분석 화면 구성
- 데이터 모델 설계와 localStorage 활용

## 핵심 기능

- 거래 추가, 수정, 삭제
- 손익, 수수료, 리스크 계산
- 거래 유형별 필터링 및 정렬
- 세션/시스템/등급 기반 분석
- 통계 대시보드
- CSV/JSON import/export
- 설정 화면에서 시스템, 수수료, 세션 관리

## 기술 스택

- Next.js 15
- React 19
- TypeScript
- Tailwind CSS
- shadcn/ui
- Recharts
- date-fns
- Zod

## 실행 방법

### 1) 저장소 클론

```bash
git clone <repository-url>
cd Trading-Journal
```

### 2) 의존성 설치

이 프로젝트는 Yarn 기준으로 구성되어 있습니다.

```bash
yarn install
```

### 3) 개발 서버 실행

```bash
yarn dev
```

### 4) 브라우저 열기

```text
http://localhost:3000
```

## 프로젝트 구조

```text
.
├── app/                 # Next.js 앱 라우트
├── components/          # 화면 컴포넌트
│   ├── ui/              # 공통 UI 컴포넌트
│   ├── trade-form/      # 거래 입력 폼 관련
│   └── features/        # 기능별 컴포넌트
├── hooks/               # 커스텀 훅
├── lib/                 # 상수, 유틸, 검증 로직
├── types/               # TypeScript 타입
├── utils/               # 계산 및 도메인 유틸
├── public/              # 정적 파일
├── styles/              # 전역 스타일
├── package.json         # 프로젝트 설정
├── tailwind.config.ts   # Tailwind 설정
├── tsconfig.json        # TypeScript 설정
├── README.md            # 프로젝트 설명
└── sample-trades.csv    # 샘플 데이터
```

## 학습 관점에서 보는 주요 파일

### app/
- 앱 전체 진입점과 페이지 구조를 담당합니다.
- 라우팅과 페이지 레이아웃을 이해하는 데 좋습니다.

### components/
- UI를 작은 단위로 나누는 구조를 확인할 수 있습니다.
- 폼, 테이블, 차트, 다이얼로그, 설정 패널을 분리해서 보는 연습에 좋습니다.

### hooks/
- 상태 로직과 UI 로직을 분리하는 패턴을 학습할 수 있습니다.
- 필터링, 정렬, 계산 같은 로직을 훅으로 만들었는지 확인해보세요.

### utils/
- 비즈니스 계산을 별도 함수로 분리하는 방식을 배울 수 있습니다.
- 손익 계산, 리스크 계산, 세션 처리 로직을 확인해보는 것이 좋습니다.

### types/
- 타입 정의를 어떻게 구조화하는지 학습할 수 있습니다.
- 데이터 모델이 어떻게 설계되어 있는지 살펴보면 실무에 큰 도움이 됩니다.

## 연습 아이디어

다음 항목을 직접 수정해보면 학습 효과가 좋습니다.

1. 새로운 거래 필드 추가
   - 예: 전략명, 메모, 레버리지, 브로커

2. 계산 로직 개선
   - 예: 기대값(Expected R), 수익률, 최대 손실률 추가

3. 필터 기능 확장
   - 예: 거래 결과별 필터, 시간대별 분석, 시스템별 통계

4. 대시보드 시각화 추가
   - 예: 월별 수익 추이, 손실/이익 비율, 승률 그래프

5. 데이터 저장 방식 변경
   - localStorage 대신 API 또는 JSON 파일 기반 구조로 확장해보기

## 주의사항

- 이 프로젝트는 학습용 예제로 구성되어 있습니다.
- 실제 거래용 서비스로 사용하기 전에 데이터 검증, 보안, 백엔드 연동 등을 추가로 고려해야 합니다.
- 브라우저 기반 저장소를 사용하므로, 브라우저 환경과 데이터 유지 방식에 대한 이해가 필요합니다.

## 참고

- Next.js 문서: https://nextjs.org/docs
- React 문서: https://react.dev/
- TypeScript 문서: https://www.typescriptlang.org/
- Tailwind CSS 문서: https://tailwindcss.com/

## 추가로 공부하면 좋은 주제

- React 상태 관리 패턴
- custom hook 설계
- form validation with Zod
- Type-safe data modeling
- dashboard UI composition
- localStorage persistence patterns

이 프로젝트는 기능 구현 중심으로 빠르게 익히는 데 적합하고, 코드를 읽으며 구조를 이해하는 연습에도 좋습니다. 필요한 경우 다음 단계로는 "기능별 코드 설명" 또는 "이 프로젝트의 구조 분석 문서" 형태로 정리해드릴 수 있습니다.
- [Lucide](https://lucide.dev/) - Beautiful & consistent icon toolkit

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/yourusername/trading-journal/issues) page
2. Create a new issue with detailed information
3. Include screenshots and error messages when applicable

## 🗺️ Roadmap

### Upcoming Features
- [ ] Mobile app version
- [ ] Cloud sync capabilities
- [ ] Advanced backtesting tools
- [ ] Integration with more brokers
- [ ] Machine learning performance predictions
- [ ] Social trading features
- [ ] Advanced portfolio analytics
- [ ] Tax reporting tools

---

**Happy Trading! 📈**

*Remember: Past performance does not guarantee future results. Always trade responsibly and never risk more than you can afford to lose.*
