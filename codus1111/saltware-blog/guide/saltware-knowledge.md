# 솔트웨어 지식 파일

솔트웨어 유튜브(@saltware_youtube)와 기술 블로그(fitcloud.github.io)에서 모은 사실이다. 2026-11-02에 정리했다.
글에 쓸 때는 여기 있는 사실만 쓰고, 출처 링크를 함께 단다. 숫자가 없는 곳에 숫자를 만들어 넣지 않는다.

## 1. 회사와 서비스

- 2003년 창립. 예전 회사 소개 영상은 사업을 클라우드, 스마트팜, 비즈니스 통합 플랫폼 엔뷰(enView) 세 가지로 소개했다.
  - 클라우드: 민감 데이터가 있는 온프레미스와 클라우드를 잇는 하이브리드 환경
  - 스마트팜: 온습도·CO2 센서, LED 램프, 컨트롤러를 빅데이터와 이어 농업 생산 자동화
  - 엔뷰: 사내에 흩어진 자원을 모아 조직 소통을 돕는 플랫폼
  - 출처: https://www.youtube.com/watch?v=ViCZPJxyB_Y
- 최근 소개 영상: Cloud, ISV, Smartfarm, Portal Solution으로 기업의 디지털 전환을 함께해 왔고, 이제 모든 서비스에 AI를 결합한다. (https://www.youtube.com/watch?v=ozsUF6KlyFw)
- 클라우드 서비스 브랜드: FitCloud (https://fitcloud.co.kr)

### Sapie 생성형 AI 시리즈
- 2025 AWS Summit Seoul에서 공개 (https://www.youtube.com/watch?v=gqJAlmk4DEQ)
  - Sapie Bot: 대화형 AI 챗봇
  - Sapie Reco: Amazon Bedrock 기반 개인화 추천
  - Sapie LLM: 기업 데이터 기반 학습, 보안을 갖춘 정보 탐색과 문서 생성
- Sapie-Guardian: 기밀·개인정보 유출을 실시간 탐지·차단하는 AI 보안 서비스 (https://www.youtube.com/watch?v=O_fvweh8jps)
- Sapie-Braille: LLM 기반 점역 솔루션, 실시간 점자 변환. 시각장애인 정보 접근성 (https://www.youtube.com/watch?v=8PnBApm_0MA)

### 그 밖의 서비스
- 쿠버네티스 센터: 2024 AWS Summit Seoul에서 소개. 고객 맞춤형 쿠버네티스 교육, 구성, 오픈소스 매니지드 서비스 (https://www.youtube.com/watch?v=L0_ptayeI4s)
- 금융 클라우드 컴플라이언스 지원 서비스 다섯 가지 (https://www.youtube.com/watch?v=MSI5E_OPG3Q)
  1. 보안 아키텍처 설계 및 구축
  2. 전자금융감독규정에 따른 중요도 평가
  3. 업무 연속성 및 안전성 확보
  4. CSP 안전성 평가
  5. 물적 요건 대응

### 행사
- AWS re:Invent 2024(라스베이거스)에서 솔트웨어 고객사 미리디가 세션 발표 (https://www.youtube.com/watch?v=fpbUjL4lMl4)
- 2022 교육정보화 컨퍼런스: 최상철 상무, "하이브리드 클라우드 시장 전망과 전략" (https://www.youtube.com/watch?v=vxyBNW_9908)

## 2. 고객 사례 (솔트웨어 기술 블로그)

### 크몽 (2020-02-27 게시) https://fitcloud.github.io/CaseStudy-Kmong-ko/
- 처음엔 AWS에서 모놀리식 구조로 시작. 인력이 100명 가까이 늘고 서비스가 커지면서 문제가 생김
- 배포에 2~3시간이 걸렸고, 그동안 관련 개발자는 다른 일을 못 하고 기다림
- 배포가 주 단위 또는 2주 단위라 업데이트가 느림
- 솔트웨어가 한 일: 2-Tier 웹서비스 구조 제안, 각 Tier 이중화와 Multi-AZ, AutoScaling, 서버리스 Fargate, AWS Code 시리즈로 CI/CD, CloudWatch Logs + ElasticSearch로 통합 모니터링, Agile 방식으로 진행해 크몽 엔지니어가 이후에도 쓰게 함
- 사용 서비스: API Gateway, CodeCommit, CodeBuild, CodeDeploy, CodePipeline, CloudFormation, ECS(Fargate, ECR), CloudWatch, ElasticSearch, IAM, ELB, RDS
- 결과(정성): 팀별 계정 분리로 리소스 사용량 파악, 서버 관리 부담 해소, 배포 편의성 증가, 서비스 분리로 배포 시간과 릴리스 기간 단축, 개발·테스트·운영 지출 감소. 숫자는 공개되지 않음

### 리파인 (2020-03-04 게시) https://fitcloud.github.io/CaseStudy-Refine-ko/
- B2B 서버 개발 중심 회사. 온프레미스에서 국내 클라우드로 옮겼다가 기능·성능 문제로 AWS로 재이전. 개인정보 영역을 빼고 대부분 AWS에서 운영
- 새 사업으로 B2C 모바일 서비스가 필요해짐. 사내에 모바일 개발 인력이 없었고, 클라우드 기반 모바일 개발 경험도 없었음. 짧은 기간에 성과를 내야 했음
- 솔트웨어가 한 일: AWS Amplify 기반 개발과 최적화, 서버리스 요건에 맞춰 MSA와 DevOps 적용
- 사용 서비스: Amplify(Amplify Console로 Git·CodeCommit·CodeBuild·배포), CloudFormation, API Gateway, SQS, CloudWatch, ElasticSearch, IAM, ELB, RDS
- 결과(정성): 팀별 계정과 VPC 분리로 사용량 파악과 보안 향상, 배포 시간과 릴리스 기간 단축, 기존 서버 개발 인력으로 모바일 개발을 하게 되어 비용 절감. 숫자는 공개되지 않음

## 3. 세미나 내용

### AWS 금융 클라우드 도입 현황 (함인용 실장, 공중기 매니저) https://www.youtube.com/watch?v=R0zLDexN5D4
- 50페타바이트는 기원전 4000년부터 2006년까지 사람이 만든 텍스트 양에 해당한다는 자료가 있다
- 100페타바이트를 1TB 하드디스크로 담으면 약 10만 2,400개. 두께 0.8cm짜리를 쌓으면 영암 월출산 높이쯤 된다 (발표자 계산)
- 데이터 처리의 기본 3단계: 수집, 저장, 분석. 수집은 많이 모으기보다 잘 모으기가 중요 (Garbage in, garbage out)
- 빅데이터 3V: 볼륨(크기), 벨로시티(속도: 배치·실시간·스트림), 버라이어티(정형·반정형·비정형)
- 금융권 활용 예: 시장 위기관리, 이상거래 탐지, 자금세탁방지, 소셜·모바일 데이터 분석, 실시간 이벤트
- 기존 데이터웨어하우스·데이터마트를 버리지 말고, 다른 성격의 데이터를 데이터 레이크에 두고 기존 것과 결합하라
- 데모 구성: Kinesis로 수집 → S3에 저장 → Athena로 SQL 조회 → QuickSight로 시각화. Glue로 ETL
- 비유: 무라카미 하루키는 장편을 바로 쓰지 않고 에세이, 단편을 먼저 쓰고 그것을 엮어 장편을 쓴다. 빅데이터도 처음부터 큰 그림을 한 번에 그리기보다 작은 과제부터 하나씩 해 보라
- 클라우드에서는 장비 구매·설치 같은 사전 작업이 없어지고, 데이터로 무엇을 할지에만 집중할 수 있다

### AWS를 활용한 Data Analytics (정영우 SA) https://www.youtube.com/watch?v=0iuvRXVC8OA
- 실시간 데이터가 필요한 이유: 데이터가 생긴 순간 반응할수록 결정이 빨라진다. 1분 뒤, 하루 뒤 분석은 각각 쓰임이 다르다
- 흐름: 소스(앱 로그, IoT 센서, 웹 클릭) → 스트림 → 임시 저장 → 처리·분석 → 데이터 레이크나 DB에 영구 저장
- 데이터를 보내는 쪽은 프로듀서, 받아 쓰는 쪽은 컨슈머
- Kafka 같은 스트림 서버를 직접 만들면 구축, 확장, 고가용성, 연동 개발, 운영이 모두 부담. 그래서 관리형 서비스 Amazon Kinesis를 쓴다
- Kinesis Data Streams: 샤드 단위로 용량을 늘리고 줄인다. 데이터를 일정 기간 임시 보관하고 다시 읽을 수 있다
- Kinesis Data Firehose: 받은 데이터를 잠시 모았다가 S3, Redshift, OpenSearch, Splunk 같은 목적지로 한꺼번에 보낸다(푸시). 샤드 관리가 필요 없다. Lambda로 중간에 데이터를 바꿀 수 있다
- Kinesis Data Analytics: 흘러오는 데이터를 저장하지 않고 SQL이나 Apache Flink로 실시간 분석. 예: 5분마다 평균 온도를 보고 기준을 넘으면 알림
  - 참고: 이 서비스는 2023년 Amazon Managed Service for Apache Flink로 이름이 바뀌었다 (https://aws.amazon.com/managed-service-apache-flink/)
- 현장 예시(발표자 소개): 국내 한 건설사 아파트에서 차량 번호판을 인식하면 그 집 층으로 엘리베이터를 미리 불러 둔다
