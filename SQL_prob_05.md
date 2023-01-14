>> ## 프로그래머스 SQL 
>> #### 1/14(토) 

***


['여러 기준으로 정렬하기'](https://school.programmers.co.kr/learn/courses/30/lessons/59404)

ANIMAL_INS 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. ANIMAL_INS 테이블 구조는 다음과 같으며, ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

동물 보호소에 들어온 모든 동물의 아이디와 이름, 보호 시작일을 이름 순으로 조회하는 SQL문을 작성해주세요. 

단, 이름이 같은 동물 중에서는 보호를 나중에 시작한 동물을 먼저 보여줘야 합니다.

***

```sql
SELECT ANIMAL_ID, NAME, DATETIME
FROM ANIMAL_INS
ORDER BY NAME, DATETIME DESC
```

***

문제에서 구하는 ANIMAL_ID, NAME, DATETIME을 출력하고, ORDER BY를 다음과 같은 순서로 출력했다.

1. NAME 순서
2. DATETIME 내림차순