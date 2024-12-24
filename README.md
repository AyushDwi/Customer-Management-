<b>Frontend:</b><br> To start the frontend application, run the following command:<br> npm run dev<br>

<b>Backend:</b><br> To initiate the backend server, execute the command:<br> node app.js<br>

<b>Database:</b><br> This project uses a cloud-based NoSQL database, MongoDB Atlas.<br> MongoDB was selected due to its flexible schema design, which makes it highly adaptable to changing data structures.<br>

<h3>How the Project Works</h3><br>
The project is a Customer Management System designed to handle customer-related information, such as first name, last name, email, phone number, company, and job title. The backend is developed using Node.js, Express, and MongoDB, while the frontend is built using React and styled with Material-UI.<br>

<h4>1. Frontend (React + Material-UI)</h4><br> The user interface is built with React and styled using Material-UI components. It includes a form for entering customer data:<br>
The form contains input fields for first name, last name, email, phone number, company, and job title.<br>
Users can fill out the required fields and click the "Submit" button.<br>
Upon submission, the data is sent to the backend via an Axios HTTP POST request.<br>
<h4>2. Backend (Node.js + Express)</h4><br> The backend is powered by Node.js and Express and provides the necessary API endpoints to handle customer data:<br>
POST Endpoint (/contacts): This endpoint receives the data submitted from the frontend, processes it, and saves it to the MongoDB database.<br>
Database Integration (MongoDB): Customer data is stored in a collection called contacts. The schema is flexible and supports adding or omitting fields as needed.<br>
<h4>3. Database (MongoDB)</h4><br> The database utilizes MongoDB for storing customer information in a document-based format, ensuring scalability and easy management:<br>
Each document represents a customer with fields such as firstName, lastName, email, phoneNumber, company, and jobTitle.<br>
MongoDB's dynamic schema allows for easy adjustments to the data model.<br>
<h4>4. Data Validation and Error Handling</h4><br> The project includes robust validation and error handling mechanisms:<br>
Frontend: Validation ensures all required fields are properly filled out before submission, providing instant feedback to the user.<br>
Backend: Error handling captures issues like missing data or database connection failures and returns appropriate error messages to the client.<br>
<h2>Challenges Encountered</h2> <h3>1. Database Integration with MongoDB</h3> Integrating MongoDB as the database was straightforward, but defining a schema that balanced flexibility and structure posed challenges.<br>
Solution: To address this, I utilized Mongoose to create a flexible schema for customer data. I incorporated optional fields where necessary and implemented validation rules for critical fields like email and phone number.<br>

<h3>2. Frontend Validation and User Experience (UX)</h3> Implementing a seamless form validation mechanism while maintaining an intuitive user experience was challenging. I aimed to provide immediate feedback for incomplete or invalid inputs.<br>
Solution: By leveraging Material-UI's TextField component, I integrated built-in validation and error handling features. Additionally, I ensured the form could not be submitted until all mandatory fields were correctly filled out, enhancing the overall user experience.<br>

