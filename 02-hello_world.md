# Oracle 19c
## Hello World!! 

- Open your **ORACLE SQL Developer**

```oracle
DECLARE
-- define funciones y variables

BEGIN
    dbms_output.put_line('Hello World..');
END;
/
 ```

- Execute your sentence.
- Ejecutamos y nos dice que ejecuto de manera satisfactorio pero no muestra nuestro mensaje para esto lo que debemos hacer es habilitar el output.

```oracle
SET SERVEROUTPUT ON;
DECLARE 
-- definicio de funciones y variable

BEGIN
    dbms_output.put_line('Hello World..');
END;
/
 ```

- Ahora en la consola podremos ver nuestro
```shell
Hello World..
 ```