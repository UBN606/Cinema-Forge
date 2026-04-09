# Architecture Design

## Overview
The architecture of the Cinema-Forge application is designed to facilitate the development of a robust and scalable online cinema booking system.

## Tech Stack
- **Frontend**: React.js, Redux, Bootstrap 5
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT (JSON Web Tokens)
- **Testing**: Jest, Mocha
- **Deployment**: Docker, AWS

## Data Models
1. **User**  
   - **Fields**:  
     - `id`: String (unique identifier)  
     - `username`: String  
     - `email`: String  
     - `password`: String  
     - `role`: String (admin/user)  

2. **Movie**  
   - **Fields**:  
     - `id`: String  
     - `title`: String  
     - `genre`: [String]  
     - `duration`: Number (in minutes)  
     - `releaseDate`: Date  
     - `rating`: Number  

3. **Booking**  
   - **Fields**:  
     - `id`: String  
     - `userId`: String (reference to User)  
     - `movieId`: String (reference to Movie)  
     - `bookingDate`: Date  
     - `seats`: Number  

## File Structure
```
Cinema-Forge/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── redux/
│   │   └── utils/
│   └── public/
│
├── backend/
│   ├── models/
│   ├── routes/
│   ├── controllers/
│   ├── middlewares/
│   └── config/
│
├── tests/
│   ├── frontend/
│   └── backend/
│
├── Dockerfile
├── docker-compose.yml
└── README.md
```  

## Conclusion
The selected tech stack and architectural design are aimed at providing a seamless user experience, efficient data management, and easy scalability as the application grows.