예시   
SELECT   
	item.id,   
    item.name,   
    stock.item_id,   
    stock.inventory_count   
FROM item RIGHT OUTER JOIN stock   
ON item.id = stock.item_id   


레프트, 라이트는 기준이 되는 파일을 정해준다.   
LEFT로 하면 item table이 기준이되고   
RIGHT로 하면 stock table이 기준이 되는데   
기준이 되는 테이블에 없는 정보는 표로 불러올때 사라지거나   
기준이 되는 테이블에 있는 정보가 반대편 테이블에 없는경우 null값을 출력된다   
LEFT OUTER JOIN   

RIGHT OUTER JOIN   

- 연산   
교집합
SELECT * FROM member_A 
**INTERSECT **
SELECT * FROM member_B

차집합
SELECT * FROM member_A 
**MINUS**
SELECT * FROM member_B

합집합
SELECT * FROM member_A
**UNION**
SELECT * FROM member_B
