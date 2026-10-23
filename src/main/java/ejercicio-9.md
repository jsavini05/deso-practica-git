Para probar el ejercicio 9, se copia en main.java lo siguiente:

```java
     import exception.DataAccessException;
     import repository.dao.FileUserDao;
     import repository.dao.FileUserDaoImpl;
     public class Main {
      public static void main(String[] args) {
        FileUserDao dao = new FileUserDaoImpl();
        try {
          dao.findAll().forEach(u -> System.out.println(u.getId() + " " + u.getUsername()));
        } catch (DataAccessException e) {
          e.printStackTrace();
        }
      }
    }
```
