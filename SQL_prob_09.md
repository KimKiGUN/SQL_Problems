>> ## 프로그래머스 SQL 
>> #### 1/15(일) 

***


['나이 정보가 없는 회원 수 구하기'](https://school.programmers.co.kr/learn/courses/30/lessons/131528)

다음은 어느 의류 쇼핑몰에 가입한 회원 정보를 담은 USER_INFO 테이블입니다. 

USER_INFO 테이블은 아래와 같은 구조로 되어있으며, USER_ID, GENDER, AGE, JOINED는 각각 회원 ID, 성별, 나이, 가입일을 나타냅니다.

GENDER 컬럼은 비어있거나 0 또는 1의 값을 가지며 0인 경우 남자를, 1인 경우는 여자를 나타냅니다.

USER_INFO 테이블에서 나이 정보가 없는 회원이 몇 명인지 출력하는 SQL문을 작성해주세요. 이때 컬럼명은 USERS로 지정해주세요.

***

```sql
SELECT COUNT(AGE IS NULL) AS USER_INFO
FROM USER_INFO
WHERE AGE IS NULL
```

***

COUNT 함수를 이용하여 AGE가 NULL 인 경우를 출력하였다.
이때 컬럼의 별칭을 'USER_INFO'로 지정하여 출력하였다.