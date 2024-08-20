Resume Builder Application
Description
A Resume Builder Application that allows users to create, edit, and manage resumes. The application uses React for the frontend, Express.js for the backend, and integrates with OpenAI's GPT-3.5-turbo model to generate resume content.

Technologies Used
Frontend: React, Tailwind CSS, Axios, React Router
Backend: Express.js

AI Service: OpenAI GPT-3.5-turbo
Features
Resume Creation: Users can input their personal details and work history to generate a resume.
Resume Editing: Users can update their resumes with new information.
Resume Management: Users can view and delete their saved resumes.
Cover Letter Generation: Automatically generate a cover letter for job applications.
Installation
Frontend
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/resume-builder-client.git
Navigate to the project directory:

bash
Copy code
cd resume-builder-client
Install dependencies:

bash
Copy code
npm install
Create a .env file in the root directory and add your environment variables:

env
Copy code
REACT_APP_BACKEND_URL=http://localhost:4000
Start the development server:

bash
Copy code
npm start
Backend
Clone the repository:

bash
Copy code
git clone https://github.com/yourusername/resume-builder-server.git
Navigate to the project directory:

bash
Copy code
cd resume-builder-server
Install dependencies:

bash
Copy code
npm install
Create a .env file in the root directory and add your environment variables:

env
Copy code
PORT=4000
S3_BUCKET_ENDPOINT=your-s3-endpoint
S3_ACCESS_KEY_ID=your-access-key-id
S3_SECRET_ACCESS_KEY=your-secret-access-key
OPENAI_API_KEY=your-openai-api-key
Start the server:

bash
Copy code
npm start
API Endpoints
/resume/create
Method: POST

Description: Create a new resume.

Request Body:

fullName: Applicant's full name
currentPosition: Current job title
currentLength: Duration in current position
currentTechnologies: Technologies used
workHistory: JSON string of work history
Response:

message: Success message
data: Created resume data
/resume/send
Method: POST

Description: Generate a cover letter and send resume.

Request Body:

applicantName: Applicant's name
recruiterName: Recruiter's name
jobTitle: Job title being applied for
myEmail: Applicant's email
recruiterEmail: Recruiter's email
companyName: Company name
companyDescription: Company description
Response:

message: Success message
data: Cover letter, recruiter email, applicant email, resume URL
Contributing
Fork the repository.
Create a new branch (git checkout -b feature/YourFeature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/YourFeature).
Create a new Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.
