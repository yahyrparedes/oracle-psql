# Oracle 19c
## Basic Varible 

- Open your **ORACLE SQL Developer**

```oracle
DECLARE 
-- define funciones y variables
    salary number; -- variable de nombre salario
    nameEmployee nvarchar2(100); -- una buena practica es poner el tamaño para no tener de tamaño
    active boolean;
    date_add date;
BEGIN
    
    nameEmployee := 'Yahyr Paredes';
    active := true;
    date_add := SYSDATE; -- '31-12-2015'
    
    dbms_output.put_line('Nombre: ' || nameEmployee );
    dbms_output.put_line('Salario: ' || salary);
    dbms_output.put_line('Activo: ' || active); -- esto genera error
END;
/
 ```

- Si ejecutamos el codigo nos genera error.
- Para imprimir boleanos debemos hacer:

```oracle
DECLARE
-- define funciones y variables
    salary number; -- variable de nombre salario
    nameEmployee nvarchar2(100); -- una buena practica es poner el tamaño para no tener de tamaño
    active boolean;
    date_add date;
BEGIN

    nameEmployee := 'Yahyr Paredes';
    active := true;
    date_add := SYSDATE; -- '31-12-2015'

    dbms_output.put_line('Nombre: ' || nameEmployee );
    dbms_output.put_line('Salario: ' || salary);
    dbms_output.put_line('Activo: ' || case when active then 'Si' else 'No'end ); -- esto genera error
END;
/
 ```

- volvemos a probar y todo ok!