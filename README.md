# Career Spark App

A React application for Career Spark - Entertainment Pathways.

## Authors
- Mahitha
- Pancham
- Ruudra

https://github.com/user-attachments/assets/b2910712-0df3-4882-b6cd-4ae0d406d3c4


## 📋 Table of Contents
- [Features](#-features)
- [Prerequisites](#%EF%B8%8F-prerequisites)
- [Installation](#-getting-started)
  - [Frontend Dependencies](#frontend-dependencies)
  - [Backend Dependencies](#backend-dependencies-python)
- [Running the App](#-running-the-app)
- [Environment Variables](#-environment-variables)
- [AWS Setup](#-aws-setup)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

## 📄 License

This project is licensed under the GNU Affero General Public License v3.0 - see the [LICENSE](LICENSE) file for details.

Key points:
- Free to use, modify, and distribute
- Any modifications must be open source
- Applies to network/server use
- Must include original copyright and license

## 🌟 Features

- **AI-Powered Career Guidance**: Get personalized career recommendations in the entertainment industry
- **Interactive Assessments**: Complete personality and skills assessments
- **Virtual Experience**: Simulate different career roles
- **Mentor Chatbot**: Get career advice from AI mentors
- **Peer Recommendations**: Connect with peers in your field of interest

## 🛠️ Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Python 3.8 or higher
- pip (Python package manager)
- AWS Account (for S3 storage)

## 🚀 Getting Started

#### Frontend Dependencies
Dependencies are already installed. If you need to reinstall:

```bash
npm install
```

#### Backend Dependencies (Python)
Install Python dependencies:

```bash
pip install -r backend/requirements.txt
```

Or if you prefer using a virtual environment (recommended):

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r backend/requirements.txt
```

### Running the App

#### Option 1: Run Frontend and Backend Together (Recommended)
```bash
npm run dev:all
```

This will start both the Python backend server (port 3001) and the Vite dev server (port 5173).

#### Option 2: Run Separately

**Backend Server (Python):**
```bash
npm run server
# or directly: python3 backend/server.py
```

**Frontend Dev Server:**
```bash
npm run dev
```

The app will be available at `http://localhost:5173` (or another port if 5173 is in use).

### Backend Configuration

The Python backend uses the same `.env` file as the Node.js backend. Make sure you have:

```env
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
AWS_REGION=us-east-1
S3_BUCKET=user-persona-data
S3_FOLDER=test-user
PORT=3001
```

### Building for Production

```bash
npm run build
```

The built files will be in the `dist` directory.

### Preview Production Build

```bash
npm run preview
```

## Backend

The backend has been migrated from Node.js/Express to Python/Flask. The Python backend (`backend/server.py`) provides the same API endpoints:

- `POST /api/upload` - Upload files and text to S3
- `GET /api/health` - Health check endpoint

The old Node.js backend (`server.js`) is still available. To use it instead, run:
```bash
npm run server:node
```

