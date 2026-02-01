# Logback MDC Demo

Spring Boot에서 MDC(Mapped Diagnostic Context)를 활용한 요청 추적 로깅 예제 프로젝트

## 주요 기능

- MDC를 활용한 요청별 고유 ID 부여
- 분산 시스템에서의 요청 추적 (Distributed Tracing)
- 비동기 처리 시 MDC 컨텍스트 전파
- Logback 패턴 설정

## 핵심 개념

- MDC는 ThreadLocal 기반으로 동작
- 각 HTTP 요청은 별도의 스레드에서 처리됨
- 요청별로 독립적인 컨텍스트 정보 유지 가능

## 기술 스택

- Java 17
- Spring Boot 3.x
- Logback
- Gradle

## 실행 방법

```bash
./gradlew bootRun
```

## 프로젝트 구조

```
src/main/java/com/example/demo/
├── LogbackMdcDemoApplication.java
├── config/
│   ├── AsyncConfig.java
│   └── MdcTaskDecorator.java
├── controller/
│   └── DemoController.java
├── filter/
│   └── MdcLoggingFilter.java
└── service/
    ├── AsyncDemoService.java
    └── OrderService.java
```
