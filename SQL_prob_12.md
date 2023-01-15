>> ## 프로그래머스 SQL 
>> #### 1/16(월) 

***


['조건에 맞는 회원수 구하기'](https://school.programmers.co.kr/learn/courses/30/lessons/131535)

다음은 어느 의류 쇼핑몰에 가입한 회원 정보를 담은 USER_INFO 테이블입니다. 

USER_INFO 테이블은 아래와 같은 구조로 되어있으며 USER_ID, GENDER, AGE, JOINED는 각각 회원 ID, 성별, 나이, 가입일을 나타냅니다.

GENDER 컬럼은 비어있거나 0 또는 1의 값을 가지며 0인 경우 남자를, 1인 경우는 여자를 나타냅니다.

USER_INFO 테이블에서 2021년에 가입한 회원 중 나이가 20세 이상 29세 이하인 회원이 몇 명인지 출력하는 SQL문을 작성해주세요.

***

```sql
SELECT COUNT(USER_ID) AS USERS
FROM USER_INFO
WHERE AGE >= 20 AND AGE <= 29 AND YEAR(JOINED) = 2021
```

***

- WHERE 에 AGE가 20~29, YEAR함수를 통해 JOINED 의 해가 2021년인 고객을 출력하고 COUNT를 이용해 총 인원을 계산하였다.
