# Домашнее задание к занятию "Работа с данными (DDL/DML)" - `Корнилов Арсений`
---
### Задание 1.
#### 1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
sudo apt install mysql-server

#### 1.2. Создайте учётную запись sys_temp.
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY '12345';


#### 1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)
<img width="525" height="242" alt="image" src="https://github.com/user-attachments/assets/0b89d6d9-7afa-4bef-ab91-3432261ec29e" />


#### 1.4. Дайте все права для пользователя sys_temp.
RANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost' WITH GRANT OPTION;FLUSH PRIVILEGES;


#### 1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
Использовал SHOW GRANTS FOR 'sys_temp'@'localhost';
<img width="1302" height="575" alt="image" src="https://github.com/user-attachments/assets/a606b8de-432b-4471-b406-97dba62b7778" />


#### 1.6. Переподключитесь к базе данных от имени sys_temp.
mysql -u sys_temp -p


1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.
wget https://downloads.mysql.com/docs/sakila-db.zip
unzip sakila-db.zip


1.7. Восстановите дамп в базу данных.
mysql -u sys_temp -p sakila < sakila-db/sakila-schema.sql
mysql -u sys_temp -p sakila < sakila-db/sakila-data.sql


1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
Использовал SHOW TABLES;
<img width="571" height="401" alt="image" src="https://github.com/user-attachments/assets/792070ed-39b9-4fff-92b1-809f4574e03f" />
<img width="461" height="373" alt="image" src="https://github.com/user-attachments/assets/31102987-3c8d-45eb-ba11-5251b155c26a" />


### Задание 2.
