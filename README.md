# ChatX 💬

A modern, real-time chat application built with React, Node.js, and Socket.io. ChatterFlux offers a seamless messaging experience with real-time communication, user authentication, and a beautiful, responsive UI.

## ✨ Features

- 🔐 **Secure Authentication** - JWT-based signup, login, and logout
- 💬 **Real-time Messaging** - Instant message delivery with Socket.io
- 🖼️ **Image Sharing** - Share images using Cloudinary integration
- 👥 **Online Status** - See who's online in real-time
- 📱 **Responsive Design** - Beautiful UI with DaisyUI and Tailwind CSS
- 🔔 **Toast Notifications** - User-friendly feedback with react-hot-toast
- 👤 **Profile Management** - Update profile pictures and user information
- 🎨 **Multiple Themes** - 30+ themes to choose from

## 🛠️ Tech Stack

### Frontend
- **React 19** - Modern UI library
- **Vite** - Fast build tool and development server
- **Tailwind CSS** - Utility-first CSS framework
- **DaisyUI** - Beautiful component library
- **Socket.io Client** - Real-time communication
- **Zustand** - State management
- **React Router DOM** - Client-side routing
- **Axios** - HTTP client
- **Lucide React** - Icon library

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Socket.io** - Real-time communication
- **MongoDB** - NoSQL database
- **Mongoose** - MongoDB object modeling
- **JWT** - Authentication tokens
- **Bcryptjs** - Password hashing
- **Cloudinary** - Image upload and storage
- **CORS** - Cross-origin resource sharing

## 🚀 Getting Started

### Prerequisites

- Node.js (v16 or higher)
- MongoDB database
- Cloudinary account (for image uploads)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd ChatX-main
   ```

2. **Install dependencies**
   ```bash
   npm run build
   ```

3. **Environment Variables**
   
   Create a `.env` file in the `Backend` directory:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
   CLOUDINARY_API_KEY=your_cloudinary_api_key
   CLOUDINARY_API_SECRET=your_cloudinary_api_secret
   NODE_ENV=development
   PORT=5001
   ```

4. **Run the application**
   
   **Development Mode:**
   ```bash
   # Backend (from Backend directory)
   cd Backend
   npm run dev
   
   # Frontend (from Frontend directory)
   cd Frontend
   npm run dev
   ```
   
   **Production Mode:**
   ```bash
   npm start
   ```

5. **Seed Database (Optional)**
   ```bash
   cd Backend
   node src/seeds/user.seed.js
   ```

## 📁 Project Structure

```
ChatterFlux-main/
├── Backend/
│   ├── src/
│   │   ├── controllers/     # Route controllers
│   │   ├── lib/            # Utilities (db, socket, cloudinary)
│   │   ├── middleware/     # Authentication middleware
│   │   ├── models/         # Database models
│   │   ├── routes/         # API routes
│   │   ├── seeds/          # Database seeding
│   │   └── index.js        # Server entry point
│   └── package.json
├── Frontend/
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── lib/           # Utilities and configurations
│   │   ├── pages/         # Page components
│   │   ├── store/         # State management
│   │   └── assets/        # Static assets
│   └── package.json
└── package.json           # Root package.json
```

## 🔧 API Endpoints

### Authentication
- `POST /api/auth/signup` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/logout` - User logout
- `GET /api/auth/check` - Check authentication status
- `PUT /api/auth/update-profile` - Update user profile

### Messages
- `GET /api/message/users` - Get all users for sidebar
- `GET /api/message/:id` - Get messages with specific user
- `POST /api/message/send/:id` - Send message to user

## 🔌 Socket Events

- `connect` - User connects to socket
- `disconnect` - User disconnects from socket
- `getOnlineUsers` - Get list of online users
- `newMessage` - Real-time message delivery

## 🎨 Themes

ChatterFlux supports 30+ themes including:
- Light & Dark modes
- Cupcake, Bumblebee, Emerald
- Corporate, Synthwave, Retro
- Cyberpunk, Valentine, Halloween
- And many more!

## 📱 Screenshots

*Add screenshots of your application here*

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

