# Save

 `iniObject.save(String namefile)`

  Si función es guardar un archivos con los valores ini.
  Usa `FileWriter` por lo que tendrás que usar `try catch` al usar esta


   ```java

      INIObject i = new INIObject();
      i.put("despedida","bye");
      try{
         i.save(namefile);
      }catch(IOException e){
         System.out.print("no se puede guardar");
      }
   ```
