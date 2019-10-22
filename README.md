# Dependencies

express, dotenv, nodemon

# Routes

1. Create route logic in controllers/bootcamps.js

2. Create actual routes in routes/bootcamps.js

# Middleware

- Functions that have access to req, res cycle and can manage the logic between those two cycles.

The middleware will be used to validate a token that is sent in. If validated, then we set a user { req.user }. We then use that user to do Private functions within the API.

# Database

1. Setup MongoDB Atlas
2. Setup MongoDB Compass Desktop App
3. Connect the above
4. npm i mongoose
5. Create config/db.js

- Setup mongoose
- Add Compass App URI to config.env as an env variable
- Connect app to MongoDB
