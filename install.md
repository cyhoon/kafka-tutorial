### 발표 순서

### 도커 쉘 진입하기

docker exec -ti {CONTAINER} /bin/bash

1. kafka 기본 개념 소개

- 카프카란?
- 카프카 구성요소 ( 토픽, 파티션, 프로듀서, 컨슈머, 그룹 컨슈머, 브로커
- 카프카 어떻게 활용할까?
- 카프카 설치하기 ( 도커 )
- 카프카 기본으로 써보기
- node에 붙여보기

### 카프카 명령어 파일 디렉터리

/opt/kafka 로 이동한다.

### 카프카 토픽 생성 방법

./bin/kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic test

### 생성된 카프카 토픽 리스트 뽑기

./bin/kafka-topics.sh --list --zookeeper zookeeper:2181

### 특정 토픽에 메시지 보내기

bin/kafka-console-producer.sh --broker-list localhost:9092 --topic test

### 메시지 가져오기

bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic test --from-beginning

### 브로커 갯수 확인하기

bin/broker-list.sh
