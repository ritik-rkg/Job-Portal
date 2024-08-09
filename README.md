# Job Portal

A full-stack job portal web application developed using the MERN stack (MongoDB, Express.js, React.js, Node.js). The application allows recruiters to post jobs, candidates to apply for jobs, and administrators to manage users and job postings.

## Features

### User Roles
- **Recruiters**:
  - Register/Login to the platform.
  - Create, view, and manage job postings.
  - View applications for their job postings.
  
- **Candidates**:
  - Register/Login to the platform.
  - Browse available jobs.
  - Apply for jobs with resume attachments.
  - View application history.

- **Admin**:
  - Manage all users (recruiters and candidates).
  - View and manage all job postings.
  - Approve or reject job postings.

### Core Features
- **Authentication**: Secure user authentication using JWT tokens and bcrypt for password hashing.
- **Dashboard**: Role-specific dashboards for recruiters, candidates, and admin.
- **Job Postings**: Create, edit, and delete job postings with rich text descriptions and skill tags.
- **Applications**: Candidates can apply for jobs and upload resumes; recruiters can view and manage applications.
- **Admin Panel**: Manage users, job postings, and applications with full control over the platform.

## Tech Stack

- **Frontend**: React.js
  - React Router for navigation.
  - Axios for API requests.
  - Bootstrap for UI components.

- **Backend**: Node.js, Express.js
  - RESTful API design.
  - JWT-based authentication.
  - Express middleware for routing and error handling.

- **Database**: MongoDB
  - Mongoose for schema and model creation.
  - MongoDB Atlas for cloud storage.

- **Authentication**: 
  - JSON Web Tokens (JWT) for secure user sessions.
  - bcrypt.js for password encryption.

## Setup and Installation

### Prerequisites
- Node.js and npm installed on your machine.
- MongoDB Atlas account for cloud database storage (or a local MongoDB instance).

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/Job-Portal.git
   cd Job-Portal
   ```

2. **Install server dependencies:**
   ```bash
   cd backend
   npm install
   ```

3. **Install client dependencies:**
   ```bash
   cd ../frontend
   npm install
   ```

4. **Set up environment variables:**
   - Create a `.env` file in the `backend` directory with the following:
     ```bash
     MONGO_URI=your_mongodb_connection_string
     SECRET_KEY=your_jwt_secret
     PORT=8000
     CLOUD_NAME=your_cloud_name (you can get this by creating account on cloudinary)
     API_KEY=your_cloudinary_api_key
     API_SECRET=your_cloudinary_api_secret
     
     ```

5. **Run the application:**
   - Start the backend server:
     ```bash
     cd backend
     npm start
     ```
   - Start the frontend development server:
     ```bash
     cd ../frontend
     npm start
     ```

6. **Access the application:**
   - Open your browser and navigate to `http://localhost:5173` for the frontend.
   - The backend API will be running on `http://localhost:8000`.

## Folder Structure

```
job-portal/
│
├── backend/                # Express.js server code
│   ├── config/             # Configuration files (db, env, etc.)
│   ├── controllers/        # Route controllers
│   ├── models/             # Mongoose models
│   ├── routes/             # API routes
│   ├── middleware/         # Express middleware (auth, error handling)
│   └── server.js           # Server entry point
│
├── frontend/               # React.js client code
│   ├── public/             # Public assets and index.html
│   ├── src/                # React app source code
│   │   ├── components/     # Reusable components
│   │   ├── pages/          # Page components
│   │   ├── context/        # React context for state management
│   │   ├── hooks/          # Custom React hooks
│   │   ├── services/       # API services using Axios
│   │   └── App.js          # App entry point
│   └── package.json        # Frontend dependencies and scripts
│
└── README.md               # Project documentation
```

## Contributing

Feel free to fork this repository and contribute by submitting a pull request. For major changes, please open an issue first to discuss what you would like to change.
