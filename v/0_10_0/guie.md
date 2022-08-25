# Guíe 0.10.0

## Funciones

   [INIObject.get](/v/0_10_0/INIObject_get.md)

   [INIObject.put](/)

   [INIObjec.save](/)

## Instancear 

   ```java
    INIObject io = new INIObject();
    INIObject iniObject = new INIObject(" STRING INI ");
   ```
Al acceder a string que no sea `INI` Lanzará INIException

   ```java
     try{
       INIObject iniObject = new INIObject("no es ini");
     }catch(INIException e){
        System.out.print(e.getMessage);
     }
   ```

   Para acceder a los valores se usa [get](/v/0_10_0/INIObject_get.md)

   ```java
      iniObject.get("name"); // return Objetos

      iniObject.getString("name"); // return String

      iniObject.getBoolean("name"); // return boolean

      iniObject.getFloat("name"); // return float

      iniObject.getInt("name"); // return int 

      iniObject.getDouble("name"); // return double
   ```

 de no existir el objetos que busca lanzara la una excepción
     
   ```java

        INIObject i = new INIObject();
        i.get("day"); // INIException
   ```

 Para añadir nuevos. Valores se usa [put](/)

   ```java

       iniObject.put("Saludo","Hola cómo estás");

   ```

La función [save](/) sirve para guardar los objetos en un archivo.ini
A cualquier error Lanzará IOException

   ```java

      try{
          iniObject.save("file.ini");
      }catch(IOException e){
          // Error code
      }
   ```
