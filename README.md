# JPA

📘 JPA 학습 정리 (with MyBatis 비교)

## 1. JPA란?
💡 객체를 DB에 자동으로 매핑해주는 ORM 기술

## 2. MyBatis vs JPA 차이
✨ MyBatis
   SELECT * FROM user WHERE id = 1;
   
✨ JPA
   userRepository.findById(1L);
   
💥 핵심 차이
| MyBatis   | JPA    |
| --------- | ------ |
| SQL 직접 작성 | 객체 중심  |
| 제어 쉬움     | 자동화    |
| 쿼리 튜닝 쉬움  | 추상화 높음 |
| 생산성 낮음    | 생산성 높음 |

## 핵심 3개
- Entity
- Repository
- 영속성 컨텍스트
👉 객체를 저장하면 바로 DB 안 감
👉 메모리에서 관리하다가 나중에 한 번에 반영

### MyBatis → JPA 느낀 점

- SQL 안 써서 편하지만 내부 동작이 안 보임
- 처음엔 답답함 (쿼리 어디서 나가는지 모름)
- 대신 생산성은 확실히 올라감

MyBatis → JOIN 직접 작성

JPA → 객체 참조로 관계 표현

## 연관관계 매핑 
JPA에서는 테이블이 아닌 객체 간 관계로 연관관계를 표현함.

1. Fetch Join
2. @EntityGraph
3. LAZY 전략 사용


### 영속성 컨텍스트 (Persistence Context)
- 엔티티를 저장하고 관리하는 1차 캐시

## 🔄 동작 흐름
1. Entity 생성
2. 영속성 컨텍스트 저장 (persist)
3. 트랜잭션 커밋
4. DB 반영

즉, 객체 → 영속성 컨텍스트 → DB




