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
### 3.0 Risks and Constraints
#### 3.1 Risks
