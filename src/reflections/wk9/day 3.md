# In a SQL table, what is the difference between information in a row and information in a column?
>the information in a row is an individiual object with all of its properties where a column is the specific property for all of the objects in the table.
# Demonstrate the basic structure for creating a new table called characters with the values name, age, description as strings, and an int id.
> CREATE TABLE characters(
  id int NOT NULL,
  name VARCHAR(255),
  age int NOT NULL,
  description VARCHAR(255)
);
# What is the difference between the following statements:
# DELETE FROM table_name;
# DROP TABLE table_name;
>The drop table command deletes the table in its entirety while the delete from command deletes only what you specifically set what needs to be deleted.

lab link: https://github.com/hannahhayward/Knights