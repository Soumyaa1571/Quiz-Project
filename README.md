# KRS Quiz Project

The KRS Quiz Site is an innovative tool designed to enhance the learning experience of students. This site revolutionizes the traditional post-class quizzes by incorporating advanced features for user engagement, progress tracking, and healthy competition among students.

This is a backend project built with Node.js and MongoDB. It uses several libraries, including:

Express - a fast, minimalist web framework for Node.js

Bcrypt - a library to help hash passwords

Jsonwebtoken - a library to generate JWT tokens

Mongoose - a MongoDB object modeling tool
## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

DATABASE: the MongoDB connection string

SECRET_KEY: the secret used to sign JWT token

PORT: Contains the port on which server will run

You can create a .env file in the root directory of the project to set these variables.

# Installation

Clone the repository

```
https://github.com/Soumyaa07/MyProject.git
```
## Install Dependencies

#### Navigate to the Backend directory:
  ``` cd Backend backup\server ```
#### Install backend Dependencies
``` npm i ```  
#### Navigate to the project root directory:
  ``` cd..```
  ``` cd..```
#### Navigate to the frontend directory
  ``` cd Play Quiz\vite-project ```
#### Install frontend dependencies:
  ``` npm i ``` 

## Run Locally

#### Start the frontend server:
``` npm start ```
#### Start the Backend server 
 ``` npm run app ```




## API Reference



| Methods | Route      | Description                  | Request               | Response              |
| ------- | ---------- | ---------------------------- | --------------------- | --------------------- |
| POST    | /signin  | User Signin                  | { "email": "user@example.com", "password": "password" } | { "email": "user@example.com", "token": "authentication_token", "role": "user_role" } |
| POST    | /register| User Registration            | { "name": "User Name", "email": "user@example.com", "phone": "1234567890", "password": "password", "dob": "YYYY-MM-DD", "role": "student", "domain": "Your Domain" } | { "email": "user@example.com", "token": "authentication_token", "role": "user_role" } |
| POST    | /questions | Add Quiz Question         | { "ques": "Question Text", "option1": "Option 1", "option2": "Option 2", "option3": "Option 3", "option4": "Option 4", "correctans": "Correct Option" } | { "message": "Question added successfully" } |
| GET     | /gettest   | Retrieve Quiz Questions   | N/A                   | [ { "ques": "Question Text", "option1": "Option 1", "option2": "Option 2", "option3": "Option 3", "option4": "Option 4", "correctans": "Correct Option" }, ... ] |
| POST    | /Sheet     | Make Announcement         | { "heading": "Announcement Heading" } | { "message": "Announcement made successfully" } |
| GET     | /getSheet  | Retrieve Announcements    | N/A                   | [ { "heading": "Announcement Heading" }, ... ] |
| POST    | /feedback  | Submit Feedback           | { "name": "User Name", "email": "user@example.com", "message": "Feedback Message" } | { "message": "Feedback submitted successfully" } |
| GET     | /getfeedback | Retrieve Feedback       | N/A                   | [ { "name": "User Name", "email": "user@example.com", "message": "Feedback Message" }, ... ] |


The middleware function is responsible for following:
- User authentication using JSON Web Tokens (JWTs)
- User registration
- Adding quiz questions
- Retrieving quiz questions
- Making announcements
- Retrieving announcements
- Submitting feedback
- Retrieving feedback
- Checking if a test has been attempted
- Storing test results

# Landing Page
![Screenshot 2024-08-15 130913](https://github.com/user-attachments/assets/90cbe64c-0242-4912-b438-28c10317dc2d)

 
# Header Section

The Navbar component serves as the navigation bar for the web application. It includes the "KRS Quizzes" title/logo and navigation links to different sections of the application.

### Title

The "KRS Quizzes" title, displayed as a Link component, serves as a clickable element that navigates users to the home page ("/").

### Navigation Links

The navigation links consist of NavLink components from React Router, allowing users to navigate to different sections of the application:

- **About:** Navigates users to the "/about" route, providing information about the application.
- **Announcements:** Navigates users to the "/announcements" route, where they can view announcements.
- **Quizzes:** Navigates users to the "/quizzes" route, allowing them to access quizzes.
- **Contact Us:** Navigates users to the "/contact" route, providing contact information.

### Login/Logout Button

This component conditionally renders a “Login” or “Logout” link based on the isLoggedIn state.

![image](https://github.com/user-attachments/assets/f63d01ff-2f62-411e-9533-031a0d013b24)

 # The Login Page

The Login form includes the following input fields:

- **Email:** This field allows users to enter their email address for authentication purposes.
- **Password:** This field is for entering the user's password.

Below the input fields, there is a "Sign in" button for submitting the login credentials.

# The SignUp page

![image](https://github.com/user-attachments/assets/60ae6e51-b442-427c-ab24-29b4e98079b3)


The SignUp form includes the following input fields:

- **Name:** This field allows users to enter their name.
- **Email:** This field allows users to enter their Email id.
- **Enter Password:** This field allows users to enter their Password.
- **Re-enter Password:** This field allows users to re-enter their password.
- **Your Domain:** This field allows users to enter their Domain.
- **Role:** This field is a special input where users enter 'Student' if they are a Student or 'Member' if they are admin.
- **Phone:** This field allows users to enter their Phone No.
- **Birth Date:** This field allows users to enter their Date of Birth.

Below the input fields, there is a "Sign Up" button for submitting the signup details.

# The About page

![Screenshot 2024-08-15 130929](https://github.com/user-attachments/assets/a6b0bd30-54dc-4a86-be66-8958689e2e3e)


# Announcement Page

![image](https://github.com/user-attachments/assets/3f9bdb8b-6918-4f67-9a49-e91f05950cbb)


# Announcement Page Components

The Announcement Page consists of the following components:

1. **Make an Announcement:**
   - Visibility: Only accessible to Members.
   - Description: This component allows Members to create and publish announcements. It is not visible or accessible to Students.
![image](https://github.com/user-attachments/assets/aec8f8ba-dcc0-44d5-80bc-722a89daa2cf)



2. **View the Announcements:**
   - Visibility: Visible to both Members and Students.
   - Description: This component allows both Members and Students to view published announcements.
   - ![image](https://github.com/user-attachments/assets/cef88704-8a37-4a5a-9d1c-67aca466bfab)



3. **View Feedbacks:**
   - Visibility: Only accessible to Members.
   - Description: This component allows Members to view feedback provided by users. It is not visible or accessible to Students.
   - ![image](https://github.com/user-attachments/assets/8a2fe6e2-8c1c-418a-bfc5-104ee7bb58e9)


4. **View Result:**
   - Visibility: Only accessible to Members.
   - Description: This component allows Members to view results or outcomes. It is not visible or accessible to Students.
   - ![image](https://github.com/user-attachments/assets/39d5523b-bdb1-4073-a78d-feb3d2dede96)


# Quize Page

![image](https://github.com/user-attachments/assets/3cfe23a6-9c7b-46cd-88b7-2e2292d6ef6c)


# Quiz Page Components

The Quiz Page consists of the following components:

1. **Create a Quiz:**
   - Accessibility: Only accessible to Members.
   - Description: This component opens a form that allows Members to create quiz questions.
   - ![image](https://github.com/user-attachments/assets/f932967c-9716-4622-bafd-1dd77d91decf)



2. **Start Quiz:**
   - Accessibility: Accessible to both Students and Members.
   - Description: This component allows both Students and Members to start the quiz.
   

# Contact Page
This page contains a feedback form where users can put their valuable feedback along with name and Email.
  ![image](https://github.com/user-attachments/assets/a3826b6e-3fff-4318-82e2-5b8592b5bcc7)




