# task-3
 Writing Basic SELECT Queries



I have created a student table and also I used WHERE, AND, OR, LIKE, BETWEEN and orderBy    

CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER,
    department TEXT,
    grade REAL
);

INSERT INTO students (id,name, age, department, grade) VALUES
(1,'Ravi Kumar', 20, 'CSE', 8.2),
(2'Anjali Mehta', 21, 'ECE', 7.9),
(3,'Sneha Das', 22, 'CSE', 9.1),
(4,'Karan Patel', 20, 'MECH', 6.5),
(5,'Divya Rani', 21, 'CSE', 7.4);

#SELECT All Columns
SELECT * FROM students;

# SELECT Specific Columns
SELECT name, department, grade FROM students;

#WHERE Clause
SELECT * FROM students
WHERE department = 'CSE'

#WHERE with LIKE
SELECT * FROM students
WHERE name LIKE 'D%';  -- names starting with D

#WHERE with BETWEEN
SELECT * FROM students
WHERE age BETWEEN 20 AND 21;

# ORDER BY (Ascending & Descending)
SELECT * FROM students
ORDER BY grade DESC;

#LIMIT Result Rows
SELECT * FROM students
ORDER BY grade DESC
LIMIT 3;

#Combined Example
SELECT name, grade FROM students
WHERE department = 'CSE' AND grade > 7.0
ORDER BY grade DESC
LIMIT 2;
