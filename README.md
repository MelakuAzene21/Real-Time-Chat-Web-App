# 💬 Real-Time Chat Web Application

A modern, full-stack real-time chat application built with the MERN stack, featuring instant messaging, user authentication, and a beautiful responsive UI.

![License](https://img.shields.io/badge/license-ISC-blue.svg)
![Node](https://img.shields.io/badge/node-%5E20.0.0-brightgreen.svg)
![React](https://img.shields.io/badge/react-18.2.0-blue.svg)

## ✨ Features

- 🔐 **User Authentication** - Secure login and registration with JWT
- 💬 **Real-Time Messaging** - Instant message delivery using Socket.io
- 👥 **One-on-One Chat** - Private conversations with other users
- 👀 **Typing Indicators** - See when someone is typing
- 🎨 **Modern UI** - Beautiful interface built with React, Chakra UI, and Tailwind CSS
- 😊 **Emoji Support** - Express yourself with emoji picker
- 📱 **Responsive Design** - Works seamlessly on desktop and mobile devices
- 🔔 **Real-Time Notifications** - Get notified of new messages instantly
- 🔒 **Secure** - Password hashing with bcrypt and JWT authentication

## 🛠️ Tech Stack

### Frontend
- **React** 18.2.0 - UI library
- **Redux Toolkit** - State management
- **Chakra UI** - Component library
- **Tailwind CSS** - Utility-first CSS framework
- **Socket.io Client** - Real-time communication
- **React Router** - Navigation
- **Axios** - HTTP client
- **Framer Motion** - Animations
- **React Toastify** - Toast notifications
- **Emoji Mart** - Emoji picker

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **MongoDB** - Database
- **Mongoose** - ODM for MongoDB
- **Socket.io** - Real-time bidirectional communication
- **JWT** - Authentication tokens
- **bcryptjs** - Password hashing
- **CORS** - Cross-origin resource sharing
- **dotenv** - Environment variables

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v20.0.0 or higher)
- **npm** or **yarn**
- **MongoDB** (local installation or MongoDB Atlas account)

## 🚀 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/MelakuAzene21/Real-Time-Chat-Web-App.git
cd Realtime-Chat
```

### 2. Install Root Dependencies

```bash
npm install
```

### 3. Setup Server

```bash
cd server
npm install
```

Create a `.env` file in the `server` directory with the following variables:

```env
PORT=8000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
BASE_URL=http://localhost:3000
NODE_ENV=development
```

**Environment Variables Explanation:**
- `PORT` - Port number for the server (default: 8000)
- `MONGODB_URI` - Your MongoDB connection string
- `JWT_SECRET` - Secret key for JWT token generation
- `BASE_URL` - Frontend URL for CORS configuration
- `NODE_ENV` - Environment mode (development/production)

### 4. Setup Client

```bash
cd ../clients
npm install
```

Create a `.env` file in the `clients` directory (if needed):

```env
REACT_APP_API_URL=http://localhost:8000
```

## 🏃 Running the Application

### Development Mode

You need to run both the server and client simultaneously.

**Terminal 1 - Start the Server:**
```bash
cd server
npm start
```
The server will run on `http://localhost:8000`

**Terminal 2 - Start the Client:**
```bash
cd clients
npm start
```
The client will run on `http://localhost:3000`

### Production Build

**Build the Client:**
```bash
cd clients
npm run build
```

## 📁 Project Structure

```
Realtime-Chat/
├── clients/                 # React frontend
│   ├── public/             # Public assets
│   ├── src/
│   │   ├── apis/           # API service functions
│   │   ├── components/     # Reusable React components
│   │   ├── pages/          # Page components
│   │   ├── redux/          # Redux slices and actions
│   │   ├── utils/          # Utility functions
│   │   ├── App.js          # Main App component
│   │   ├── index.js        # Entry point
│   │   └── store.js        # Redux store configuration
│   └── package.json
│
├── server/                  # Node.js backend
│   ├── controllers/        # Request handlers
│   ├── middleware/         # Custom middleware
│   ├── models/             # Mongoose models
│   ├── mongoDB/            # Database connection
│   ├── routes/             # API routes
│   ├── index.js            # Server entry point
│   └── package.json
│
├── .babelrc                # Babel configuration
├── .prettierrc             # Prettier configuration
├── .gitignore              # Git ignore rules
├── License.md              # License file
├── package.json            # Root package.json
└── README.md               # This file
```

## 🔑 Key Features Explained

### Real-Time Communication
The application uses Socket.io to establish WebSocket connections between clients and the server, enabling:
- Instant message delivery
- Typing indicators
- Online/offline status
- Real-time notifications

### Authentication Flow
1. User registers with email and password
2. Password is hashed using bcryptjs
3. JWT token is generated upon successful login
4. Token is stored and sent with subsequent requests
5. Middleware validates token for protected routes

### State Management
Redux Toolkit is used for efficient state management:
- User authentication state
- Active chats and messages
- UI state (modals, notifications)
- Real-time updates

## 🎨 UI Components

The application features a modern, intuitive interface with:
- **Login/Register Pages** - Clean authentication forms
- **Chat List** - View all your conversations
- **Chat Window** - Real-time messaging interface
- **User Search** - Find and start conversations
- **Profile Management** - Update user information
- **Emoji Picker** - Express emotions in messages

## 🔒 Security Features

- Password hashing with bcryptjs
- JWT-based authentication
- HTTP-only cookies (if implemented)
- CORS configuration
- Input validation and sanitization
- Protected API routes

## 🧪 Testing

```bash
# Run tests (when implemented)
npm test
```

## 🐛 Troubleshooting

### Common Issues

**MongoDB Connection Error:**
- Ensure MongoDB is running
- Check your `MONGODB_URI` in `.env`
- Verify network access if using MongoDB Atlas

**Port Already in Use:**
- Change the `PORT` in server `.env` file
- Kill the process using the port: `npx kill-port 8000`

**Socket.io Connection Failed:**
- Ensure server is running
- Check CORS configuration
- Verify the Socket.io client URL matches server URL

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the ISC License - see the [License.md](License.md) file for details.

## 👨‍💻 Author

**Shakir Farhan**

## 🙏 Acknowledgments

- Socket.io for real-time communication
- MongoDB for the database
- React community for amazing libraries
- All contributors and users of this project

## 📧 Contact & Support

For issues, questions, or suggestions:
- Open an issue on [GitHub Issues](https://github.com/ShakirFarhan/Realtime-Chat/issues)
- Contact the maintainer

## 🚧 Roadmap

Future enhancements planned:
- [ ] Group chat functionality
- [ ] File and image sharing
- [ ] Voice and video calls
- [ ] Message reactions
- [ ] Message search
- [ ] Dark mode
- [ ] Push notifications
- [ ] Message encryption
- [ ] User presence status
- [ ] Read receipts

---

**Made with ❤️ using the MERN Stack**
