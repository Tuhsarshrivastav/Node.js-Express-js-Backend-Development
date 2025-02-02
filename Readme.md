# Video Streaming API - Node.js

This is the backend API for a **Video Streaming App** built with **Node.js**. It provides essential features for handling user data, video streaming, tweets, subscriptions, comments, playlists, and file uploads. The API is designed to be highly scalable and efficient, built to handle real-time user interactions.

## 🚀 Features

- **User Authentication & Management:** Register, login, and manage users.
- **Video Upload & Streaming:** Upload and stream video content.
- **Tweets:** Users can post tweets related to videos.
- **Subscription:** Users can subscribe to channels for updates.
- **Comments:** Users can comment on videos.
- **Playlist Management:** Users can create and manage video playlists.
- **File Upload:** Handles file uploads with **Multer** for local storage and **Cloudinary** for cloud storage.

## 🛠️ Technologies Used

- **Node.js**: Backend runtime environment
- **Express.js**: Web framework for building APIs
- **MongoDB**: Database for storing user and video data
- **Mongoose**: ODM for MongoDB to define models and handle queries
- **JWT (JSON Web Token)**: For authentication and authorization
- **Multer**: Middleware for handling file uploads locally
- **Cloudinary**: For storing videos and images in the cloud
- **Bcrypt.js**: For hashing passwords

## 🏗️ API Structure

### Models

- **User Model**: Stores user information such as username, email, password, etc.
- **Video Model**: Stores video details such as title, description, file URL, etc.
- **Tweet Model**: Stores tweets posted by users related to videos.
- **Subscription Model**: Tracks subscriptions to video creators or channels.
- **Comment Model**: Stores user comments on videos.
- **Playlist Model**: Stores user-created playlists.

### Routes & Controllers

- **User Routes**: 
  - `POST /api/auth/register`: Register a new user
  - `POST /api/auth/login`: Login to an existing account
  - `GET /api/user/profile`: Get user profile details

- **Video Routes**:
  - `POST /api/videos/upload`: Upload a new video (with Multer and Cloudinary integration)
  - `GET /api/videos/:id`: Get a video by ID
  - `GET /api/videos/stream/:id`: Stream a video

- **Tweet Routes**:
  - `POST /api/tweets`: Create a tweet related to a video
  - `GET /api/tweets/:videoId`: Get tweets related to a specific video

- **Subscription Routes**:
  - `POST /api/subscription`: Subscribe to a channel
  - `GET /api/subscription/:userId`: Get user subscriptions

- **Comment Routes**:
  - `POST /api/comments`: Post a comment on a video
  - `GET /api/comments/:videoId`: Get comments for a specific video

- **Playlist Routes**:
  - `POST /api/playlist`: Create a playlist
  - `GET /api/playlist/:userId`: Get playlists for a user
  - `POST /api/playlist/add`: Add video to playlist

## ⚡ Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/video-streaming-api.git

