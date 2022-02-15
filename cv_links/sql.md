# HW_1 (basic)
1. Вывести все поля и все строки.
```sql
select *
from students s;
```

2. Вывести всех студентов в таблице
```sql
select name
from students s;
```

3. Вывести только Id пользователей
```sql
select id
from students s;
```

4. Вывести только имя пользователей
```sql
select name
from students s;
```

5. Вывести только email пользователей
```sql
select email
from students s;
```

6. Вывести имя и email пользователей
```sql
select name, email
from students s;
```

7. Вывести id, имя, email и дату создания пользователей
```sql
select id, name, email, created_on
from students s;
```

8. Вывести пользователей где password 12333
```sql
select name
from students s
where password = '12333';
```

9. Вывести пользователей которые были созданы 2021-03-26 00:00:00
```sql
select name
from students s
where created_on = '2021-03-26 00:00:00';
```

10. Вывести пользователей где в имени есть слово Анна
```sql
select name
from students s
where name like '%Anna%';
```

11. Вывести пользователей где в имени в конце есть 8
```sql
select name
from students s 
where name like '%8';
```

12. Вывести пользователей где в имени в есть буква а
```sql
select name
from students s 
where name like '%a%';
```

13. Вывести пользователей которые были созданы 2021-07-12 00:00:00
```sql
select name
from students s 
where created_on = '2021-07-12 00:00:00';
```

14. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и имеют пароль 1m313
```sql
select name
from students s 
where created_on = '2021-07-12 00:00:00' and password = '1m313';
```

15. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть слово Andrey
```sql
select name
from students s 
where created_on = '2021-07-12 00:00:00' and name like '%Andrey%';
```

16. Вывести пользователей которые были созданы 2021-07-12 00:00:00 и у которых в имени есть цифра 8
```sql
select name
from students s 
where created_on = '2021-07-12 00:00:00' and name like '%8%';
```

17. Вывести пользователя у которых id равен 110
```sql
select name
from students s 
where id = 110;
```

18. Вывести пользователя у которых id равен 153
```sql
select name
from students s 
where id = 153;
```

19. Вывести пользователя у которых id больше 140
```sql
select name
from students s 
where id > 140;
```

20. Вывести пользователя у которых id меньше 130
```sql
select name
from students s 
where id < 130;
```

21. Вывести пользователя у которых id меньше 127 или больше 188
```sql
select name
from students s 
where id < 127 or id > 188;
```

22. Вывести пользователя у которых id меньше либо равно 137
```sql
select name
from students s 
where id <= 137;
```

23. Вывести пользователя у которых id больше либо равно 137
```sql
select name
from students s 
where id >= 137;
```

24. Вывести пользователя у которых id больше 180 но меньше 190
```sql
select name
from students s 
where id > 180 and id < 190;
```

25. Вывести пользователя у которых id между 180 и 190
```sql
select name
from students s 
where id between 180 and 190;
```

26. Вывести пользователей где password равен 12333, 1m313, 123313
```sql
select name
from students s 
where password in ('12333', '1m313', '123313');
```

27. Вывести пользователей где created_on равен 2020-10-03 00:00:00, 2021-05-19 00:00:00, 2021-03-26 00:00:00
```sql
select name
from students s 
where created_on in ('2020-10-03 00:00:00', '2021-05-19 00:00:00', '2021-03-26 00:00:00');
```

28. Вывести минимальный id 
```sql
select min(id)
from students s;
```

29. Вывести максимальный.
```sql
select max(id)
from students s;
```

30. Вывести количество пользователей
```sql
select count(name)
from students s;
```

31. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку возрастания даты добавления пользоватлеля.
```sql
select id, name, created_on
from students s 
order by created_on;
```

32. Вывести id пользователя, имя, дату создания пользователя. Отсортировать по порядку убывания даты добавления пользоватлеля.
```sql
select id, name, created_on
from students s 
order by 3 desc;
```
# HW_2 (DDL operations)
1. Создать таблицу employees
	- id. serial,  primary key,
	- employee_name. Varchar(50), not null
```sql
create table employees(
	id serial primary key,
	employee_name varchar(50) not null
);
```
2. Наполнить таблицу employee 70 строками
```sql
insert into employees(employee_name)
values ('James Gandolfini'),
	('Edie Falco'),
	('Michael Imperioli'),
	('Steve Van Zandt'),
	('Robert Iler'),
	('Tony Sirico'),
	('Jamie-Lynn Sigler'),
	('Lorraine Bracco'),
	('Dominic Chianese'),
	('Aida Turturro'),
	('Steve Schirripa'),
	('Drea de Matteo'),
	('Dan Grimaldi'),
	('Joseph R. Gannascoli'),
	('Sharon Angela'),
	('John Ventimiglia'),
	('Vincent Curatola'),
	('Frank Vincent'),
	('Federico Castelluccio'),
	('Jerry Adler'),
	('Arthur J. Nascarella'),
	('Max Casella'),
	('Maureen Van Zandt'),
	('Vincent Pastore'),
	('Robert Funaro'),
	('Carl Capotorto'),
	('Matt Servitto'),
	('Tom Aldredge'),
	('Nancy Marchand'),
	('Joe Pantoliano'),
	('Suzanne Shepherd'),
	('Kathrine Narducci'),
	('Angelo Massagli'),
	('Denise Borino-Quinn'),
	('Ray Abruzzo'),
	('George Loros'),
	('Tony Darrow'),
	('Steve Buscemi'),
	('Peter Bogdanovich'),
	('Will Janowitz'),
	('Richard Portnow'),
	('Oksana Lada'),
	('Paul Schulze'),
	('John Fiore'),
	('Frank Santorelli'),
	('John Ciarcia'),
	('Miryam Coppersmith'),
	('Jeffrey M. Marchetti'),
	('Jason Cerbone'),
	('Frank Pando'),
	('Toni Kalem'),
	('Frank Pellegrino'),
	('Tony Lip'),
	('Anthony J. Ribustello'),
	('Joe Pucillo'),
	('David Proval'),
	('Al Sapienza'),
	('Karen Young'),
	('Richard Maldone'),
	('John Bianco'),
	('Danielle Di Vecchio'),
	('Ed Vassallo'),
	('Louis Lombardi'),
	('Greg Antonacci'),
	('Lenny Venito'),
	('Annika Pergament'),
	('Marianne Leone'),
	('Chris Caldovino'),
	('Dan Castleman'),
	('Joseph Badalucco Jr.');
```
3. Создать таблицу salary
	- id. Serial  primary key,
	- monthly_salary. Int, not null
```sql
create table salary(
	id serial primary key,
	monthly_salary int not null
);
```
4. Наполнить таблицу salary 15 строками
```sql
insert into salary(monthly_salary)
values (1000),
	(1100),
	(1200),
	(1300),
	(1400),
	(1500),
	(1600),
	(1700),
	(1800),
	(1900),
	(2000),
	(2100),
	(2200),
	(2300),
	(2400),
	(2500);
```
5. Создать таблицу employee_salary
	- id. Serial  primary key,
	- employee_id. Int, not null, unique
	- salary_id. Int, not null
```sql
create table employee_salary(
	id serial primary key,
	employee_id int not null unique,
	salary_id int not null
);
```
6. Наполнить таблицу employee_salary 40 строками:
	- в 10 строк из 40 вставить несуществующие employee_id
```sql
insert into employee_salary(employee_id, salary_id)
values (1, 1),
	(2, 2),
	(3, 3),
	(4, 4),
	(5, 5),
	(6, 6),
	(7, 7),
	(8, 8),
	(9, 9),
	(10, 10),
	(11, 11),
	(12, 12),
	(13, 13),
	(14, 14),
	(15, 15),
	(16, 16),
	(17, 1),
	(18, 2),
	(19, 3),
	(20, 4),
	(21, 5),
	(22, 6),
	(23, 7),
	(24, 8),
	(25, 9),
	(26, 10),
	(27, 11),
	(28, 12),
	(29, 13),
	(30, 14),
	(311, 15),
	(322, 16),
	(333, 1),
	(344, 2),
	(355, 3),
	(366, 4),
	(377, 5),
	(388, 6),
	(399, 7),
	(400, 8);
```
7. Создать таблицу roles
	- id. Serial  primary key,
	- role_name. int, not null, unique
```sql
create table roles(
	id serial primary key,
	role_name int not null unique
);
```
8. Поменять тип столба role_name с int на varchar(30)
```sql
ALTER TABLE roles ALTER COLUMN role_name TYPE varchar(30);
```
9. Наполнить таблицу roles 20 строками
```sql
insert into roles(role_name)
values ('Junior Python developer'),
	('Middle Python developer'),
	('Senior Python developer'),
	('Junior Java developer'),
	('Middle Java developer'),
	('Senior Java developer'),
	('Junior JavaScript developer'),
	('Middle JavaScript developer'),
	('Senior JavaScript developer'),
	('Junior Manual QA engineer'),
	('Middle Manual QA engineer'),
	('Senior Manual QA engineer'),
	('Project Manager'),
	('Designer'),
	('HR'),
	('CEO'),
	('Sales manager'),
	('Junior Automation QA engineer'),
	('Middle Automation QA engineer'),
	('Senior Automation QA engineer');
```
10. Создать таблицу roles_employee
	- id. Serial  primary key,
	- employee_id. Int, not null, unique (внешний ключ для таблицы employees, поле id)
	- role_id. Int, not null (внешний ключ для таблицы roles, поле id)*/
```sql
create table roles_employee(
	id serial primary key,
	employee_id int not null unique,
	role_id int not null,
	foreign key (employee_id) 
		references employees(id),
	foreign key (role_id)
		references roles(id)
);
```
11. Наполнить таблицу roles_employee 40 строками
```sql
insert into roles_employee(employee_id, role_id)
values (1, 1),
	(2, 2),
	(3, 3),
	(4, 4),
	(5, 5),
	(6, 6),
	(7, 7),
	(8, 8),
	(9, 9),
	(10, 10),
	(11, 11),
	(12, 12),
	(13, 13),
	(14, 14),
	(15, 15),
	(16, 16),
	(17, 17),
	(18, 18),
	(19, 19),
	(20, 20),
	(21, 1),
	(22, 2),
	(23, 3),
	(24, 4),
	(25, 5),
	(26, 6),
	(27, 7),
	(28, 8),
	(29, 9),
	(30, 10),
	(31, 11),
	(32, 12),
	(33, 13),
	(34, 14),
	(35, 15),
	(36, 16),
	(37, 17),
	(38, 18),
	(39, 19),
	(40, 20);
```

# HW_3 (JOIN operations)
1. Вывести всех работников чьи зарплаты есть в базе, вместе с зарплатами.
```sql
select employee_name, monthly_salary 
from employees e join employee_salary es 
on e.id = es.employee_id 
join salary s 
on es.salary_id = s.id;
```
2. Вывести всех работников у которых ЗП меньше 2000.
```sql
select employee_name, monthly_salary
from employees e join employee_salary es 
on e.id = es.employee_id 
join salary s 
on es.salary_id = s.id 
where monthly_salary < 2000;
```
3. Вывести все зарплатные позиции, но работник по ним не назначен. (ЗП есть, но не понятно кто её получает.)
```sql
select employee_name, monthly_salary 
from employees e right join employee_salary es
on e.id = es.employee_id
join salary s 
on es.salary_id = s.id
where employee_name is null;
```
4. Вывести все зарплатные позиции  меньше 2000 но работник по ним не назначен. (ЗП есть, но не понятно кто её получает.)
```sql
select employee_name, monthly_salary
from employees e right join employee_salary es
on e.id = es.employee_id 
join salary s 
on es.salary_id = s.id 
where employee_name is null and monthly_salary < 2000;
```

5. Найти всех работников кому не начислена ЗП.
```sql
select employee_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
left join salary s 
on es.salary_id = s.id 
where monthly_salary is null;
```

6. Вывести всех работников с названиями их должности.
```sql
select employee_name, role_name
from employees e left join roles_employee re 
on e.id = re.employee_id 
left join roles r
on re.role_id = r.id;
```

7. Вывести имена и должность только Java разработчиков.
```sql
select employee_name, role_name
from employees e join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id 
where lower(role_name) like '% java %';
```

8. Вывести имена и должность только Python разработчиков.
```sql
select employee_name, role_name
from employees e join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id 
where lower(role_name) like '% python %';
```

9. Вывести имена и должность всех QA инженеров.
```sql
select employee_name, role_name
from employees e join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id 
where lower(role_name) like '% qa %';
```

10. Вывести имена и должность ручных QA инженеров.
```sql
select employee_name, role_name
from employees e join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id 
where lower(role_name) like '% qa %' and lower(role_name) like '% manual %';
```

11. Вывести имена и должность автоматизаторов QA
```sql
select employee_name, role_name
from employees e join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id 
where lower(role_name) like '% qa %' and lower(role_name) like '% auto%';
```

12. Вывести имена и зарплаты Junior специалистов
```sql
select employee_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
left join salary s
on es.salary_id = s.id 
left join roles_employee re 
on e.id = re.employee_id 
left join roles r
on re.role_id = r.id 
where lower(role_name) like 'junior %';
```

13. Вывести имена и зарплаты Middle специалистов
```sql
select employee_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
left join salary s
on es.salary_id = s.id 
left join roles_employee re 
on e.id = re.employee_id 
left join roles r
on re.role_id = r.id 
where lower(role_name) like 'middle %';
```

14. Вывести имена и зарплаты Senior специалистов
```sql
select employee_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
left join salary s
on es.salary_id = s.id 
left join roles_employee re 
on e.id = re.employee_id 
left join roles r
on re.role_id = r.id 
where lower(role_name) like 's %';
```

15. Вывести зарплаты Java разработчиков
```sql
select monthly_salary, role_name
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '% java %';
```

16. Вывести зарплаты Python разработчиков
```sql
select monthly_salary, role_name
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '% python %';
```

17. Вывести имена и зарплаты Junior Python разработчиков
```sql
select employee_name, monthly_salary
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%junior python%';
```

18. Вывести имена и зарплаты Middle JS разработчиков
```sql
select employee_name, monthly_salary
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%middle javascript%';
```

19. Вывести имена и зарплаты Senior Java разработчиков
```sql
select employee_name, monthly_salary
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%senior java%';
```

20. Вывести зарплаты Junior QA инженеров
```sql
select monthly_salary
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%junior%' and lower(role_name) like'%qa%';
```

21. Вывести среднюю зарплату всех Junior специалистов
```sql
select round(avg(monthly_salary), 2) as average_junior_salary
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%junior%';
```

22. Вывести сумму зарплат JS разработчиков
```sql
select sum(monthly_salary)
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%javascript%';
```

23. Вывести минимальную ЗП QA инженеров
```sql
select min(monthly_salary)
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%qa%';
```

24. Вывести максимальную ЗП QA инженеров
```sql
select max(monthly_salary)
from salary s join employee_salary es 
on s.id = es.salary_id 
join employees e 
on es.employee_id = e.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r 
on re.role_id = r.id
where lower(role_name) like '%qa%';
```

25. Вывести количество QA инженеров
```sql
select count(role_name)
from salary s join employee_salary es 
on s.id = es.salary_id 
full join employees e 
on es.employee_id = e.id 
full join roles_employee re 
on e.id = re.employee_id 
full join roles r 
on re.role_id = r.id
where lower(role_name) like '%qa%';
```

26. Вывести количество Middle специалистов.
```sql
select count(role_name)
from salary s join employee_salary es 
on s.id = es.salary_id 
full join employees e 
on es.employee_id = e.id 
full join roles_employee re 
on e.id = re.employee_id 
full join roles r 
on re.role_id = r.id
where lower(role_name) like '%middle%';
```

27. Вывести количество разработчиков
```sql
select count(role_name)
from salary s join employee_salary es 
on s.id = es.salary_id 
full join employees e 
on es.employee_id = e.id 
full join roles_employee re 
on e.id = re.employee_id 
full join roles r 
on re.role_id = r.id
where lower(role_name) like '%dev%';
```

28. Вывести фонд (сумму) зарплаты разработчиков.
```sql
select sum(monthly_salary)
from salary s join employee_salary es 
on s.id = es.salary_id 
full join employees e 
on es.employee_id = e.id 
full join roles_employee re 
on e.id = re.employee_id 
full join roles r 
on re.role_id = r.id
where lower(role_name) like '%dev%';
```

29. Вывести имена, должности и ЗП всех специалистов по возрастанию
```sql
select employee_name, role_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
left join salary s
on es.salary_id = s.id 
left join roles_employee re 
on e.id = re.employee_id 
left join roles r
on re.role_id = r.id
order by 3;
```

30. Вывести имена, должности и ЗП всех специалистов по возрастанию у специалистов у которых ЗП от 1700 до 2300
```sql
select employee_name, role_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
join salary s
on es.salary_id = s.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id
where monthly_salary >= 1700 and monthly_salary < 2300
order by 3;
```

31. Вывести имена, должности и ЗП всех специалистов по возрастанию у специалистов у которых ЗП меньше 2300
```sql
select employee_name, role_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
join salary s
on es.salary_id = s.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id
where monthly_salary >= 1700 and monthly_salary < 2300
order by 3;
```

32. Вывести имена, должности и ЗП всех специалистов по возрастанию у специалистов у которых ЗП равна 1100, 1500, 2000
```sql
select employee_name, role_name, monthly_salary
from employees e left join employee_salary es 
on e.id = es.employee_id 
join salary s
on es.salary_id = s.id 
join roles_employee re 
on e.id = re.employee_id 
join roles r
on re.role_id = r.id
where monthly_salary in (1100, 1500, 2000)
order by 3;
```