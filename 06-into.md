# Oracle 19c
## Basic Varible 

- Open your **ORACLE SQL Developer**
 
**INTO** ONE VALUE
```oracle
SET SERVEROUTPUT ON;
DECLARE  
    cantidad number;
    usuario nvarchar2(100);
BEGIN
    select user into usuario from dual;
    dbms_output.put_line('Usuario' || usuario );

    select count(*) into cantidad from dual;
    dbms_output.put_line('Cantindad' || cantidad );    
END;
/
 ```

**INTO** MULTIPLE VALUES
```oracle
SET SERVEROUTPUT ON;
DECLARE  
    cantidad number;
    usuario nvarchar2(100);
BEGIN
    select user, COUNT(*) into usuario,cantidad from dual;
    dbms_output.put_line('Usuario' || usuario ); 
    dbms_output.put_line('Cantindad' || cantidad );    
END;
/
 ```