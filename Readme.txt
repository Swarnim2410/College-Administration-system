How to run the Student Management System (StudentMS) Project

1. Download the  zip file

2. Extract the file and copy studentms folder

3.Paste inside root directory(for xampp xampp/htdocs, for wamp wamp/www, for lamp var/www/html)

4. Open PHPMyAdmin (http://localhost/phpmyadmin)

5. Create a database with name studentmsdb

6. Import studentmsdb.sql file(given inside the zip package in SQL file folder)

7.Run the script http://localhost/studentms (frontend)



Credential for admin panel :

Username: admin
Password: Test@123

Credential for Student / Faculty panel :

 --> Register a new Student/Faculty.


---> Brief Working Details of the Project:-

In the project implementation we have the following entities :
• Admin
• Students
• Faculties
• Departments (CSE, ECE, BS)
• Courses
• Head of Department
• Marks and Attendance
• Exam Schedule through Notices

All the three main entities of the project i.e. Admin, Students and Faculties can 
login through their respective login portals.

The Roles of the Admin: 

➢ Admin can add a new student by getting his/her data through a form that 
contains the basic details like name, gender, dob etc. Admin will then provide 
a new username and id to the enrolled student.
➢ Admin can edit the details of the student at any point of time.
➢ Admin can add a new Faculty by getting his/her data through a form that 
contains the basic details like name, gender, dob etc. Admin will then provide 
a new username and id to the enrolled Faculty.
➢ Admin can edit the details of the Faculty at any point of time.
➢ Admin can add a new course in any department and assign faculties to the 
course. One course in a department can have only one faculty but one faculty 
can teach more than one course.
➢ Admin can assign multiple courses to any of the enrolled students. The 
enrolled student can only get the courses belonging to his/her respective 
department.
➢ Admin can issue a public notice which is accessible to both the faculties and 
the students. It can be helpful in providing the details regarding the exam 
schedule. The Notice would be displayed in the home page.
➢ Admin can edit its own details as well.


The Roles of the Faculty:

➢ As soon as the faculty logins through his/her login portal, his/her personal 
dashboard will show all the courses which are assigned to him/her.
➢ The Faculty can view all the students that are enrolled in his/her assigned 
courses. 
➢ The Faculty can add/edit the marks and attendance of a particular student in a 
particular course.
➢ The updated marks would be available for students to see in their respective 
dashboards.
The Roles of the Student:
➢ As soon as the student logins through his/her login portal, his/her personal 
dashboard will show all the courses in which he/she is enrolled.
➢ The student can then view the respective marks and attendance of a particular 
course in which he/she is enrolled.

Relational Schema:

Below is the relational schema representing these tables and their relationships: 

1. course:
• Fields: studentID (Primary Key), courseName (Primary Key)

2. tblstudent: 
• Fields: ID (Primary Key), StudentName, StudentEmail, StudentClass, 
Gender, DOB, StuID, FatherName, MotherName, ContactNumber, 
AltenateNumber, Address, UserName, Password, Image, 
DateofAdmission 

3. tbladmin: 
• Fields: ID (Primary Key), AdminName, UserName, MobileNumber, 
Email, Password, AdminRegdate

4. info: 
• Fields: studentId (Primary Key), courseName (Primary Key) , marks, 
attendance

5. tblfaculty: 
• Fields: ID (Primary Key) , FacultyName, FacultyEmail, Department, 
Gender, DOB, FacultyID, ConatctNumber, UserName, Password, 
DateOfAdmission

6. tblclass: 
• Fields: ID (Primary Key), ClassName, Section, CreationDate, Faculty

7. tblpublicnotice: 
• Fields: ID (Primary Key), NoticeTitle, NoticeMessage, CreationDate
