<b>Frontend :</b><br>
To run the frontend use command <br>
npm run dev<br>
<b>Backend:</b><br>
To run backend use command <br>
node app.js<br>
<b>Database:<b><br>
Database used over here is MongoDB over cloud (Mongodb Atlas).<br>
The reason for choosing the mongodb is because of it is a nosql database which provides dynamic schema design.<br>
<h3>Working of the Project</h3><br>

This project is a Customer Management System that allows users to manage customer-related data such as first name, last name, email, phone number, company, and job title. It is built using Node.js, Express, and MongoDB for the backend, and Material-UI for the frontend.<br>

<h4>1. Frontend (React with Material-UI)</h4><br>
The frontend is built using React and utilizes Material-UI components for styling. It provides an easy-to-use form for users to input customer data:<br>

The form contains fields for first name, last name, email, phone number, company, and job title.<br>
The user enters the required details and clicks the Submit button.<br>
Upon submission, the form data is sent to the backend via an HTTP POST request using Axios.<br>
2.<h4> Backend (Node.js and Express)</h4><br>
The backend is built using Node.js and Express, which provides the necessary APIs to manage customer data:<br>

POST Request (/contacts): When the form is submitted, the data is sent to the backend, where it is handled by an Express route. This route processes the incoming data and stores it in the MongoDB database.<br>
Database Interaction (MongoDB): The data is stored in a MongoDB database collection named contacts. The schema is flexible, allowing different fields to be added or omitted as necessary.<br>
<h4>3. Database (MongoDB)</h4><br>
The MongoDB database stores all customer data in a document-based format, making it easy to scale and manage.<br>
Each document in the database represents a customer and contains fields like firstName, lastName, email, phoneNumber, company, and jobTitle.<br>
<h4>4. Data Validation and Error Handling</h4><br>
On the frontend, form validation is implemented to ensure that all fields are filled in correctly before the form is submitted.<br>
On the backend, error handling ensures that any issues (e.g., database connection failures, missing data) are captured and returned to the user with appropriate messages.<br>
<h2>Challenges Faced</h2>
<h3>Database Integration with MongoDB</h3>
Integrating MongoDB for data storage was straightforward, but I faced some initial difficulty in structuring the database schema to meet the project requirements. I had to ensure that the data models were flexible enough to handle different types of customer data without rigid constraints.

Solution: I decided to keep the MongoDB schema simple and flexible by using Mongoose to define the customer data model. I ensured that the fields were optional where necessary and added validation to enforce required fields like email and phone number.
<h3>Frontend Validation and UX Challenges</h3>
Ensuring that the form validation on the frontend was both user-friendly and functional posed a challenge. I needed to make sure the user received feedback when submitting incomplete or incorrect data.

Solution: I used Material-UI's TextField component's built-in validation and error handling features. I also ensured that the form was not submitted unless all required fields were filled in, providing immediate feedback to the user.
