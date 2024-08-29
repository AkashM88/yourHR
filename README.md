# yourHR
Find your dream job by signing up and uploading your resume




This project is a basic fullstack web application that allows job seekers to sign up by filling out a form with their personal information and uploading their resume. The application uses a Node.js backend with Express.js for handling requests, MongoDB for storing user data, and a simple frontend built with HTML, CSS, and JavaScript.

Architecture
The application follows a typical MVC (Model-View-Controller) pattern:

Model: The Mongoose model defines the schema for storing user information in MongoDB.
View: The frontend consists of simple HTML pages (index.html and signup.html) with CSS for styling.
Controller: The Express.js routes handle HTTP requests, process form data, and interact with the database.


Frontend
Home Page (index.html)

Displays a simple introduction to the application.
Provides navigation links to the signup page.


Signup Page (signup.html)

Contains a form where users can enter their full name, email, phone number, and upload their resume.
Submits the form data to the backend for processing.



Backend
Express Server (app.js)

Initializes an Express server and connects to MongoDB using Mongoose.
Serves static files from the public directory.
Handles routes, including the signup route for processing form submissions.


Mongoose Model (models/User.js)

Defines the User schema, which includes fields for fullName, email, phone, and resume.
Each field is validated to ensure the data is stored correctly in the MongoDB database.


Signup Route (routes/signup.js)

Uses the multer middleware to handle file uploads (resumes).
Saves the user's information and the uploaded resume file name in the MongoDB database.
Responds to the client with a success or error message.
