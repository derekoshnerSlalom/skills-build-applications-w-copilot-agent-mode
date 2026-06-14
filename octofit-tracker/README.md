# OctoFit Tracker

A modern multi-tier application for fitness tracking with GitHub Copilot agent mode.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite application
│   ├── src/
│   ├── package.json
│   ├── vite.config.js
│   └── index.html
└── backend/           # Node.js + Express + TypeScript API
    ├── src/
    ├── package.json
    ├── tsconfig.json
    └── .env.example
```

## Technology Stack

### Frontend
- **React 19** - UI library
- **Vite 5** - Build tool and dev server
- **Port**: 5173

### Backend
- **Node.js** - Runtime
- **Express 4** - Web framework
- **TypeScript** - Type safety
- **Mongoose 8** - MongoDB ODM
- **Port**: 8000

### Database
- **MongoDB** - NoSQL database
- **Port**: 27017

## Getting Started

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- MongoDB (local or Atlas connection string)

### Frontend Setup

```bash
cd octofit-tracker/frontend
npm install
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd octofit-tracker/backend
npm install
cp .env.example .env
npm run dev
```

The backend will be available at `http://localhost:8000`

### MongoDB Connection

Update the `MONGODB_URI` in `.env`:
```
MONGODB_URI=mongodb://localhost:27017/octofit-tracker
```

Or use MongoDB Atlas:
```
MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/octofit-tracker
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint

### Backend
- `npm run dev` - Start development server with ts-node
- `npm run build` - Compile TypeScript to JavaScript
- `npm run start` - Run compiled application
- `npm run lint` - Run ESLint

## API Endpoints

- `GET /api/health` - Health check endpoint

## Development

Both frontend and backend support hot module reloading during development:

1. Start MongoDB
2. Start backend: `npm run dev` from `backend/`
3. Start frontend: `npm run dev` from `frontend/`
4. Open `http://localhost:5173` in your browser

## License

MIT
