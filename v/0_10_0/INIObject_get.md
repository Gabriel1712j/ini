# GET

`iniObject.get(key);`

## Code

   ```java
      iniObject.get(key); retorno Objeto
   ```

## GUIE

Si colocar get retornará un objeto y puedes revisar si es número o string por tu cuenta
Pero para especificar tipo de datos puedes usar estás otras funciones

   ```java

      iniObject.getString(key); // retorna string

      iniObject.getBoolean(key); // retorna boolean, si no es boolean lanza exception

      iniObject.getInt(key); // retorna Entero, si no es entero lanza excepción 

      iniObject.getFloat(key); // retorna float, si no es float lanza exception 

      iniObject.getDouble(key); // retorna double, si no es double Lanzará exception  

      iniObject.getINIObject(key); // retorna INIObject, si no es ini lanza exception
   ```
### getINIObject
Es cuando una llave es un objetoINI
> EJEMPLO DE CODIGO INI

   ```
      hello = hola
      Bye = adiós
      Bye.Boolean = False
   ```

En este código la key bye es un objeto ini por lo que se puede heredar de get

    
### Ejemplo

   ```java
      INIObject io = new INIObject();
      io.put("hello","hello world");
      io.getInt("hello"); // The Key 'hello' IS NOT A INTEGER
   ```
   ```java
      String INI = "hello = hola\nbye=adios\nbye.boolean=False"
      INIObject io = new INIObject(INI);
      io.get("hello"); // retorna "hola"
      Object obj = io.get("bye"); // retorna INIObject
      INIObject bye = (INIObject)obj;
      bye.get(); // retorna "adiós"
      bye.get("boolean"); // retorna false
   ```
