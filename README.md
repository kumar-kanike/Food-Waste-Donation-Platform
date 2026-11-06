# Food Waste Donation Platform

React + Node.js/Express + MongoDB application connecting food donors with NGOs and community groups to safely redistribute surplus food.

## Features
- Email/password authentication with bcrypt and JWT.
- Donors can list surplus food, quantity, pickup address and deadline.
- Signed-in users can browse available donations and claim a listing.
- Claimed donations are marked unavailable to prevent duplicate claims.
- MongoDB Atlas persistence.

## Stack
React, Vite, Node.js, Express, MongoDB Atlas, Mongoose.

## Database
`food_donation_db` — collections: `users`, `donations`, `claims`, `pickupRequests`.

## Run
Create an Atlas database user and allow the backend host IP. Copy `backend/.env.example` to `backend/.env`, set `MONGODB_URI` and a random 32+ character `JWT_SECRET`. Run `cd backend && npm install && npm run dev`; in another terminal run `cd frontend && npm install && npm run dev`. Open port 5173.

## Production gap
Add donor/NGO verification, food-safety checks, pickup coordination, expiry automation, moderation and audit logging before real-world use.
