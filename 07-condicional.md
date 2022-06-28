# Oracle 19c
## Basic Varible 

- Open your **ORACLE SQL Developer**
 
**IF** 
```oracle
SET SERVEROUTPUT ON;
DECLARE  
    nota number := 18;
    estado nvarchar2(100) := 'Bad';
BEGIN
--      if (nota >= 15) then
     if (nota between 17 and 20) then
         estado :='Very Good';
--      if (nota between 13 and 16) then
--          estado :='Good';
--      if (nota between 10 and 12) then
--          estado :='Bad';
--      if (nota between  0 and 9) then
--          estado :='Very Bad';
      end if;
     dbms_output.put_line('estado ' || estado );
END;
/
 ```
 