# Oracle 19c
## Basic Varible 

- Open your **ORACLE SQL Developer**
 
**FOR** 
```oracle
SET SERVEROUTPUT ON;
DECLARE  

BEGIN
    
    for i in 1..10 loop
--             dbms_output.put_line('i = ' || i );
            dbms_output.put_line(i || ' * 2 = ' || ( i * 2));
    end loop;
     
END;
/
 ```
 