>> ## 프로그래머스 SQL 
>> #### 1/16(월) 

***


['12세 이하인 여자 환자 목록 출력하기'](https://school.programmers.co.kr/learn/courses/30/lessons/132201)

다음은 종합병원에 등록된 환자정보를 담은 PATIENT 테이블입니다. PATIENT 테이블은 다음과 같으며 PT_NO, PT_NAME, GEND_CD, AGE, TLNO는 각각 환자번호, 환자이름, 성별코드, 나이, 전화번호를 의미합니다.

PATIENT 테이블에서 12세 이하인 여자환자의 환자이름, 환자번호, 성별코드, 나이, 전화번호를 조회하는 SQL문을 작성해주세요. 

이때 전화번호가 없는 경우, 'NONE'으로 출력시켜 주시고 결과는 나이를 기준으로 내림차순 정렬하고, 나이 같다면 환자이름을 기준으로 오름차순 정렬해주세요.

***

```sql
SELECT PT_NAME, PT_NO, GEND_CD, AGE, IFNULL(TLNO, 'NONE')
FROM PATIENT
WHERE AGE<=12 AND GEND_CD = 'W'
ORDER BY AGE DESC, PT_NAME
```

- PT_NAME, PT_NO, GEND_CD, AGE를 출력하고, TLNO는 IFNULL을 통해서 값이 없을 경우 'NONE'로 출력하였다.

- WHERE 조건을 주어 AGE가 12이하이고 성별이 'W'인 자료만 출력하였다.