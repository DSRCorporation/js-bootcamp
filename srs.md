# JS Bootcamp 2019 SRS

## Project scope

The purpose of the project is to create a digital school diary.
The scope of the project includes creating several items:

1. ReactJS web app

## General requirements

Supported browsers:

1. Google Chrome 68+, Firefox 61.0+
   1. Desktop mode only
   1. Screen resolution 1024 \* 768 px and greater

No internationalization is assumed. All text should be in English.

## Roles and permissions

The system defines 2 different user roles:

1. Student
2. Teacher

Users with the roles described above should have the following permissions:

1. Teacher
   1. Can view a list of students
      1. Only in classes he teaches
   1. Can view a list of marks
      1. Only in classes he teaches
      1. Only for a subject he teaches
   1. Can add new marks
      1. Only in classes he teaches
      1. Only for a subject he teaches
   1. Can edit existing marks
      1. Only in classes he teaches
      1. Only for a subject he teaches
   1. Can not delete existing marks
   1. Can teach many classes
   1. Can teach only one subject
1. Student
   1. Can view a list of students
      1. Only in a class he belongs to
   1. Can view a list of marks
      1. Only ones that belong to him
   1. Can belong to only one class

## Functional requirements

Web application should provide the following major functions:

1. Account management
   1. Login
1. Classes
   1. View a list of classes
1. Students
   1. View a list of students
1. Teachers
   1. View a list of teachers
   1. Assign a class to a teacher
   1. Take a class away from a teacher
1. Marks
   1. View a list of marks
   1. Add a new mark
      1. Each mark is a number from 2 to 5
   1. Edit an existing mark
1. Subjects
   1. View a list of existing subjects

## User interfaces

Common elements:

1. The app should have a top menu with a full name of a logged-in user and "Log out" button. The menu should be visible only after a successful login. After clicking "Log out" button the user should be redirected to "Login" screen.

Screens:

1. Common
   1. Login
      1. Should have an input to enter a user name
         1. Full name should be used as a user name
      1. Should have an input to enter a password
1. Teacher
   1. List of classes
      1. A user should be redirected to "List of marks" screen upon clicking a class
   1. List of marks
      1. Should have a table with students as rows and dates as columns
      1. Should have a way to add a new mark
      1. Should have a way to edit an existing mark
      1. Should have a horizontal scroll if there are a lot of columns
         1. List of students should always be visible upon scrolling horizontally
1. Student
   1. List of students in one's class
   1. List of one's marks
      1. Should have a table with subjects as rows and dates as columns
      1. Should have a horizontal scroll if there are a lot of columns
         1. List of subjects should always be visible upon scrolling horizontally

## Non-functional requirements

Technology stack:

1. Web app
   1. ReactJS
   1. Redux
   1. Webpack

Delivery requirements:

1. The web app and documentation should be stored in a public repo on Github licensed under MIT license
2. The app should start with a single command `npm start`. After executing this command an end-user should be able to access the web app at [http://localhost:3001](http://localhost:3001/)
