# 구현 계획

- [ ] 1. 프로젝트 스캐폴딩 및 설정
  - frontend와 backend 폴더로 프로젝트 디렉토리 구조 생성
  - Vite를 사용하여 TypeScript로 React 프론트엔드 초기화 (npm create vite@latest frontend -- --template react-ts)
  - TypeScript와 Express로 Node.js 백엔드 초기화 (npm init, express, typescript, @types/node 설치)
  - 메시지 테이블을 위한 간단한 스키마로 SQLite 데이터베이스 설정
  - 프론트엔드와 백엔드 모두를 위한 TypeScript 컴파일 구성
  - 프론트엔드와 백엔드에서 사용하는 Message 인터페이스를 위한 공유 타입 파일 생성
  - 개발을 위한 기본 package.json 스크립트 설정 (dev, build, start)
  - 워크샵 참가자를 위한 설정 지침이 포함된 간단한 README 생성
  - _요구사항: 3.1, 3.2, 3.3_

- [ ] 2. 채팅 애플리케이션 구축
  - CORS 미들웨어와 JSON 파싱을 포함한 Express 백엔드 서버 생성
  - SQLite 데이터베이스에 메시지를 저장하는 POST /api/messages 엔드포인트 구현
  - 최신순으로 정렬된 모든 메시지를 반환하는 GET /api/messages 엔드포인트 구현
  - 메시지 상태를 관리하고 API 호출을 처리하는 React App 컴포넌트 구축
  - 입력 필드, 제출 버튼, 기본 유효성 검사가 포함된 MessageForm 컴포넌트 생성
  - 타임스탬프와 함께 메시지 목록을 표시하는 MessageFeed 컴포넌트 생성
  - 깔끔하고 간단한 인터페이스를 위한 기본 CSS 스타일링 추가
  - API 실패와 빈 메시지 유효성 검사를 위한 오류 처리 구현
  - 전체 플로우 테스트: 메시지 게시, 피드에 나타나는지 확인
  - _요구사항: 1.1, 1.2, 1.3, 1.4, 2.1, 2.2, 2.3, 2.4, 3.1, 3.2, 3.4_

- [ ] 3. AWS 인프라스트럭처 코드 구축
  - TypeScript로 AWS CDK 프로젝트 초기화 (cdk init app --language typescript)
  - 공개 읽기 액세스가 가능한 정적 웹사이트 호스팅을 위한 S3 버킷 생성
  - aws-lambda-express 어댑터를 사용하여 Express 백엔드를 실행하는 Lambda 함수 설정
  - Lambda 함수로 HTTP 요청을 라우팅하는 API Gateway 구성
  - Lambda 함수 모니터링을 위한 CloudWatch 로깅 추가
  - 프론트엔드를 빌드하고 S3에 업로드하며 백엔드를 배포하는 배포 스크립트 생성
  - 프론트엔드 액세스를 허용하는 API Gateway CORS 설정 구성
  - 라이브 애플리케이션 URL에 액세스하여 배포 테스트
  - _요구사항: 3.1, 3.2, 3.3, 3.4_

- [ ] 4. Playwright로 엔드투엔드 테스트 구축
  - TypeScript용 Playwright 설치 및 구성 (npm init playwright@latest)
  - 애플리케이션을 열고 페이지가 올바르게 로드되는지 확인하는 테스트 작성
  - 새 메시지를 게시하고 피드에 나타나는지 확인하는 테스트 생성
  - 빈 메시지 유효성 검사 테스트 추가 (제출 버튼 비활성화 또는 오류 표시)
  - 여러 메시지가 올바른 순서로 표시되는지 확인하는 테스트 작성 (최신순)
  - 로컬 개발 환경과 배포된 AWS 환경 모두에서 테스트를 실행하도록 Playwright 구성
  - Playwright의 내장 접근성 테스트를 사용한 기본 접근성 테스트 추가
  - 간단한 테스트 보고서 생성 및 CI 준비 구성 생성
  - _요구사항: 1.1, 1.2, 1.4, 2.1, 2.2, 2.3, 2.4_
