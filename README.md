# JPA

## 1. JPA란?
💡 객체를 DB에 자동으로 매핑해주는 ORM 기술

## 2. MyBatis vs JPA 차이
- MyBatis
 ✨ SELECT * FROM user WHERE id = 1;
- JPA
 ✨ userRepository.findById(1L);
💥 핵심 차이
| MyBatis   | JPA    |
| --------- | ------ |
| SQL 직접 작성 | 객체 중심  |
| 제어 쉬움     | 자동화    |
| 쿼리 튜닝 쉬움  | 추상화 높음 |
| 생산성 낮음    | 생산성 높음 |
