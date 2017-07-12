# Databases

## Types of databases

No SQL
* MongoDB
* CouchDB

Object relational matter ORM: Mongoose (gives good methods we can use with the data).

SQL
* Oracle
* Postgres
* SQLite
* MySQL
* AWS relational database management systems

Object relational matter ORM: Active Record (gives good methods we can use with the data).

### SQL
Database -> Tables -> Rows -> Columns

Readable.

### No SQL
Each row is an object (document).

Database -> Collections -> Documents

Efficient, scalable, flexible.

## Installing Postgres

psql (to enter PSQL).
\q (to exit PSQL).
\l (lists all the databases we have).

CREATE DATABASE blog; Creates a database

\c blog (to access blog)

Capitals are SQL methods.

Creating a table:

```
CREATE TABLE post (
   id     SERIAL NOT NULL,
   title  VARCHAR(255) NOT NULL,
   body   TEXT NOT NULL,

   PRIMARY KEY( id )
);
```

Serial: ids in number
VARCHAR(255) : limits the characters to 255
TEXT: normal text

PRIMARY KEY( id ): Unique way to ref each row.

Crud..
Create is noted as INSERT in SQL.
Read is noted as SELECT in SQL.
U
D

Query to create a row: (create)

```
INSERT INTO post ( title, body ) VALUES ( 'Post 1', 'Tinas excellent post');
```

Query to select all rows: (index)

```
SELECT * FROM post;
```

Query to select specific rows: (show)

```
SELECT * FROM post WHERE id = 1;
```

Query to select specific column and row:

```
SELECT title FROM post WHERE id = 1;
```

Query to select a column or row which contains a specific keyword:

```
SELECT * FROM post WHERE body LIKE '%Tina%';
```

Query to Update a columnn and row:

```
UPDATE post SET title='Post 2' WHERE id = 2;
```

Query to delete a row from a table:

```
DELETE FROM post WHERE id = 2;
```