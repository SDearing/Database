# Entity-Relationship-Diagrams-Example
## Scenario
A student registers for up to 8 modules and each module has many students on it. Record the student ID, their full name and address and also
each module ID and title. Also, each module is related to a specific course,
each course has a course ID and a title. Also, each course is related to a
department. Finally, each department has a department ID, a name, and a
head of the department
## ERD
![ERD](https://github.com/SDearing/Entity-Relationship-Diagrams-Example/blob/master/ERD.PNG)
The tool I used to create this ERD was found on www.Draw.io
## SQL Code Examples
INSERT INTO (Student) VALUES (01,Jack,Smith,38 Long Lane)
This inserts a new record into the table with a student ID of 01, first name Jack, last name Smith and whos address is 38 Long Lane.
UPDATE (Student) SET (Bob) WHERE (First Name) IS (Jack)
This updates the value of the Field First Name to Bob if the records first name equals Jack
DELETE FROM Student WHERE (First Name) IS (Bob)
This deletes the record with the first name of Bob
