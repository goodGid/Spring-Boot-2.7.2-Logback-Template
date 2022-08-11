# Spring-Boot-2.7.3-Logback-Template

## Spec

* Java 11

* Spring Boot 2.7.3

* Gradle 7.5

* Logback 1.2.11


## Comment

* log 파일 생성을 위해 설정한 Path에 관련 directory가 없으면 자동으로 생성된다.

  ``` xml
  <file>logs/request1.log</file>
  --> `logs` directory는 자동으로 생성된다.
  ```

* [MDC를 사용해서 logback에 출력하려면 `%X{KEY}` 형식으로 사용하면 된다.](https://github.com/goodGid/Spring-Boot-2.7.3-Logback-Template/blob/main/src/main/resources/logback-spring-prod.xml#L38-L49)

  ``` xml
  <encoder>
    <pattern>%X{job}%n</pattern>
  </encoder>
  ```

* rollingPolicy에서 "SizeAndTimeBasedRollingPolicy"와 "TimeBasedRollingPolicy" 사용법

  ref : [appender name="ERROR" 참고](https://github.com/goodGid/Spring-Boot-2.7.3-Logback-Template/blob/main/src/main/resources/logback-spring-prod.xml#L51-L81)