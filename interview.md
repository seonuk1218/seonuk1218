결과적으로 제시해야 하는 것 

1. 수행내역
2. 최근 작업 내용
3. 직무 발전을 위한 노력

---
title: interview
markmap:
  colorFreezeLevel: 3
---

## resume

- 전문 메타데이터 배포 서비스 Rebuilding (iBatis to JPA)
  - 개요
  - 문제발생 및 분석
  - 수행내역
  - 결과 및 향후 개선과제
- KakaoBank-Card Blue/Green 배포를 위한 메타데이터 배포 Rolling옵션 개발
  - 개요
  - 문제발생 및 분석
  - 수행내역
  - 결과 및 향후 개선과제
- 사내 스터디 운영
  - 개요
  - 운영 방향
    - 단계별 도전과제 제시
    - 테스트베드 구축
    - 제품 도큐먼트 관리
    - Gitlab 설치와 Webhook, CRON Tab으로 상태 보고서 관리
  - 향후 개선과제
- elink-batch Update
  - 개요
  - 문제발생 및 분석
  - 수행내역
    - ERD 작성시 추가로 고려 했던 점이 있는지?
      인덱싱이라던지, 데이터 특성에 따른 처리
    - 왜 SpringBatch? 데이터 옮기는 똑똑한 사람들이 만든 추상화, Listener 자유로움 실패지점 재시작... 등
      왜 SpringIntegration? 파일 생성 이벤트 감지, Apache Mina SSHD로의 전환..
  - 결과 및 향후 개선과제
- MCI 리팩토링
  - 개요
  - 문제발생 및 분석
  - 수행내역
  - 결과 및 향후 개선과제

## Domain & Solution

- Recent 수행 Task
  - 대외파일배치 인터페이스 FEP Batch Interface 관리
    - KbCard(Sftp) <-> KakaoCard(S3 bucket)
  - S3 Adapter
    - KakoBank-Card 에서의 요구사항?
    - File Up&Download 
  - SFTP Connection Pooling (with ApacheCommonPool)
    - 기존 문제?
  - Truncate Account Switching with AOP
    - 문제?
  - Bandwidth InputStream 제작

- EAI (Hub & Spoke)
  - 제품 특징
  - 현대적인 EAI 제품이 되려면?
    - 타 제품 사례
    - ⭐️ 지속적인 DDD를 통한 솔루션 모듈화 관리 (Core, Extension...)
    - 강력 Monitoring 을 위한 오픈소스 통합 지원
      - Logging(ELK), Metric(Grafana), Tracing(???)
     
- Batch
  - 제품 특징
  - 현대적인 ETL 제품이 되려면?
    - 타 제품 사례 (Apache Airflow, Spring Cloud Data flow)
    - ⭐️ 지속적인 DDD를 통한 솔루션 모듈 관리 (Core, Extension...)
    - 강력 Monitoring 을 위한 오픈소스 통합 지원
      - Logging(ELK), Metric(Grafana), Tracing(???)

## Tech Research

- Gradle
	- Gradle 은 무슨 도구?
	- Build가 아니라 JIB?
- MSA
	- MSA 에서의 데이터 정합성 맞추기
		- CQRS (TODO 그림 제시)
			- CDC 로 정합성 맞추기
		- SAGA (TODO 그림 제시)
			- 	보상 트랜잭션
	- 전환 시 장점?
		- 도메인을 분리하는 것 만으로 좋은 설계를 유도할 수 있다고 생각
- 여러가지 Git Branching 전략
- DB
	- Master/Slave 구조의 MySQL, PostgreSQL, ...
		- Postgre	의 MVCC (Undo가 아니라 Tuple생성하여 가비지 발생 우려?)
	- READ/WRITE 전부 허용하는 Oracle, Tibero?
	- DB Appliance / 
	- MySQL 가이드 보면서 DB 부문 지식 강화
- Data PipeLine
  - Collect
  - Ingest
    - CDC or batch process
  - Compute
    - Batch Processing: Apache Spark, MapReduce, Hive
    - Stream Processing(real time data): Flink, Apache Storm ...
    - ETL (Extract Transform Load): Apache Airflow, AWS Glue ...
  - Store
    - Data lake (S3, HDFS 비정형데이터 / snowFlake ... 데이터웨어하우스)
- Spark
  - 핵심개념
  - Spark with springbatch (https://docs.spring.io/spring-hadoop/docs/current/reference/html/springandhadoop-spark.html) 예시 만들어보기
- CAP
- Data 를 다루는 기술
  - Relational Database
    - DB Layer Tranaction & control at Application Layer 
    - 정규화
    - ERD 설계
  - Key, Value Database Redis
    - Distributed Lock
  - Kafka
    - Message Broker Lock
  - HDFS
    - Data Transaction at Hadoop?
  - Stream API 를 보면 데이터가 보인다 (여러 자료구조에 따른 다양한 API 를 제공하므로 그 과정에서 데이터처리를 배울 수 있다.)
- Apache Ignite Cache
  - 개요
  - Property
  - 구성예제
- Kafka
  - 개요
  - Property
  - 구성예제
- Redis
  - Cache
  - Session Data
  - Replication (AOF, Snapshot)
  - Distributed Lock
  - Ray Limiter
- Logging (ELK)
  - 개요
  - Property
  - 구성예제
- Metric (Prometheus)
  - 개요
  - Property
  - 구성예제
- Tracing (Opentelementry)
- Transaction
- BDD
  - 테스팅은 내가 작성한 API 의 첫 고객이 내가 되어봄으로써 사용자의 입장을 생각할 수 있게 해보는 장점이 있다.
- DDD
- SAGA
  - choreography
  - orchestration
- CQRS
- SSL/TLS & mTLS
- key-pair
- JPA
- CI / CD
  - Rollout
  - Blue Green
  - Canary
- Encoding
- Container Orchestration
- NIO
- Resilience4J
- Algorithm
  - 알고리즘은 먼저 차수 측정!
 
- Zookeeper
- NginX
- Treafik
- Terraform

## Book

- Code Complete
  - 좋은 개발자가 된다는 것은?
    - 좋은 코드 작성
    - 정확하고 빠른 reasonable Query 작성
    - 트랜잭션에 대한 깊은 이해 100번 강조해도 아깝지 않다 그림과 함께~~~
- 데이터 중심 애플리케이션 설계
- 실용주의 프로그래머
  - 쓸만한 내용도 많으나 앞부분은 논리적으로 생각하면 당연한 내용들 같은 느낌??
- GoF 디자인패턴
  - 생성
  - 구조
  - 행동
- Refactoring 2판
