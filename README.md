# Databases
Databases are constantly used in the software industry, this is because most software companies need to store information for their software to work, be it, storing user information for a social media website or keeping track of orders on an online shop, databases are vital for the storing, sorting and viewing of information.

Databases are usually created by first designing tables for the objects you are storing data for, each table being based on a different category of object, involving different attributes that need to be stored. Once the tables have been designed then they need to be put into a entity relationship diagram, a ERD is a way of showing the relationship between different tables so the database builder can see how the whole database will function. For example a student table may be linked to a teacher table with a many-to-one link as a teacher can have multiple students but a student will only have one teacher for that subject.
## Entity Relationship Diagram
Below is the entity relationship diagram that I am using for my database
![ERD](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/ERD.PNG)
The tool I used to create this ERD was found on www.Draw.io
## SQL Code Examples
INSERT INTO (Student) VALUES (01,Jack,Smith,38 Long Lane)
This inserts a new record into the table with a student ID of 01, first name Jack, last name Smith and whos address is 38 Long Lane.
UPDATE (Student) SET (Bob) WHERE (First Name) IS (Jack)
This updates the value of the Field First Name to Bob if the records first name equals Jack
DELETE FROM Student WHERE (First Name) IS (Bob)
This deletes the record with the first name of Bob
