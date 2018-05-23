# Databases
Databases are constantly used in the software industry, this is because most software companies need to store information for their software to work, be it, storing user information for a social media website or keeping track of orders on an online shop, databases are vital for the storing, sorting and viewing of information.

Databases are usually created by first designing tables for the objects you are storing data for, each table being based on a different category of object, involving different attributes that need to be stored. Once the tables have been designed then they need to be put into a entity relationship diagram, a ERD is a way of showing the relationship between different tables so the database builder can see how the whole database will function. For example a student table may be linked to a teacher table with a many-to-one link as a teacher can have multiple students but a student will only have one teacher for that subject.
## Entity Relationship Diagram
Below is the entity relationship diagram that I am using for my database, which also contains the tables for a basic RPG game.
![ERD](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/ERDExample.PNG)

The tool I used to create this diagram was www.Draw.io, a website that allows you to create diagrams.
In the diagram the 'Enemy' table has a many-to-one relationship with the 'Enemy Skills' table, as a enemy can have multiple enemy skills but a enemy skill can only belong to one enemy. The 'Hero' table has the same relationship with the 'Hero Skills' table for the same reason. Finally both the 'Enemy Skills' and 'Hero Skills' have a many-to-one relationship with the 'Skills' table, as the skill table will provide the skills to be used by the heroskills and enemyskills.
## Data Dictionaries
Data dictionaries are a documentation of the tables of the database, containing the fields of each table, the data type of the data being held by the field and extra information on the field such as how many characters will be in a string field. Every table will contain a primary key which is the unique indicator for each individual record, this is so specific records can be found with ease especially with tables containing a large amount of records. Some tables may also have a foreign key which is the primary key from the table it is linked to, this is also so certain records can be found with more ease.
Below is the data dictionary for my database, to make the data dictionary I used the tool software Excel.
![DD](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/DatabaseDictionary.PNG)

## User Stories
When planning the requirements of the database, user stories can be used. User stories are simple objectives that need to be completed to fully suit the users needs and can also be used as milestones in the development process.
* I would like to see how much hp each hero has
* I would like to see how much hp the enemy has
* I would like to see the name of the enemy
* I would like to see how much damage/healing a skill is dealing
* I would like to see the type of a skill
* I would like to see the name of a hero
* I would like to see the race of a hero
* I would like to see the status of a hero
* Each Record should have a unique ID
## Forms and Reports for Database
In a database a form is a more user friendly way of inputting data into a table than by using a query. A report is a clearer way of presenting data from a table. Below is a collection of all forms and reports from my database.
### ENEMIES Form
![EnemiesForm](https://github.com/SDearing/Database/blob/master/EnemiesForm.PNG)
### ENEMIES Report
![EnemiesReport](https://github.com/SDearing/Database/blob/master/Enemies%20report.PNG)
### HEROES Form
![HeroesForm](https://github.com/SDearing/Database/blob/master/HeroesForm.PNG)
### HEROES Report
![HeroesReport](https://github.com/SDearing/Database/blob/master/HeroesReport.PNG)
### ENEMIES_SKILLS Form
![EnemySkillForm](https://github.com/SDearing/Database/blob/master/EnemySkill%20Form.PNG)
### ENEMIES_SKILLS Report
![EnemySkillReport](https://github.com/SDearing/Database/blob/master/EnemySkillReport.PNG)
### HEROES_SKILLS Form
![HeroSkillForm](https://github.com/SDearing/Database/blob/master/HeroSkillForm.PNG)
### HEROES_SKILLS Report
![HeroSkillReport](https://github.com/SDearing/Database/blob/master/HeroSkill%20Report.PNG)
### SKILLS Form
![SkillForm](https://github.com/SDearing/Database/blob/master/SkillForm.PNG)
### SKILLS Report
![SkillReport](https://github.com/SDearing/Database/blob/master/SkillReport.PNG)
## SQL Code
### CREATE 
The create function is used to construct the tables that will be used by the database, for this example I will be using the CREATE command to create the 'Enemy' table of the database.

![create](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/CREATE.PNG)

The first line of code is used to establish the name of the table, then below the different fields of the table are described. For example on the third line the 'Name' field is first established, then the max amount of characters is specified and that the data inputted in this field will be a string by writing "VARCHAR(50)", finally the field is set to never be blank by writing "NOT NULL"
### INSERT
The insert function is used to input a record into the database, for this example I will be inputting a record in the 'Enemy' table.

![insert](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/INSERT.PNG)

In this example I first declare that I am inserting into the enemy table, then on the next line I declare the values of each field as they appear in the table.
### UPDATE
The update function is used to change the fields of a record, in this example, I will be updating the name of the current record I just inserted, to change the name 'Dragon' to 'Lizard'.

![update](https://github.com/SDearing/Database/blob/master/UPDATE%20SQL.PNG)

In the code I first declare which table is being updated, then what I want the new updated value to be and what field it should be upated in and finally under what condition should be met to change the value of the field. In this example I have declared that I am updating the ENEMIES table and changing the NAME field to 'LIZARD' whenever it finds the name 'DRAGON'.
### DELETE
The delete function is used to remove certain records from a database. In this example I will be removing a record from the 'ENEMIES' table with the name 'Mistake'.

![delete](https://github.com/SDearing/Database/blob/master/DELETESQL.PNG)

In the code I first declare what table I am deleting from, then I set the condition of when a record should be deleted.

### SELECT
The select command is used to find the value of fields in a database, this command is especially useful when working with large databases. For this example I will be selecting all hero names in the table.

![SELECT](https://github.com/SDearing/Database/blob/master/SELECT.PNG)

In the code I first declare what columns I am selecting from (NAME) and then the table I am selecting from, giving the result 

## The User Manual
Technical and user documentation
### 1.0 General Information
#### 1.1 System Overview
This database is designed to hold information about the heroes, enemies and their skills in an RPG game. The data assigned for heroes will be their level, name, race and status. The data for enemies will be their name, health points and damage. The data for skills will be the name, damage or heal, the type of damage and range.
#### 1.2 Tools used
The following list is the tools that I used during the development process of the database.
* Draw.io to make the Entity Relationship Diagram
* Microsoft Excel 2016 was used to make the data dictionary
* Microsoft Access 2016 was used to make the database
* Microsoft Word 2016 was used to make the technical and user documentation
#### 1.3 The Role of Database Systems
#### 1.3.1 Back-end System
A back-end system is a database that can be accessed by multiple users by using an external application rather by using the software that the database is being used to host the database or by using SQL code.
#### 1.3.2 E-commerce
E-commerce databases are used to store information about an online store. This information stored will usually be their products, stock and customer transactions. A e-commerce database focuses on two main categories: site content and transactional data. Site content refers to the information we see while browsing a website, so the list of products and information on specific products. Transactional data refers to the actions of the user on the website, which would include customer orders and inventory updates.
#### 1.3.3 Data Mining 
Data mining is the process of finding patterns in large sets of data, this is so large amounts of data can be managed with more ease. Data mining is also useful for finding useful peices of data out of a set of raw data and assures that a database only includes useful data.
### 2.0 System Summary
#### 2.1 What is an Object Oriented Database
Object oriented databases are used to store objects rather than normal data such as integers. Objects are used in object oriented programming and consist of attributs and methods. Attributes are data that defines the characteristics of an object and methods refers to the behaviour of the object; also known as the functions of the object. Therefore an object oriented database is designed to hold the executable code of the object's methods and the data of their attributes. Another system an object database supports, is the use of classes and inheritance. Classes define the attributes and methods an object will contain, acting as a template for an object. Inheritance is the method of creating a object from a class.
#### 2.2 What is the System for?
This system is used to hold the attributes of the player characters and enemies, aswell as the attributes of the skills they will be using. 
### 3.0 Risks and Contingencies
#### 3.1 Risks
During development there will be risks that will disrupt the development process of the database, possible risks are:
* Forms having incorrect data being inputted into them, i.e a string being enntered into a field when it is expecting an integer.
* Relationships between tables not being correctly implemented.
* Tables not being normalised fully. Normalisation is the process of restructuring a database to ensure that there are no data redundancies and ensure the integrity of the data within the tables.
* Errors in SQL code which would create errors in the database
#### 3.2 Contingencies
To avoid the risks previously mentioned certain contingencies need to be put in place:
* Assign a data type to each field: to assure that the wrong data is not put into a field, every field will be assigned a data type to be checked for, when a user is inputting a new record.
* Create a clear design of the ERD: to assure that the relationship between each table is correct, the ERD will be first designed on paper so that all the relationships can be planned out and checked to see if they are the correct type of relationships.
* Design of database will be put through layers of normalisation: Before the database is implemented in microsoft access, the design of the tables will be put through the layers of normalisation to make sure every peice of data is not redundant.
* Multiple versions of the database will be saved: incase an error in the development process disrupts the database, previous versions of the database will be saved, so that if there is an issue a previous working version can be implemented and the development process can continue.
### 4.0 Design Decisions
#### 4.1 Key Factors Influencing Design
A key functionality I focused on during the design was the implementation of player/hero and enemy skills in the game. To do this I created a skill table that holds the main bulk of data about each skill in the game. Then to assign those skills to the players and the enemies, I created new two tables which contained the skills that each enemy and player have access to in the game and created many-to-one relationships with the skill table; as a player/enemy can have many skills but a skill can only belong to one player/enemy.
#### 4.2 Database Management System Decision
The DBMS that I decided to use to create the database was Microsoft Access 2016. I am using this software because Access provides the tools to create my database in a effective and effecient way. Some of the tools provided are the integration of SQL queries to create and manipulate tables, a simple format to create forms and reports from the database and the ability to change data in a table with relative ease. Another point worth mentioning is Access' simple UI which allows me to navigate around the DBMS and find and use the tools effectively.
#### 4.3 Security and Privacy Design Decision
The database that I created is private, meaning that only someone with access to the database file can edit and view it. This means that there is minimal risk of someone breaching the database, but ensure the database is secure I will make sure that only I have access to any copies of database.
#### 4.4 Performance and Maintenance Design Decision
The database only required a limited amount of user requirements, this meant that the scope of the database was not that large. This means that the database will run at a high performance anyway, so no decisions needed to be made performance-wise. Maintenance on the database will be conducted weekly as new records are added and new user requirements are given.
## Test Plan
To ensure that the user and system requirements of the database are met, I will be conducting tests on the system to make sure all aspects of the database are working correctly. To illustrate these tests I have created a test plan with the outcomes of each test included in the table.
