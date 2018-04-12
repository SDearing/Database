# Databases
Databases are constantly used in the software industry, this is because most software companies need to store information for their software to work, be it, storing user information for a social media website or keeping track of orders on an online shop, databases are vital for the storing, sorting and viewing of information.

Databases are usually created by first designing tables for the objects you are storing data for, each table being based on a different category of object, involving different attributes that need to be stored. Once the tables have been designed then they need to be put into a entity relationship diagram, a ERD is a way of showing the relationship between different tables so the database builder can see how the whole database will function. For example a student table may be linked to a teacher table with a many-to-one link as a teacher can have multiple students but a student will only have one teacher for that subject.
## Entity Relationship Diagram
Below is the entity relationship diagram that I am using for my database, which also contains the tables for a basic RPG game.
![ERD](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/ERDExample.PNG)

The tool I used to create this diagram was www.Draw.io, a website that allows you to create diagrams.
In the diagram the 'Enemy' table has a many-to-one relationship with the 'Enemy Skills' table, as a enemy can have multiple enemy skills but a enemy skill can only belong to one enemy. The 'Hero' table has the same relationship with the 'Hero Skills' table for the same reason. Finally both the 'Enemy Skills' and 'Hero Skills' have a many-to-one relationship with the 'Skills' table, as the skill table will provide the skills to be used by the heroskills and enemyskills.
## SQL Code Examples

