# Домашнее задание к занятию "Базы данных" - Варфоломеева Марьяна

### Задание 1

Опишите не менее семи таблиц, из которых состоит база данных:

- какие данные хранятся в этих таблицах;
- какой тип данных у столбцов в этих таблицах, если данные хранятся в PostgreSQL.

Приведите решение к следующему виду:

Сотрудники (

- идентификатор, первичный ключ, serial,
- фамилия varchar(50),
- ...
- идентификатор структурного подразделения, внешний ключ, integer).

---
### Ответ

 **Сотрудники** (  
- идентификатор, первичный ключ, serial,  
- фамилия varchar(50),  
- имя varchar(50),  
- отчество varchar(50),  
- Оклад money,  
- ID должности, внешний ключ, integer
- ID структурного подразделения, внешний ключ, integer  
- Дата найма date,
- ID адреса филиала, внешний ключ, integer  )  


**Должности** (  
- идентификатор, первичный ключ, serial  
- наименование должности varchar(100) )  
  
**Типы подразделений** (  
- идентификатор, первичный ключ, serial 
- наименование типа подразделения varchar(40) )  

**Структурные подразделения** (  
- идентификатор, первичный ключ, serial
- ID типа подразделения, внешний ключ, integer  
- наименование подразделения varchar(100)  )  

**Города филиалов** (  
- идентификатор, первичный ключ, serial 
- город филиала varchar(50)  )  

**Адреса филиалов** (  
- идентификатор, первичный ключ, serial   
- ID города, внешний ключ, integer  
- адрес филиала varchar(150)  )  
  
**Проекты** (  
- идентификатор, первичный ключ, serial   
- наименование проекта varchar(100) )  

**Назначения на проекты** (  
- ID сотрудника, внешний ключ, integer  
- ID проекта, внешний ключ, integer )  
