Создать базу данных по скрипту в два варианта:

1)

1.1) create database demo_database_crud;

1.2) установить в файле application.properties следующее свойство на create!!!
spring.jpa.hibernate.ddl-auto=create

или

2)

2.1) create database demo_database_crud;
     use mem;
     create table employee (
         employeeId bigint AUTO_INCREMENT PRIMARY KEY,
         employeeName varchar(255),
         employeeRole varchar(255)
         );

2.2) установить в файле application.properties следующее свойство на update!!!
spring.jpa.hibernate.ddl-auto=update


3) Установить в файле поля username имя и password пользователя базы данных
(обычно это имя учетки админа и пароль админа)

   spring.datasource.url=jdbc:mysql://localhost/demo_database_crud?useUnicode=true&useJDBCCompliantTimezoneShift=true&useLegacyDatetimeCode=false&serverTimezone=UTC
   spring.datasource.username=********
   spring.datasource.password=********\

Если нужна другая БД, то demo_database_crud везде заменить!!!