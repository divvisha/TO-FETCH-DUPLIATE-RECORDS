# EXP 05 - CREATE A SQL PROGRAM TO FETCH THE DUPLICATE RECORD.

## AIM:

To fetch the duplicate records existing in the table using SQL.

## ALGORITHM:

1) Create a sample table in SQL using CREATE TABLE syntax
2) Insert all the values and Titles respectively using INSERT INTO syntax
3) Now check whether all the rows are affected or not by fetching the table
4) After checking, now use SELECT for choosing the column name that we want and use FROM to choose the table
5) Then use GROUP BY syntax to group the column containing duplicates and count them to display by using COUNT.
6) After compiling and running the program, the results will be displayed.

## PROGRAM:
```java
create table Zoo(
  Sno int,
  Animal varchar(50),
  No_of_animals int
);
insert into Zoo (Sno,Animal,No_of_animals)
values (1,'Leopard',5);
insert into Zoo (Sno,Animal,No_of_animals)
values (2,'Turtle',10);
insert into Zoo (Sno,Animal,No_of_animals)
values (3,'Elephant',15);
insert into Zoo (Sno,Animal,No_of_animals)
values (4,'Cheetah',3);
insert into Zoo (Sno,Animal,No_of_animals)
values (5,'Tiger',5);
insert into Zoo (Sno,Animal,No_of_animals)
values (6,'Otter',7);
insert into Zoo (Sno,Animal,No_of_animals)
values (7,'Giraffe',4);
insert into Zoo (Sno,Animal,No_of_animals)
values (8,'Crocodile',6);
insert into Zoo (Sno,Animal,No_of_animals)
values (9,'Koala',7);
insert into Zoo (Sno,Animal,No_of_animals)
values (10,'White tiger',3);

select No_of_animals as noa, count(No_of_animals) as count
from Zoo
group by No_of_animals
having count(No_of_animals)> 1;
```

## OUTPUT:

<img width="367" alt="dbms e5 op" src="https://github.com/divvisha/TO-FETCH-DUPLIATE-RECORDS/assets/127508123/856a40b0-c98e-410e-aa2c-11ceb8d7ca39">

## RESULT:

Thus we have successfully obtained the required result using the above-given code.
