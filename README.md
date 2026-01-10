# Event Management System (EMS) 👋

A full-stack Event Management System built with Expo React Native (frontend) and Node.js/Express (backend).

## Project Structure

```
EMS/
├── frontend/          # React Native/Expo app
│   ├── app/          # Expo Router pages (file-based routing)
│   ├── src/          # Source code
│   │   ├── features/ # Feature-based modules
│   │   └── shared/   # Shared components, hooks, utils
│   ├── components/   # Reusable components
│   ├── hooks/        # Custom React hooks
│   └── constants/    # App constants
│
├── backend/          # Node.js/Express API
│   └── src/
│       ├── features/ # Feature-based modules
│       └── shared/   # Shared models, middleware, config
│
└── docs/             # Documentation
```

## Getting Started

### Prerequisites

- Node.js (v18 or higher)
- npm or yarn
- MongoDB (for backend)
- Expo CLI (optional, but recommended)

### Installation

1. **Install all dependencies** (frontend + backend):

   ```bash
   npm run install:all
   ```

   Or install separately:
   ```bash
   # Frontend
   cd frontend && npm install

   # Backend
   cd backend && npm install
   ```

2. **Set up environment variables**:

   - Backend: Create `backend/.env` (see `ENV_SETUP.md`)
   - Frontend: Create `frontend/.env` (see `ENV_SETUP.md`)

### Running the Project

#### Option 1: Run from Root (Recommended)

```bash
# Run frontend only (same as before!)
npm start

# Run backend only
npm run start:backend

# Run both simultaneously
npm run dev
```

#### Option 2: Run from Individual Directories

```bash
# Frontend
cd frontend
npm start
# or
npx expo start

# Backend
cd backend
npm start
# or for development with auto-reload
npm run dev
```

## Development

### Frontend Development

The frontend uses Expo Router for file-based routing. Edit files in `frontend/app/` to create new screens.

- **Start development server**: `npm start` (from root) or `cd frontend && npm start`
- **Run on Android**: `npm run android` (from frontend directory)
- **Run on iOS**: `npm run ios` (from frontend directory)
- **Run on Web**: `npm run web` (from frontend directory)

### Backend Development

The backend uses Express.js with MongoDB. Features are organized in `backend/src/features/`.

- **Start server**: `npm run start:backend` (from root) or `cd backend && npm start`
- **Development mode** (with auto-reload): `cd backend && npm run dev`

### Adding New Features

Both frontend and backend follow a feature-based structure:

**Frontend Feature:**
```
frontend/src/features/[feature-name]/
├── components/
├── hooks/
├── services/
└── types/
```

**Backend Feature:**
```
backend/src/features/[feature-name]/
├── controllers/
├── routes/
├── services/
└── validators/
```

See `DIRECTORY_STRUCTURE.md` for detailed structure guidelines.

## Project Commands

### Root Level Commands

- `npm run install:all` - Install dependencies for frontend and backend
- `npm start` - Start frontend development server
- `npm run start:frontend` - Start frontend development server
- `npm run start:backend` - Start backend server
- `npm run dev` - Start both frontend and backend simultaneously

### Frontend Commands (from `frontend/` directory)

- `npm start` - Start Expo development server
- `npm run android` - Run on Android
- `npm run ios` - Run on iOS
- `npm run web` - Run on web
- `npm run lint` - Run ESLint

### Backend Commands (from `backend/` directory)

- `npm start` - Start server
- `npm run dev` - Start server with nodemon (auto-reload)

## Documentation

- [`DIRECTORY_STRUCTURE.md`](./DIRECTORY_STRUCTURE.md) - Detailed directory structure and organization
- [`QUICK_REFERENCE.md`](./QUICK_REFERENCE.md) - Quick reference guide
- [`RUN_COMMANDS.md`](./RUN_COMMANDS.md) - Detailed run commands documentation
- [`ENV_SETUP.md`](./ENV_SETUP.md) - Environment variables setup guide

## Tech Stack

### Frontend
- **Framework**: React Native with Expo
- **Routing**: Expo Router (file-based)
- **Language**: TypeScript
- **State Management**: React Hooks
- **HTTP Client**: Axios

### Backend
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT
- **Language**: JavaScript (Node.js)

## Contributing

1. Create a feature branch: `git checkout -b feature/your-feature-name`
2. Follow the feature-based directory structure
3. Make your changes
4. Test your changes
5. Submit a pull request

## Learn More

- [Expo Documentation](https://docs.expo.dev/)
- [Expo Router](https://docs.expo.dev/router/introduction)
- [Express.js](https://expressjs.com/)
- [MongoDB](https://www.mongodb.com/docs/)
