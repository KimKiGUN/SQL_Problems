>> ## 프로그래머스 SQL 
>> #### 1/13(금) 

***


['어린 동물 찾기'](https://school.programmers.co.kr/learn/courses/30/lessons/59037)

ANIMAL_INS 테이블은 동물 보호소에 들어온 동물의 정보를 담은 테이블입니다. ANIMAL_INS 테이블 구조는 다음과 같으며, ANIMAL_ID, ANIMAL_TYPE, DATETIME, INTAKE_CONDITION, NAME, SEX_UPON_INTAKE는 각각 동물의 아이디, 생물 종, 보호 시작일, 보호 시작 시 상태, 이름, 성별 및 중성화 여부를 나타냅니다.

동물 보호소에 들어온 동물 중 **젊은 동물** 의 아이디와 이름을 조회하는 SQL 문을 작성해주세요. 이때 결과는 아이디 순으로 조회해주세요.

**젊은동물은 INTAKE_CONDITION이 Aged가 아닌 경우를 뜻함**

```sql
SELECT ANIMAL_ID, NAME
FROM ANIMAL_INS
WHERE INTAKE_CONDITION != 'Aged'
```

***

- 문제에서 나온대로 INTAKE_CONDITION 이 'Aged' 가 아닌 동물만 출력했다.