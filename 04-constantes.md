# Oracle 19c
## Basic Varible 

- Open your **ORACLE SQL Developer**

- Un variable constante en un dato que no cambia.

** Hallemos el area de un circulo **
```oracle
DECLARE 
-- Constantes
    PI CONSTANT number := 3.14;
     
-- Variables
    area number;
    radio number;
BEGIN
    
    area =: PI * (radio * radio);
    dbms_output.put_line('Area ' || area || 'cm2');
END;
/
 ```

- Si ejecutamos el codigo no muestra nada por que no emos inializado el radio

- Volvemos a ejecutar y los decimales son muy largos
```oracle
DECLARE 
-- Constantes
    PI CONSTANT number := 3.14;
     
-- Variables
    area number;
    radio number;
BEGIN
    
    area =: PI * (radio * radio);
    dbms_output.put_line('Area ' ||  area  || 'cm2');
END;
/
 ```

- Redondeamos los decimales con round

```oracle
DECLARE 
-- Constantes
    PI CONSTANT number := 3.14;
     
-- Variables
    area number;
    radio number;
BEGIN
    
    area =: PI * (radio * radio);
    dbms_output.put_line('Area ' || ROUND(area, 2) || 'cm2');
END;
/
 ```