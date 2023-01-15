>> ## 프로그래머스 SQL 
>> #### 1/15(일) 

***


['동물의 아이디와 이름'](https://school.programmers.co.kr/learn/courses/30/lessons/59403)

ANIMAL_INS 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. 

ANIMAL_INS 테이블 구조는 다음과 같으며, ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

동물 보호소에 들어온 모든 동물의 아이디와 이름을 ANIMAL_ID순으로 조회하는 SQL문을 작성해주세요

***

```sql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
ORDER BY ANIMAL_ID
```

***

ANIMAL_ID와 NAME을 출력하였다. 
이 때 ORDER BY 로 ANIMAL_ID 순으로 나오게끔 하였다.