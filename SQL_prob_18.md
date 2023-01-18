>> ## 프로그래머스 SQL 
>> #### 1/18(수) 

***


['조건에 맞는 도서 리스트 출력하기'](https://school.programmers.co.kr/learn/courses/30/lessons/144853)

다음은 어느 한 서점에서 판매중인 도서들의 도서 정보(BOOK) 테이블입니다.

BOOK 테이블은 각 도서의 정보를 담은 테이블로 아래와 같은 구조로 되어있습니다.

| Column name    | Type       | Nullable | Description                |   |   |   |   |   |   |
|----------------|------------|----------|----------------------------|---|---|---|---|---|---|
| BOOK_ID        | INTEGER    | FALSE    | 도서 ID                      |   |   |   |   |   |   |
| CATEGORY       | VARCHAR(N) | FALSE    | 카테고리 (경제, 인문, 소설, 생활, 기술)  |   |   |   |   |   |   |
| AUTHOR_ID      | INTEGER    | FALSE    | 저자 ID                      |   |   |   |   |   |   |
| PRICE          | INTEGER    | FALSE    | 판매가 (원)                    |   |   |   |   |   |   |
| PUBLISHED_DATE | DATE       | FALSE    | 출판일                        |   |   |   |   |   |   |

BOOK 테이블에서 2021년에 출판된 '인문' 카테고리에 속하는 도서 리스트를 찾아서 도서 ID(BOOK_ID), 출판일 (PUBLISHED_DATE)을 출력하는 SQL문을 작성해주세요.

결과는 출판일을 기준으로 오름차순 정렬해주세요.

```sql
SELECT BOOK_ID, DATE_FORMAT(PUBLISHED_DATE, '%Y-%m-%d')
FROM BOOK
WHERE YEAR(PUBLISHED_DATE) = 2021 AND CATEGORY = '인문'
ORDER BY PUBLISHED_DATE
```

- DATE_FORMAT 함수는 처음 사용해봤다. FORMAT을 이용해 날짜 표시를 디테일하게 출력할 수 있음을 확인할 것!

- WHERE 에 조건으로 2021년에 출판한 '인문' 카테코리를 출력하였다.
