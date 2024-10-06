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
    - 타 제품 사례
    - ⭐️ 지속적인 DDD를 통한 솔루션 모듈 관리 (Core, Extension...)
    - 강력 Monitoring 을 위한 오픈소스 통합 지원
      - Logging(ELK), Metric(Grafana), Tracing(???)

## Tech Research

- Spark
  - 핵심개념
  - Spark with springbatch
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
- DDD
- SAGA
- CQRS
- SSL/TLS & mTLS
- key-pair
- JPA
- CI
- Encoding
- Container Orchestration
- NIO
- Resilience4J
- Zookeeper
- NginX
- Treafik
- Terraform
