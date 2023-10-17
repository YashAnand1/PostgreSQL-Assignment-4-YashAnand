<div align="center">


<!-- add technical charcha logo postgres session 3 -->
# PostgresSQL Session 4        
### — Task Documentation by Yash Anand —    

_____________________________________________________________________________________                        

## Contents
</div>


  - [**Overview**](#overview)
  - [**Prerequisites**](#prerequisites)
  - [**Task 1: Create Roles**](#task-1-create-roles)
     - [**1.1. Creating Three Roles**](#11-creating-three-roles)
     - [**1.2. Assigning Passwords**](#12-assigning-passwords)
  - [**Conclusion**](#conclusion)
 
_____________________________________________________________________________________      
<div align="center">
   
# **Overview** 
</div>

While the first three Technical Charcha Sessions on PostgreSQL were about helped the participants better understand querying of data, the fourth session helped us learn more about administration under PostgreSQL.

As per the fourth PostgreSQL Assignment that was assigned by Mr. Vinay Panwar, we  

As a part of the third Technical Charcha session on PostgreSQL, the attendees were given an assignment comprising of 4 tasks to help gauge their understanding of PostgreSQL. This document serves as a documentation of these 4 tasks which involve the following:
- The creation of database, schemas, tables
- The querying of the created data

These completed tasks have been compiled into this single document with practical demonstrations. Through this document, one can aim to better understand how to <u>form relationships between data</u>, as it can be understood as the main theme of the assignment itself. 

For the completition of the majority of the assigned tasks, I referenced [this PostgreSQL tutorial](https://www.w3schools.com/postgresql/postgresql_intro.php) by W3School along with Prescott Computer Guy's YouTube tutorial on the same, which has been provided below:

<div align="center">     

[![IMAGE_ALT](https://img.youtube.com/vi/NvrpuBAMddw/maxresdefault.jpg)](https://www.youtube.com/watch?v=NvrpuBAMddw)
   </div>

<!-- Adding youtube videos
0 or 1 or 2 or 3 or 4, 0 (big) to 4 (small)
hqdefault.jpg <- high quality
mqdefault.jpg <- medium quality
sddefault.jpg <- standard definition
maxresdefault.jpg <- maximum resolution -->

_____________________________________________________________________________________     

<div align="center">
   
## **Prerequisites**
</div>



Before getting started with the assigned tasks, it was important to have PostgreSQL installed on my computer. In order to install this [Relational Database Management System](https://cloud.google.com/learn/what-is-a-relational-database) and its additional utilities, I had to run the following command:
```
sudo apt-get install postgresql postgresql-contrib
```

<div align="center">     

![image](https://ashnik-images.s3.amazonaws.com/prod/wp-content/uploads/2021/02/20050444/Postgresql-w-400x106.png)
   </div>

Next, I ensured that the status of the installed postgreSQL service was active. This was checked by runnning the following command:
```
service postgresql status
```
I was ready to get started with the assigned tasks as all of the conditions for the prerequisites had been met, when the output of the above command displayed PostgreSQL as an `active` service:
<div align="center">

![image](https://i.imgur.com/6cPtjnt.gif)
</div>

In the coming sections, the following assigned tasks will be performed and demonstrated:
- Task 1: Creation of Database
- Task 2: Schema Design
- Task 3: Relationships
- Task 4: Queries & Reporting

--------
<div align="center">

## **Task 1: Create Roles**
</div>

Roles in postgreSQL are users..............

## **1.1. Creating Three Roles**
> 1.1. Create three roles: admin, employee, and customer. Use the CREATE
ROLE statement

Once ensuring that the PostgreSQL service was active on the system, I proceeded with the first task for creating a database called 'keenable'. However, I had to follow some specific steps before so that I could be able to create the specified database.

First, I assumed the identity of the `Postgres` user for performing the administrative tasks related to PostgreSQL that are permitted to the default Postgres user. Such tasks include managing PostgreSQL, starting the PSQL terminal and writing SQL queries, to name a few. Switching to this user was done using the following command:
```
sudo su postgres
```

Here, sudo su is a command that is used for switching user or `su` using the privileges of a superuser `sudo`. As explained earlier, `postgres` is the user we switch to. The output of running the above command was as follows:
<div align="center">

![image](https://i.imgur.com/3zqrnw3.png)
</div>


## **1.2. Assigning Passwords**
> 1.2. Assign a password to each role    

Once ensuring that the PostgreSQL service was active on the system, I proceeded with the first task for creating a database called 'keenable'. However, I had to follow some specific steps before so that I could be able to create the specified database.

First, I assumed the identity of the `Postgres` user for performing the administrative tasks related to PostgreSQL that are permitted to the default Postgres user. Such tasks include managing PostgreSQL, starting the PSQL terminal and writing SQL queries, to name a few. Switching to this user was done using the following command:
```
sudo su postgres
```

Here, sudo su is a command that is used for switching user or `su` using the privileges of a superuser `sudo`. As explained earlier, `postgres` is the user we switch to. The output of running the above command was as follows:
<div align="center">

![image](https://i.imgur.com/3zqrnw3.png)
</div>

_____________________________

<div align="center">

## **Task 2: Grant Privileges**
</div>

Roles in postgreSQL are users..............

## **2.1. Creating DB: `ecommerce`**

____________
## **2.2 Assigning Privileges To Users**
https://tableplus.com/blog/2018/04/postgresql-how-to-grant-access-to-users.html

<div align="center">

#### **2.2.1 All DB Privileges To `admin`**
</div>

> The admin role should have full access to the ecommerce database.
When `\l` is run for cr

```
GRANT ALL PRIVILEGES ON DATABASE ecommerce TO admin;
```



<div align="center">

#### **2.2.2 Read & Write Table Privileges To `employee`**
</div>

> The employee role should have read and write access to the products table
in the ecommerce database.

<div align="center">

#### **2.2.3 Read Table Privileges To `customer`**
</div>

>The customer role should have read-only access to the products table.

In addition to the resouce mentioned in this section, I also utilised this [Article by CommandPrompt](https://www.commandprompt.com/education/how-to-create-a-read-only-user-in-postgresql/#:~:text=Conclusion-,To%20create%20a%20read%2Donly%20user%20in%20the%20PostgreSQL%20database,schema%2C%20and%20tables%20in%20it.) for creating granting a Read-Only privilege to the `Customer` user/role.
___________________




  <div align="center">

## **Conclusion**
</div>

After the completion of these 4 tasks, which greatly depended on building relationships between tables, I was able to learn and understand the concept of primary keys, foreign keys, constraints, joins and alters. Through this document, I was also able to demonstrate and perform the assigned tasks, which helped me gain a lot of practical understanding of PostgreSQL and SQL.

--------
