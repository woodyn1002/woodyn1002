# :man_technologist: WooJin Choi (woodyn1002)
:pencil2: Blog: https://velog.io/@woodyn1002
* 안녕하세요! 저는 신입 백엔드 개발자를 꿈꾸는 학생 개발자 최우진입니다.
* 문제를 비판적으로 바라보고, 해결책을 찾으러 논리적으로 파고드는 것을 좋아합니다.
* 남들이 읽기 쉬운 코드나 문서를 작성하는 일을 즐깁니다.
* 프로젝트에서 생긴 이야기들을 [블로그](https://velog.io/@woodyn1002)에 남기고 있습니다.
# 🛠️ Skills
* Java, Kotlin
* Gradle
* Spring Boot, Spring MVC
* Spring Data JPA, Hibernate
* MySQL
* JUnit5, Mockito
* Git
# :clipboard: Projects
## 수업 관리 플랫폼 'pullgo'
> 소규모 학원들을 위한 수업 관리와 시험 응시 플랫폼

:octocat: Repo: https://github.com/FirstianB101/pullgo-server
### 📝 프로젝트 개요
* 자체적인 홈페이지를 갖지 않는 소규모 동네 학원들을 위해 수업 관리와 시험 응시 기능을 제공하는 플랫폼입니다.
* 총 5인 구성의 팀으로 진행했습니다.
### 📅 진행 기간
* 2021년 1월 ~ (진행중)
### :raising_hand_man: 수행 내용
* 팀원 1인과 함께 백엔드 서버 개발 파트를 맡았습니다.
* 팀원과 함께 도메인 [Entity 모델링](https://drive.google.com/file/d/1KIiR9p_zbi99eTOl9kfQb_ljQgN4wq2h/view?usp=sharing)과 [REST API 설계](https://api.pullgo.kr/v1/docs/api-guide.html)를 진행했습니다.
* 개발 초기에는 페어 프로그래밍을 진행했고, 이후에는 GitHub의 [Issues](https://github.com/FirstianB101/pullgo-server/issues?q=is%3Aissue+is%3Aclosed)와 [Pull Requests](https://github.com/FirstianB101/pullgo-server/pulls?q=is%3Apr+is%3Aclosed) 기능을 활용해 협업을 효율적으로 수행했습니다.
* 중요한 의사결정이 필요하면 주어진 선택지의 각 장단점을 분석하고 팀원과 의견을 조율했습니다.
* 원활한 소통을 위해 Pull Request에서 Issue의 해결 방식을 논리적으로 설명하고, 수정한 코드를 검증하는 테스트 코드를 함께 커밋했습니다.
* 추가로 인증/인가 기능 개발과 API 문서화, 간단한 배포 자동화 시스템 구축을 도맡아 진행했습니다.
### 🛠️ 주요 기술
* Java, Lombok
* Gradle
* Spring Boot, Spring MVC, Spring Security
* Spring Data JPA, Hibernate
* MySQL
* JUnit, Mockito
* Spring REST Docs
* Git, GitHub
### 📄 프로젝트 관련 자료
* [REST API 가이드 문서](https://api.pullgo.kr/v1/docs/api-guide.html)
* [프로젝트 진행 회고록](https://velog.io/@woodyn1002/series/poolgo)
## 수강 신청 서버 애플리케이션 'my-klas'
> 수강 신청에서 많은 트래픽을 버텨낼 수 있도록 연구하고 개선해보기 위한 토이 프로젝트

:octocat: Repo: https://github.com/woodyn1002/my-klas

📝 프로젝트 개요
* 큰 트래픽이 발생하는 수강 신청에서, 사용자 경험을 위해 응답 시간을 개선해보기 위해 진행한 개인 프로젝트입니다.
* 2000명의 학생이 6개 강의를 연달아 신청하며, 이때 인기 강의의 존재로 20%의 요청이 만석으로 인해 실패하는 상황을 가정했습니다.
* 블로그에 [개선 과정과 고민들](https://velog.io/@woodyn1002/series/my-klas)을 기록해가며 진행했습니다.
### 📅 진행 기간
* 2021년 4월 9일 ~ 2021년 5월 7일
### :raising_hand_man: 수행 내용
* 낙관적 락과 비관적 락을 비교하는 도중 발생한 [데드락을 MySQL의 `SHOW ENGINE` 명령어의 도움으로 해결](https://velog.io/@woodyn1002/my-klas-%EB%82%99%EA%B4%80%EC%A0%81-%EB%9D%BD-vs-%EB%B9%84%EA%B4%80%EC%A0%81-%EB%9D%BD)했습니다.
* JVM에 대한 이해를 기반으로 시뮬레이션 중 [Warm-up을 수행](https://velog.io/@woodyn1002/my-klas-%EB%B6%80%ED%95%98-%ED%85%8C%EC%8A%A4%ED%8A%B8-%EC%8B%9C%EB%AE%AC%EB%A0%88%EC%9D%B4%EC%85%98)하여 평균 응답 시간을 개선했습니다. (약 1000ms 개선)
* Spring Boot Actuator로 수집한 Metrics를 시각화하여, [HikariCP 최대 풀 크기에 의한 병목을 밝혀내어 해결](https://velog.io/@woodyn1002/my-klas-%EB%B3%91%EB%AA%A9-%ED%95%B4%EA%B2%B0%ED%95%98%EA%B8%B0)했습니다. (약 1700ms 개선)
* [MySQL Slow Query Log를 활용하여 특정 쿼리에 의한 성능 저하를 찾아](https://velog.io/@woodyn1002/my-klas-%EC%BF%BC%EB%A6%AC-%EA%B0%9C%EC%84%A0-1)내어 쿼리를 개선했습니다. (약 950ms 개선)
* [`ConcurrentHashMap`을 통해 만석 강의를 캐싱하는 로직을 작성](https://velog.io/@woodyn1002/my-klas-%EC%BF%BC%EB%A6%AC-%EA%B0%9C%EC%84%A0-2)했습니다. (약 60ms 개선)
* 2000명의 학생이 6개 강의를 동시 신청할 때, 최종 결과 평균 응답 시간 383ms로, 사용자 경험을 개선하는 데에 성공했습니다.
### 🛠️ 주요 기술
* Kotlin
* Spring Boot, Spring MVC
* Spring Data JPA, Hibernate
* MySQL
### 📄 프로젝트 관련 자료
* [프로젝트 진행 회고록](https://velog.io/@woodyn1002/series/my-klas)
