# DocEase - Doctor Appointment Booking System

A full-stack MERN application for booking doctor appointments online.

## Features

- User Registration & Login (Patients & Doctors)
- Doctor Search & Filtering
- Appointment Booking System
- Dashboard for managing appointments
- Role-based access control
- Responsive design

## Tech Stack

- **Frontend**: React.js, Tailwind CSS, React Router
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or cloud)
- npm or yarn

## Installation & Setup

### 1. Clone the repository
```bash
git clone <repository-url>
cd DOC_EASE
```

### 2. Backend Setup
```bash
cd server
npm install
```

### 3. Frontend Setup
```bash
cd ../client
npm install
```

### 4. Environment Configuration

Create a `.env` file in the server directory:
```env
PORT=5000
MONGODB_URI=mongodb://localhost:27017/docease
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
```

### 5. Database Setup

Make sure MongoDB is running on your system. The application will automatically create the database and collections.

### 6. Running the Application

#### Start the Backend Server
```bash
cd server
npm run dev
```
The server will run on http://localhost:5000

#### Start the Frontend
```bash
cd client
npm start
```
The client will run on http://localhost:3000

## Usage

### For Patients:
1. Register as a patient
2. Login to your account
3. Browse available doctors
4. Book appointments
5. Manage your appointments from the dashboard

### For Doctors:
1. Register as a doctor (provide specialization, experience, education, consultation fee)
2. Login to your account
3. View and manage patient appointments
4. Confirm or cancel appointments

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `GET /api/auth/me` - Get current user

### Doctors
- `GET /api/doctors` - Get all doctors
- `GET /api/doctors/:id` - Get single doctor
- `POST /api/doctors` - Create doctor profile
- `PUT /api/doctors/:id` - Update doctor profile

### Appointments
- `GET /api/appointments` - Get appointments
- `POST /api/appointments` - Book appointment
- `PUT /api/appointments/:id/status` - Update appointment status
- `DELETE /api/appointments/:id` - Cancel appointment

## Project Structure

```
DOC_EASE/
├── server/
│   ├── models/
│   │   ├── User.js
│   │   ├── Doctor.js
│   │   └── Appointment.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── doctors.js
│   │   └── appointments.js
│   ├── middleware/
│   │   └── auth.js
│   ├── config.js
│   └── server.js
├── client/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── services/
│   │   └── utils/
│   └── public/
└── README.md
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the ISC License.
