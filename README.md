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
## SQL Code
### CREATE 
The create function is used to construct the tables that will be used by the database, for this example I will be using the CREATE command to create the 'Enemy' table of the database.

![create](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/CREATE.PNG)

The first line of code is used to establish the name of the table, then below the different fields of the table are described. For example on the third line the 'Name' field is first established, then the max amount of characters is specified and that the data inputted in this field will be a string by writing "VARCHAR(50)", finally the field is set to never be blank by writing "NOT NULL"
### INSERT
The insert function is used to input a record into the database, for this example I will be inputting a record in the 'Enemy' table.

![insert](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/INSERT.PNG)

In this example I first declare that I am inserting into the enemy table, then on the next line I declare the values of each field as they appear in the table.
### Update
The update function is used to change the fields of a record, in this example, I will be updating the name of the current record I just inserted, to change the name 'Dragon' to 'Lizard'.

![update](https://github.com/SDearing/Database/blob/master/UPDATE%20SQL.PNG)
