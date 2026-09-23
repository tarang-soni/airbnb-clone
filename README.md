🏠 Airbnb Clone — Full Stack Web Application

A full-stack Airbnb-inspired accommodation booking platform developed as a team project. The application allows users to explore properties, search for stays, view property details, make bookings, and manage their reservations.

The project is built using React.js, Node.js, Express.js, and MongoDB and uses dummy/sample data for properties, users, bookings, and other application content.

«Note: This project is developed for educational and academic purposes. It is not affiliated with or connected to Airbnb.»

---

📌 Project Overview

The Airbnb Clone provides a simplified version of an accommodation booking platform where users can:

- Browse available properties
- Search properties based on location and other criteria
- View detailed property information
- Register and log in
- Select check-in and check-out dates
- Select the number of guests
- Make a simulated booking
- View their bookings
- Manage their profile

The application also provides functionality for hosts to manage their property listings.

---

🚀 Features

👤 User Features

- User registration and login
- User authentication
- Browse property listings
- Search and filter properties
- View property details
- View property images, price, amenities, and ratings
- Select check-in/check-out dates
- Select number of guests
- Create bookings
- View booking history
- Cancel bookings
- Add properties to wishlist

🏡 Host Features

- Host dashboard
- Add new property
- Update property details
- Delete property listings
- View property bookings
- Manage listed properties

💳 Booking

The project contains a simulated payment/booking flow for demonstration purposes.

No real payment gateway or financial transaction is implemented.

---

🛠️ Tech Stack

Frontend

- React.js
- JavaScript
- HTML5
- CSS3
- React Router
- Axios

Backend

- Node.js
- Express.js
- REST APIs

Database

- MongoDB
- Mongoose
- MongoDB Compass

Development Tools

- Visual Studio Code
- Git
- GitHub
- Postman
- npm

---

🏗️ System Architecture

                     AIRBNB CLONE
                          │
                          ▼
                    React Frontend
                          │
                    React Router
                          │
                        Axios
                          │
                          ▼
                    REST API Layer
                          │
                          ▼
                   Node.js + Express
                          │
                       Mongoose
                          │
                          ▼
                       MongoDB

Application Flow

User
 │
 ▼
React Frontend
 │
 ▼
Axios API Request
 │
 ▼
Express.js Backend
 │
 ▼
Mongoose
 │
 ▼
MongoDB
 │
 ▼
Response
 │
 ▼
React UI

---

📂 Project Structure

airbnb-clone/
│
├── frontend/
│   │
│   ├── public/
│   │
│   └── src/
│       ├── components/
│       │   ├── Navbar.jsx
│       │   ├── SearchBar.jsx
│       │   ├── PropertyCard.jsx
│       │   └── Footer.jsx
│       │
│       ├── pages/
│       │   ├── Home.jsx
│       │   ├── Login.jsx
│       │   ├── Register.jsx
│       │   ├── PropertyDetails.jsx
│       │   ├── Booking.jsx
│       │   ├── Wishlist.jsx
│       │   └── MyBookings.jsx
│       │
│       ├── services/
│       │   └── api.js
│       │
│       ├── data/
│       │   └── dummyData.js
│       │
│       ├── App.jsx
│       └── main.jsx
│       │
│       └── package.json
│
├── backend/
│   │
│   ├── controllers/
│   │   ├── userController.js
│   │   ├── propertyController.js
│   │   └── bookingController.js
│   │
│   ├── models/
│   │   ├── User.js
│   │   ├── Property.js
│   │   └── Booking.js
│   │
│   ├── routes/
│   │   ├── userRoutes.js
│   │   ├── propertyRoutes.js
│   │   └── bookingRoutes.js
│   │
│   ├── middleware/
│   │   └── authMiddleware.js
│   │
│   ├── config/
│   │   └── db.js
│   │
│   ├── server.js
│   └── package.json
│
└── README.md

---

🗄️ Database Collections

The application uses MongoDB with collections such as:

Users

Stores user information.

User
├── name
├── email
├── password
├── phone
└── role

Roles can include:

guest
host

Properties

Stores property listing information.

Property
├── title
├── description
├── location
├── city
├── pricePerNight
├── guests
├── bedrooms
├── bathrooms
├── amenities
├── images
├── rating
└── hostId

Bookings

Stores booking information.

Booking
├── userId
├── propertyId
├── checkIn
├── checkOut
├── guests
├── totalAmount
└── status

---

🔌 API Endpoints

Property APIs

Method| Endpoint| Description
GET| "/api/properties"| Get all properties
GET| "/api/properties/:id"| Get property by ID
POST| "/api/properties"| Create property
PUT| "/api/properties/:id"| Update property
DELETE| "/api/properties/:id"| Delete property

User APIs

Method| Endpoint| Description
POST| "/api/users/register"| Register a user
POST| "/api/users/login"| Login user
GET| "/api/users/profile"| Get user profile

Booking APIs

Method| Endpoint| Description
POST| "/api/bookings"| Create booking
GET| "/api/bookings"| Get user bookings
GET| "/api/bookings/:id"| Get booking details
DELETE| "/api/bookings/:id"| Cancel booking

«API endpoints may be updated as the project develops.»

---

📊 Dummy Data

This project uses dummy/sample data for development and demonstration.

Example property:

{
  "title": "Luxury Apartment in Pune",
  "location": "Kharadi, Pune",
  "pricePerNight": 2500,
  "guests": 4,
  "bedrooms": 2,
  "bathrooms": 2,
  "rating": 4.7
}

Sample destinations may include:

- Pune
- Mumbai
- Goa
- Delhi
- Bangalore
- Hyderabad
- Jaipur
- Manali

No real customer, payment, or private Airbnb data is used.

---

⚙️ Installation & Setup

1. Clone the Repository

git clone https://github.com/<your-username>/<repository-name>.git

cd airbnb-clone

2. Setup Frontend

cd frontend
npm install

Start the React development server:

npm run dev

3. Setup Backend

Open another terminal:

cd backend
npm install

Start the backend server:

npm run dev

or:

node server.js

4. Configure Environment Variables

Create a ".env" file inside the backend directory.

PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key

«Do not upload your ".env" file or database credentials to GitHub.»

---

🧪 API Testing

Backend APIs can be tested using Postman.

Example:

GET http://localhost:5000/api/properties

The API returns property information in JSON format.

---

🔐 Security

The project follows basic security practices such as:

- Password protection
- Authentication
- JWT-based authorization
- Protected API routes
- Environment variables for sensitive configuration
- Input validation

---

🖥️ Application Workflow

                    START
                      │
                      ▼
                  Home Page
                      │
             ┌────────┴────────┐
             │                 │
          Register           Login
             │                 │
             └────────┬────────┘
                      │
                      ▼
                Search Property
                      │
                      ▼
               Property Listing
                      │
                      ▼
              Property Details
                      │
                      ▼
               Select Dates
                      │
                      ▼
              Select Guests
                      │
                      ▼
                Reserve Stay
                      │
                      ▼
            Simulated Payment
                      │
                      ▼
             Booking Confirmed
                      │
                      ▼
                My Bookings

---

👥 Team Collaboration

The project is developed collaboratively using Git and GitHub.

Typical development responsibilities include:

- Frontend / React development
- Backend / REST API development
- Database design and integration
- Authentication
- Booking functionality
- Testing and debugging
- UI/UX development

Team members work through Git branches and pull requests before merging changes into the main branch.

---

🔮 Future Enhancements

The project can be extended with:

- Real payment gateway integration
- Google Maps / Mapbox integration
- Cloud image storage
- Advanced property filtering
- Reviews and ratings
- Host analytics dashboard
- Real-time chat
- Email notifications
- Property availability calendar
- Deployment to cloud platforms
- Recommendation system

---

📸 Screenshots

Screenshots of the application will be added here as the project progresses.

Coming Soon

---

🎓 Project Purpose

This project was developed as part of a Full Stack Development academic project to gain practical experience in:

- Frontend development with React
- Backend development with Node.js and Express
- REST API development
- MongoDB database management
- Authentication and authorization
- Git/GitHub collaboration
- Full-stack application architecture



You may modify and use the code for learning and academic purposes.
