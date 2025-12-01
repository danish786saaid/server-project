# QuickNotes Project information 

A full-stack, self-hostable note-taking application built with Node.js, Express, MongoDB, and EJS templating.

#Course Name
the Server Side and Cloud Computing course 

#Course Code   S3810SEF

#Group   Group 31.

[🔗QuickNotes Demo🔗](https://server-project-14rn.onrender.com/)


## Collaborators

13696301 Saaid Danish

14187424 Ching Man Chung

14084841

# 🛠️ System Requirements

## Hardware & Software

- Computer with modern OS (macOS / Linux / Windows)
- Node.js (v14 or higher) installed and configured
- A web browser (Chrome, Firefox, Safari, Edge)
- Basic knowledge in command line operations
- Git installed 
- IDE or code editor (VS Code, WebStorm, Sublime Text, etc.)    

### API Services Required

- MongoDB API key Database connection string for data storage
- Unsplash API Access key (Optional) 
- High network bandwidth (If you want to host your own instance)

### Installation Links

For computers that do not have Node.js installed
Download **Node.js**: [here](https://nodejs.org/en)

For computers that do not have git installed
Download **Git**: [here](https://git-scm.com/)

## Set up

Step 1: Clone the Repository

Clone the repository to your computer using git:

    ```
    git clone https://github.com/danish786saaid/server-project.git

    ```

Step 2: Install Dependencies

Open the cloned folder in command line and install all required dependencies:

    ```
    npm i
    
    // Or you can use
    
    npm install
    ```

Step 3: Environment Configuration

Create a.env file in the root directory and configure your API keys:

   | Field |Description 
   |-------------------|-----------------------------------------------------|                                 
   | `MONGODB_URL`            | MongoDB backend for server data CURD access                                      |
   | `UNSPLASH_API_KEY`       | For accessing backdrop from Unsplash (Optional)                                  |

4. Run the application

    ```
    npm start

    ```

## Features

📝 Note Management
Create notes
Edit notes 
Delete notes 
Search note 
Organized layout 

🔐 Authentication System
1. Email Login
2. Email Sign-up 
3. Session management

🎨 User Interface
1. Dark / Light mode 
2. Responsive design 
3. Dynamic backgrounds
4. Clean interface

🔧 Technical Features
1. RESTful API 
2. Database integration( MongoDB with Mongoose ODM )
3. Real-time updates 
4. Error handling

📁 Project Documentation

#Project File Overview

[🔗See here (Link)🔗](docs/projectFileOverview.md)

## Operation Guide

[🔗See here (Link)🔗](docs/operationGuide.md)

## 📚 Libraries & Dependencies

### NPM Packages

|Package	      | Description|
|-------------------|-----------------------------------------------------|
|`express`      | Web application framework for Node.js|
|`mongoose`     | MongoDB object modeling for database `operations`|
|`ejs`      | Embedded JavaScript templating for views|
|`passport`      | Authentication middleware for Node.js|
|`express-session`	| Session management middleware|
|`bcryptjs`	| Password hashing and verification|
|`dotenv`		| Environment variable management|
|`node-fetch`	| HTTP request library for API calls|
|`uuid`		| Unique identifier generation|

### CDNs

| Package / Library | Description                                         |
|-------------------|-----------------------------------------------------|
| Google Font       | Typeface for the application                        |
| Bootstrap         | User Interface Framework and Icons                  |
| jQuery            | Fast, small, feature-rich JavaScript library        |
| Masonry           | Flexible, responsive, scalable grid system          |
| Unsplash          | Photography API                                     |

#Environment Variables

Ensure all required environment variables are set in your deployment platform:

Render.com, Heroku, Railway, or other cloud platforms

MongoDB Atlas for database hosting

Google Cloud Console for OAuth credentials

📄 License
This project is developed for educational purposes as part of the COMP S381F / S3810SEF course at HKMU.

🙏 Acknowledgments

HKMU - Server Side and Cloud Computing Course

Render - Cloud hosting platform for live demo

All team members - For collaboration and contribution


