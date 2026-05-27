# backend-intro
# Backend Intro API

A intro to backend project built with **Node.js**, **Express.js**, **MongoDB**, and **Mongoose**.  
This project practices creating API routes, connecting to a database, hashing passwords, and testing requests with Postman.

## Tech Stack

- JavaScript
- Node.js
- Express.js
- MongoDB Atlas
- Mongoose
- bcrypt
- dotenv
- nodemon
- Postman

## Features

- Register user
- Login user
- Logout user
- Hash passwords with bcrypt
- Create posts
- Get all posts
- Update posts by ID
- Delete posts by ID

## Project Structure

```txt
backend-intro/
├── package.json
├── .env
├── .gitignore
└── backend/
    └── src/
        ├── index.js
        ├── app.js
        ├── config/
        │   ├── database.js
        │   └── constants.js
        ├── models/
        │   ├── user.model.js
        │   └── post.model.js
        ├── controllers/
        │   ├── user.controller.js
        │   └── post.controller.js
        └── routes/
            ├── user.route.js
            └── post.route.js
Setup
Install dependencies:
npm install
Create a .env file in the root folder:
PORT=4000
MONGODB_URI=your_mongodb_connection_string
DB_NAME=intro_to_backend
Start the server:
npm run dev
Server runs locally at:
http://localhost:4000
API Routes
User Routes
Base URL:
/api/v1/users
Method	Route	Description
POST	/register	Register a new user
POST	/login	Log in a user
POST	/logout	Log out a user
Example register body:
{
  "username": "olivia",
  "email": "olivia@example.com",
  "password": "123456"
}
Post Routes
Base URL:
/api/v1/posts
Method	Route	Description
POST	/create	Create a post
GET	/getPosts	Get all posts
PATCH	/update/:id	Update a post by ID
DELETE	/delete/:id	Delete a post by ID
Example post body:
{
  "name": "oliver",
  "description": "belongs in a jar",
  "age": 21
}
What I Learned
This project helped me understand the basic backend request flow:
Postman/client → Express app → route → controller → Mongoose model → MongoDB → JSON response
I learned how to:
Structure a Node/Express backend
Use routes and controllers
Connect MongoDB Atlas with Mongoose
Store secret values in .env
Hash passwords before saving them
Test API endpoints in Postman
Debug common backend errors
