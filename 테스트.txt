-- 문제
/*
BOOK 테이블에서 2021년에 출판된 '인문' 카테고리에 속하는 도서 리스트를 찾아서 도서 ID(BOOK_ID), 출판일 (PUBLISHED_DATE)을 출력하는 SQL문을 작성해주세요.
결과는 출판일을 기준으로 오름차순 정렬해주세요.
*/

-- 답
-- 코드를 입력 하세요
SELECT BOOK_ID, TO_CHAR(PUBLISHED_DATE,'YYYY-MM-DD') PUBLISHED_DATE
  FROM BOOK
 WHERE CATEGORY = '인문'                        /* 인문에 속하고 */
   AND TO_CHAR(PUBLISHED_DATE,'YYYY') = '2021'  /* 2021년에 출판된 */         
ORDER BY 2
--ORDER BY PUBLISHED_DATE -- ASC가 없어도 그대로 출력