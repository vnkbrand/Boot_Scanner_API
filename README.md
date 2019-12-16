# BootScanner API

Backend, full CRUD API for finding, creating, updating, reviewing bootcamps and courses.

## Initialize App

### Run in dev mode
npm run dev

### Run in prod mode
npm start

## Database Seeder

### Destroy all data
node seeder -d

### Import all data
node seeder -i

# API Specifications

## Bootcamps

### List all bootcamps in the database

### Search bootcamps by radius from zipcode
- Use a geocoder to get exact location and coords from a single address field
### Get single bootcamp

### Create new bootcamp
- Authenticated users 
- "publisher" or "admin"

### Upload photos
- Local upload

### Update bootcamps
- Authenticated users

### Delete Bootcamp
- Authenticated users

### Calculate the average cost of all courses

### Calculate the average rating from the reviews


## Courses

### List all courses for bootcamp

### List all courses for all bootcamps

### List single course

### Create a course
- Authenticated users
- "publisher" or "admin"
- Publishers can create >1 course

### Update course
- Authenticated users

### Delete course
- Authenticated users


## Reviews

### List all reviews for a single bootcamp

### List all reviews for all bootcamps

### List a single review

### Create a review
- Authenticated users
- "user" or "admin" (no publishers)

### Update review
- Authenticated users

### Delete review
- Authenticated users


## Users & Authentication
- Authentication is done through JWT/cookies
- JWT and cookie should expire in 30 days

### User registration
- Either register as a "user" or "publisher"
- Token sent alongside a cookie
- Passwords are hashed

### User login
- Email & Password
- Once hashed password validated, JWT & Cookie provided

### User logout
- Cookie will be sent to set token as 'none'.

### Get user
- Current logged-in user route

### Password reset
- Hashed token will be emailed to the users registered email address
A put request can be made to the generated url to reset password
The token will expire after 10 minutes

### Update user info
- Authenticated users
- Separate route to update password
- User CRUD
- Admin only
- Users can only be made admin by updating the database field manually
