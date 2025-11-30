# Project files overview

### Structure

```
├── README.md
├── models
│   │   ├── Note.js
│   │   ├── User.js
│   │   ├── noteEntrySchema.js
│   │   └── userSchema.js
├── .gitignore
├── .gitignore~
├── Notable.zip
├── package-lock.json
├── package.json
├── public
│   ├── images
│   │   └── background.jpeg
│   ├── style.css
├── server.js
└── views
│   │   └──partials
│   │      └──footer.ejs
│   │      └──header.ejs
│   │      └──layout.ejs
|   ├── homepage.ejs
|   ├── login.ejs
|   └── signup.ejs

```

*Excluding folder from “node_modules” and "docs" folder

### server.js

This is the place where all the server side operation and route for the client handled.

It handles the CURD of the MongoDB database for user and note and more, for instance:

🔌 API Endpoints

Web Routes
- GET / - Root redirect (to login or homepage)
- GET /login - Login page rendering
- GET /signup - Registration page rendering
- POST /signup - User registration processing
- POST /login - User authentication
- GET /homepage - Main application interface
- GET /logout - User session termination

Note Operations
- POST /notes - Create new note
- POST /notes/edit/:id - Update existing note
- GET /notes/delete/:id - Delete note

REST API Endpoints
- GET /api/notes - Retrieve all notes (JSON format)
- GET /api/notes/:id - Retrieve specific note
- POST /api/notes - Create new note via API
- PUT /api/notes/:id - Update note via API
- DELETE /api/notes/:id - Delete note via API

Utility Routes
- GET /background - Get random background image from Unsplash
- GET /auth/google - Google OAuth initiation
- GET /auth/google/callback - Google OAuth callback processing

### package.json

Dependencies used:

```
{
  "name": "notable",
  "version": "1.0.0",
  "description": "Group Project for COMPS381F / COMPS3810SEF",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "private": true,
  "author": "",
  "license": "ISC",
  "dependencies": {
    "bcryptjs": "^2.4.3",
    "dotenv": "^16.4.5",
    "ejs": "^3.1.10",
    "express": "^4.21.1",
    "express-session": "^1.18.1",
    "mongoose": "^8.8.1",
    "node-fetch": "^2.7.0",
    "passport": "^0.7.0",
    "passport-google-oauth20": "^2.0.0",
    "uuid": "^11.0.2"
  },
  "devDependencies": {
    "nodemon": "^3.0.1"
  }
}

```

### public

```
├── public
│   ├── images
│   │   └── background.jpeg
│   ├── style.css

```

### views

```
└── views
│   │   └──partials
│   │      └──footer.ejs
│   │      └──header.ejs
│   │      └──layout.ejs

```

Place where all the page structure is defined

### models

```
├── models
│   │   ├── Note.js
│   │   ├── User.js
│   │   ├── noteEntrySchema.js
│   │   └── userSchema.js
```

### docs
```
├── docs
│   ├── images
│   │   └── Create-Note.png
│   │   └── Invalidinput1.png
│   │   └── Invalidinput2.png
│   │   └── login.png
│   │   └── showcase.png
│   │   └── signUp-failed1.png
│   │   └── signUp.png
│   ├── operationGuide.md
│   ├── projectFileOverview.md
```

Place where the blueprint of the data-structure of the MongoDB Database backend structure are defined