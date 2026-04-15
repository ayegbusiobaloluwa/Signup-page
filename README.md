# Signup/Login Application

A Node.js Express application with user authentication using MongoDB and bcrypt.

## Features
- User signup with email validation
- Secure password hashing with bcryptjs
- User login authentication
- Email notifications on signup (using Nodemailer)
- Dashboard for logged-in users

## Tech Stack
- **Backend**: Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: bcryptjs
- **Email**: Nodemailer
- **Template Engine**: EJS

## Setup

### Local Development
1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file (copy from `.env.sample`):
   ```
   MONGOURI=your_mongodb_connection_string
   PORT=2110
   ```
4. Start the server:
   ```bash
   npm start
   ```

## Environment Variables
- `MONGOURI` - MongoDB connection string
- `PORT` - Port to run the server (default: 2111)

## Deployment on Render

1. **Create a Render Account**
   - Go to [render.com](https://render.com)
   - Sign up and log in

2. **Connect GitHub Repository**
   - Click "New +" → "Web Service"
   - Connect your GitHub account
   - Select this repository

3. **Configure the Service**
   - **Name**: Choose any name (e.g., `signup-page`)
   - **Runtime**: Node
   - **Build Command**: `npm install`
   - **Start Command**: `npm start`

4. **Add Environment Variables**
   - Click "Environment"
   - Add the following variables:
     - `MONGOURI`: Your MongoDB connection string
     - `PORT`: 3000

5. **Deploy**
   - Click "Create Web Service"
   - Render will automatically deploy whenever you push to GitHub

## Important Notes
- `.env` file is not committed to Git for security
- MongoDB must be accessible from Render (whitelist 0.0.0.0/0 in MongoDB Atlas)
- Email notifications require valid credentials in nodemailer configuration

## Troubleshooting
- If deployment fails, check Render logs
- Ensure MongoDB URI is correct and accessible
- Make sure all environment variables are set in Render dashboard
