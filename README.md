🎓 Student-Course Enrollment System using Sparse Hash Table
This Java application demonstrates a sparse hash table implementation for storing relationships between students and their enrolled courses. It supports bidirectional queries:

Retrieve all courses for a student

Retrieve all students in a course

🧠 Core Concepts
Custom hash-based sparse table (hash map with separate chaining)

Data structures: Linked lists and arrays

Object-oriented programming in Java

Efficient memory use in sparse scenarios (not all students take all courses)

🧾 Project Overview
The application includes:

students: class to represent a student with ID and name

courses: class to represent a course with course_id and name

sparse_table: class that:

Uses a hashed array of nodes to map students to courses and vice versa

Handles collisions using chaining

Supports efficient insertions and queries

Main: demo program to:

Create students and courses

Enroll students in courses

Retrieve courses per student and students per course

💡 Example Output
text
Copy code
Course for student 123 is : 
Data structures
Programming
Data science

Students for course 130 is : 
ali
📚 Classes
✅ students
Fields: ID, name

Represents a student

✅ courses
Fields: course_id, name

Represents a course

✅ sparse_table
Node class stores each relationship (student-course)

arr[] stores Nodes indexed via a hash of student ID and course ID

Methods:

insert(student, course)

getstudentcourses(studentId)

getcoursestudents(courseId)

🛠️ How It Works
Calculate a hash index from student ID and course ID.

Store the (student, course) relationship at that index.

Use chaining to resolve collisions.

Query by scanning through all columns/rows and matching IDs.

🚀 Getting Started
Compile & Run
javac Main.java
java Main

No external libraries needed.
