```console
$ whoami
장혁 · Backend Developer (Java / Spring)
```

기능을 만든 뒤 직접 계측을 붙여 문제를 재현하고, 같은 조건의 측정으로 개선을 확인하는 백엔드 개발자입니다.

[![Blog](https://img.shields.io/badge/Blog-janghyeok.tistory.com-1a7f37?style=flat-square&logo=tistory&logoColor=white)](https://janghyeok.tistory.com/)
[![Email](https://img.shields.io/badge/Email-wkdgur456789%40gmail.com-0969da?style=flat-square&logo=gmail&logoColor=white)](mailto:wkdgur456789@gmail.com)

## Now

- 💼 백엔드 개발자로 재직 중 (2026.07 ~)
- 🎓 경성대학교 컴퓨터공학과 (2027.02 졸업 예정)
- 📜 정보처리기사

## Featured Project · HighTeenDay

고등학생 대상 익명 커뮤니티의 백엔드입니다. 동아리 프로젝트 리드로 게시글·댓글·인기글·파일 업로드를 개발했고, 지금은 혼자 유지보수합니다.

`Java 17` `Spring Boot 3.4` `JPA` `QueryDSL` `MySQL 8` `Redis` `Docker` `AWS`

| 개선 | 전 | 후 |
|---|---:|---:|
| 댓글 목록 요청당 평균 SQL 수 | 1,507 | 3.9 |
| 같은 혼합 시나리오의 전체 p95 | 226.7ms | 34.3ms |

<sub>같은 데이터셋·부하로 단계마다 5회씩 실행한 평균입니다(로컬 측정). 측정 과정은 [사례 문서](https://github.com/JangHyeok2909/highteenday-backend/blob/main/performance/cases/comment-query-amplification.md)와 [블로그 글](https://janghyeok.tistory.com/57)에 있습니다.</sub>

- 댓글·반응·스크랩을 트랜잭션 커밋 뒤 Redis Sorted Set 인기글 점수에 반영하고, 날짜별 키에 TTL 적용
- 조회수 증가분을 Redis에 모아 60초마다 DB에 반영하고, 반영에 성공한 만큼만 차감해 실패분은 다음 주기에 재시도
- 부하 실험 도구가 조건이 다른 실행을 기준선으로 골라 회귀를 잘못 보고하던 문제를 비교 조건 검사로 차단 · [실행 기록](https://janghyeok2909.github.io/highteenday-backend/)

**→ [highteenday-backend](https://github.com/JangHyeok2909/highteenday-backend)**

## Open Source

- **spring-boot-data-source-decorator** [#198](https://github.com/gavlyukovskiy/spring-boot-data-source-decorator/pull/198) · 머지됨 (2026.10.21) · [블로그 글](https://janghyeok.tistory.com/66)  
  라이브러리가 Spring Boot BOM을 사용하는 쪽에 전파해 의존성 버전을 바꾸던 문제 수정
- **springdoc.github.io** [#108](https://github.com/springdoc/springdoc.github.io/pull/108) · 응답 대기  
  v2 문서의 Spring Boot 호환 표 정리

## Tech Stack

![Java](https://img.shields.io/badge/Java_17-1f2328?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring_Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/JPA_(Hibernate)-59666C?style=flat-square&logo=hibernate&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-0769AD?style=flat-square)
![MyBatis](https://img.shields.io/badge/MyBatis-B52E31?style=flat-square)

![MySQL](https://img.shields.io/badge/MySQL_8-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![Flyway](https://img.shields.io/badge/Flyway-CC0200?style=flat-square&logo=flyway&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2_·_S3-232F3E?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)

![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)

## Recent Posts

<!-- BLOG-POST-LIST:START -->
- [라이브러리가 함께 배포한 Spring Boot BOM 때문에 앱이 뜨지 않던 문제: 오픈소스에 이슈를 올리고 PR이 머지되기까지](https://janghyeok.tistory.com/66) <sub>2026.10.25</sub>
- [LLM 기초 개념을 주제로 첫 테크세션을 이끌다](https://janghyeok.tistory.com/64) <sub>2026.10.22</sub>
- [요청당 쿼리수를 관측하여 N+1 파악과 해결](https://janghyeok.tistory.com/57) <sub>2026.10.15</sub>
- [LLM 서빙 용어 정리: vLLM, TTFT, Prefill과 Decode, KV 캐시, Thinking, 샘플링 파라미터](https://janghyeok.tistory.com/55) <sub>2026.09.27</sub>
- [아키텍쳐 정리](https://janghyeok.tistory.com/54) <sub>2026.06.27</sub>

<!-- BLOG-POST-LIST:END -->

<sub>블로그 RSS를 매일 읽어 자동으로 갱신합니다.</sub>

## Algorithm

[![Solved.ac Profile](https://mazassumnida.wtf/api/v2/generate_badge?boj=wkdgur456789)](https://solved.ac/wkdgur456789/)
