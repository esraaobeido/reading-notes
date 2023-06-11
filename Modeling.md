# Data Modeling
## SQL and NoSQL
**1. What type of database is the best fit for the complex query intensive environment?** <br>SQL DataBase.

**2. What type of database is the best fit for hierarchical data storage?**
<br> NoSQL DataBase

**3. Describe the differences in scalability between a SQl and NoSQL database as though you were speaking to a non-technical friend.**

An SQL database is like a library with categorized sections and labeled shelves. Each book has a specific place based on its category, making it easy to find and organize. However, if you need more space for books in a particular category, you may have to rearrange the shelves or add more shelves to that specific section, which can be time consuming.
On the other side, a NoSQL database is like a library where you can put books wherever there's an empty space. If you have more books to add, you can simply find an empty spot and place them there. its more flexible than SQL.

## sql modeling techniques
**1. Among data tables, what is a one-to-many relationship and how do we “relate” them?**
<br>
In a one-to-one relationship, one record in a table is associated with one and only one record in another table.

**2.Prior to designing your relational database, it might be useful to ___ a ___ of the database tables and their relationships.**
<br>
create a diagram

**3. Explain the difference between a primary and foreign key**
A primary key uniquely identifies a row in a table, while a foreign key is used to link two tables together by referencing the primary key of the related table. The most important difference that you should note here is that a primary key cannot have a NULL value, whereas a foreign key can accept NULL values.

## sql vs nosql

**1. How do we treat keywords and parameters differently in SQL syntax?**

keywords are predefined words with fixed meanings in SQL that define the operations of queries, examples of SQL keywords include SELECT, INSERT, UPDATE, DELETE, WHERE, JOIN, and ORDER BY. 
<br>
Parameters, on the other hand, act as placeholders for dynamic values and are used to provide flexibility when executing SQL statements.

**2. Define normalization within the context of schemas and data.**
Normalization is the process of organizing data in a database. This includes creating tables and establishing relationships between those tables according to rules designed both to protect the data and to make the database more flexible by eliminating redundancy and inconsistent dependency.

**3. Explain the difference between one-to-one, one-to-many, and many-to-many relationships to a non-technical recruiter.**
- A one-to-one relationship is like having a unique identification number for each person. Imagine where each employee in a company has a specific employee ID assigned to them.
- A one-to-many relationship is like a teacher and students in a classroom. Think of a teacher who has multiple students in their class. Each student belongs to only one teacher, but a teacher can have several students.
- A many-to-many relationship is like actors and movies. Consider a scenario where actors can be a part of multiple movies, and each movie can have multiple actors.

## Reflection
**What are your learning goals after reading and reviewing the class README?** <br>
I'm seeking to improve my understanding of data modeling, which will enable me to work effectively with and manipulate data in JavaScript applications.