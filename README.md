# CI/CD 실습 교육 과정: 초간단 연말정산 계산기 프로젝트

이 프로젝트는 GitHub Actions를 활용한 CI/CD 실습 교육 과정의 일부입니다. 학생들은 간단한 연말정산 계산기 애플리케이션을 통해 현대적인 소프트웨어 개발 및 배포 프로세스를 학습하게 됩니다.

## 교육 목표

- Git 및 GitHub 사용법 숙달
- CI/CD 파이프라인 구축 및 이해
- 자동화된 테스트 및 배포 프로세스 경험
- 컨테이너화 및 클라우드 배포 실습

## 주요 기술 스택

- Python
- GitHub Actions
- Docker
- 네이버 클라우드 플랫폼

## 실습 내용

1. **VPC환경내에 서버 생성**: Public VPC에 ACL을 설정하고 Rocky linux를 생성
2. **유닛 테스트 자동화**: 코드 변경 시 자동으로 테스트 실행
3. **보안 점검**: Bandit을 이용한 코드 보안 취약점 검사
4. **코드 품질 관리**: pylint를 통한 코드 품질 검사
5. **Docker 컨테이너화**: 애플리케이션의 컨테이너화 및 멀티 아키텍처 빌드
6. **클라우드 배포**: 네이버 클라우드 VM에 자동 배포

## 시작하기

1. 이 저장소를 포크합니다.
2. 로컬 환경에 클론합니다:
   ```
   git clone https://github.com/your-username/tax_calculator.git
   ```
3. 필요한 의존성을 설치합니다:
   ```
   pip install -r requirements.txt
   ```
4. 로컬에서 애플리케이션을 실행합니다:
   ```
   uvicorn main:app --host 0.0.0.0 --port 8000 --reload 
   ```

## GitHub Actions 워크플로우

이 프로젝트에는 다음과 같은 GitHub Actions 워크플로우가 포함되어 있습니다:

- `unit-tests.yml`: 유닛 테스트 실행
- `security-check.yml`: 보안 취약점 검사
- `docker-build-push.yml`: Docker 이미지 빌드 및 푸시
- `deploy-to-naver-cloud.yml`: 네이버 클라우드 VM에 배포

각 워크플로우 파일의 내용을 확인하고 필요에 따라 수정해보세요.

## 워크플로우 사전작업

1. NCP 포털 마이페이지에서 공개키, 비밀키를 획득
2. 워크플로우에 등록된 secrets을 등록합니다. (Settings>Secret and Variables>Actions)

## 퀘스트

1. 새로운 기능을 추가하고 해당 기능에 대한 유닛 테스트를 작성하세요.
2. 보안에 취약하도록 코드를 추가/수정하세요.
3. Bandit 보안 점검 결과를 분석하고 발견된 취약점을 수정하세요.
4. 네이버 클라우드 VM 배포 프로세스를 개선하세요.
5. 변경 작업마다 워크플로우가 정상 작동하는지 확인하세요.

## 도움말 및 문의

문제가 발생하거나 질문이 있는 경우, Issues 탭을 통해 문의해주세요.

즐거운 학습 되세요!!!
```