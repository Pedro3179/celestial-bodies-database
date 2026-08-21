# Celestial Bodies Database

This project is a *PostgreSQL* database of *celestial bodies*. Built using *psql*, it catalogs galaxies, stars, planets and moons. It also records important attributes such as their distance from Earth, apparent magnitude, mass, type and more.

This is part of the *certification project* and one of the requirements for earning the *Relational Databases Certification*. The lab project is called "Build a Celestial Bodies Database".


---

## What I learned

1. How to use *psql*, a command-line application, to connect to *PostgreSQL* with `psql --username=user --dbname=database`
2. How to list the databases in said application with `\l`
3. How to list the relations with `\d`
4. How to check a particular table schema with `\d table_name`
5. How to connect to another database using `\c database_name`
6. How to create a database using *SQL* syntax
7. How to create a unique, auto-incrementing *primary key*
8. How to add, alter and drop columns with *SQL* syntax
9. How to add, update and drop constraints
10. How to use foreign keys to create relationships between tables
11. How to make a backup of the database schema using *pg_dump*
12. How to save the command history in *psql* with `\s file_name.txt`
13. How to restore the schema of a database from a file using the command `psql -U user < file_name.sql`

Below are the instructions to complete the project.

---

## Build a Celestial Bodies Database

For this project, you need to log in to PostgreSQL with psql to create your database. Do that by entering psql --username=freecodecamp --dbname=postgres in the terminal. Make all the tests below pass to complete the project. Be sure to get creative, and have fun!

Don't forget to connect to your database after you create it.

Here's some ideas for other column and table names: description, has_life, is_spherical, age_in_millions_of_years, planet_types, galaxy_types, distance_from_earth.

Notes:
If you leave your virtual machine, your database may not be saved. You can make a dump of it by entering `pg_dump -cC --inserts -U freecodecamp universe > universe.sql` in a bash terminal (not the psql one). It will save the commands to rebuild your database in universe.sql. The file will be located where the command was entered. If it's anything inside the project folder, the file will be saved in the VM. You can rebuild the database by entering `psql -U postgres < universe.sql` in a terminal where the .sql file is.


Complete the tasks below:

1. You should create a database named universe

2. Be sure to connect to your database with \c universe. Then, you should add tables named galaxy, star, planet, and moon

3. Each table should have a primary key

4. Each primary key should automatically increment

5. Each table should have a name column

6. You should use the INT data type for at least two columns that are not a primary or foreign key

7. You should use the NUMERIC data type at least once

8. You should use the TEXT data type at least once

9. You should use the BOOLEAN data type on at least two columns

10. Each "star" should have a foreign key that references one of the rows in galaxy

11. Each "planet" should have a foreign key that references one of the rows in star

12. Each "moon" should have a foreign key that references one of the rows in planet

13. Your database should have at least five tables

14. Each table should have at least three rows

15. The galaxy and star tables should each have at least six rows

16. The planet table should have at least 12 rows

17. The moon table should have at least 20 rows

18. Each table should have at least three columns

19. The galaxy, star, planet, and moon tables should each have at least five columns

20. At least two columns per table should not accept NULL values

21. At least one column from each table should be required to be UNIQUE

22. All columns named name should be of type VARCHAR

23. Each primary key column should follow the naming convention table_name_id. For example, the moon table should have a primary key column named moon_id

24. Each foreign key column should have the same name as the column it is referencing
