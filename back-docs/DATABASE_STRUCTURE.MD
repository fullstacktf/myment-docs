# Database

#### What is it?

Is an organized collection of structured information, or data, typically stored electronically in a computer system.

In this case (Myment web app), the database will be controlled by a relational database management system (RDBMS). Together, the data and the RDBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database.

Data within the most common types of databases in operation today is typically modeled in rows and columns in a series of tables to make processing and data querying efficient. The data can then be easily accessed, managed, modified, updated, controlled, and organized.

# Technologies that we will use in the Myment Travel web app database:

- [MariaDB](https://mariadb.com/kb/en/): open-source fork of the MySQL relational database management system (RDBMS) that use structured query language (SQL) for writing and querying data.

- [Sequelize](https://sequelize.org/): Javascript library that makes it easy to manage a SQL database and implements the ORM technique (wich allows us to write queries, using the object-oriented paradigm of our preferred programming language). In other words, we will interact with our database using our language of choice instead of SQL.

# Database structure

The Myment Travel web app has an internal structure that needs to be understood in order to make a clear and logical front-end.

1. We will use Sequelize as an ORM.
2. MariaDB as a database management system.
3. 