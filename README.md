# Best-seller-prediction
## 내가 추천하는 책이 베스트 셀러가 될까?

### 1. 문제 배경
- 도서 OTT 서비스로 인해 온라인 서점 이용자 수가 감소함

### 2. 문제 정의
- 이용자 욕구에 맞는 서비스를 제공하여 온라인 서점 방문객 수를 늘려야 함

### 3. 서비스 정의
1) '에디터 추천 신간' 개편
- 현재 에디터 추천 신간은 출판사 마케팅 공간이라는 인식이 강함
- 독자 선호가 높은 추천 신간 비중을 늘려 도서 OTT 서비스와 차별화할 필요가 있음

2) 독자 선호도가 높은 도서를 추천하기 위해 **베스트 셀러가 될 확률**을 알려주는 어플리케이션 개발

### 4. 서비스 설계
1) 데이터 수집 및 DB 구축
![스크린샷 2022-02-15 오후 2 59 48](https://user-images.githubusercontent.com/93904398/165765345-25d08e84-c84f-4ae6-aac0-898a4d263314.png)

- 알라딘 API로 도서 정보 수집
- MySQL 스키마 구성 및 데이터 적재
 - 베스트 셀러 목록
 - 신간 추천 목록
 - 카테고리 정보
- 타겟 데이터 설정
 - 신간 추천 테이블에 베스트 셀러 테이블을 레프트 조인 -> 조인 후 생긴 Null 값을 베스트 셀러 여부를 판단하는 칼럼으로 활용

2) 머신러닝 기반 앱 개발 및 메타베이스 시각화

![스크린샷 2022-02-15 오후 3 46 13](https://user-images.githubusercontent.com/93904398/165766160-a96af90b-cb15-47f4-8029-b55f6814e70a.png)

### 5. 대시보드(메타베이스) 결과 요약
- 독자는 작가보다 장르에 따라 책을 구매함
- 장르 다양성 보존 및 출판사 마케팅 정책에 따라 여러 장르의 책이 골고루 추천되고 있음
- 추천 신간의 가격 분포와 베스트 셀러의 가격 분포는 대체로 일치함

### 6. 제안
- 같은 작가를 여러분 추천하는 것보다 유망한 장르는 추천할 것을 제안함
- 만화, 자격증, 수험서 등 비문학과 실용서에 대한 소개 비중을 늘릴 필요가 있음
- 추천 신간과 베스트셀러의 가격 분포는 대체로 일치하기 때문에 별도의 조정이 필요해보이지 않음