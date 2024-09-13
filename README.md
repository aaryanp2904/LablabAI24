
# Next.js & Flask Full-Stack Application

This project is a full-stack web application consisting of a **Next.js frontend** and a **Flask backend**. The frontend interacts with the backend via RESTful API calls. This guide will help you set up the project on your local machine.

## Prerequisites

Before you begin, ensure you have the following installed on your machine:

- [Node.js](https://nodejs.org/en/) (v14.x or higher)
- [Python 3.x](https://www.python.org/)
- [Git](https://git-scm.com/)
- [npm](https://www.npmjs.com/)

## Project Structure

```bash
root/
├── flask-backend/       # Flask backend
│   ├── app.py           # Main backend script
│   └── requirements.txt # Python dependencies
├── nextjs-frontend/     # Next.js frontend
│   ├── package.json     # Node.js dependencies
│   ├── src/             # Frontend source files
│   └── .env             # Environment variables for Next.js
└── .gitignore           # Ignored files for Git
```

## Setup Instructions

### 1. Clone the Repository

First, clone the repository and navigate into the project directory:

```bash
git clone https://github.com/your-username/your-repository-name.git
cd your-repository-name
```

### 2. Setting Up the Flask Backend

Next, you'll set up the **Flask backend**. Navigate into the `flask-backend` directory and follow the steps below.

#### a. Create and Activate a Virtual Environment

On **Linux/MacOS**:

```bash
cd flask-backend
python3 -m venv venv
source venv/bin/activate
```

On **Windows**:

```bash
cd flask-backend
python -m venv venv
venv\Scripts\activate
```

#### b. Install Backend Dependencies

```bash
pip install -r requirements.txt
```

If you encounter CORS issues, install and configure `flask-cors`:

```bash
pip install flask-cors
```

#### c. Run the Flask Backend

```bash
python app.py
```

The Flask backend will now be running at `http://localhost:5000/`.

### 3. Setting Up the Next.js Frontend

Navigate to the `nextjs-frontend` directory:

```bash
cd ../nextjs-frontend
```

#### a. Install Frontend Dependencies

```bash
npm install
```

#### b. Run the Next.js Development Server

```bash
npm run dev
```

By default, the Next.js app will be running at `http://localhost:3000/`.

### 4. Environment Variables

#### Flask Backend

Create a `.env` file in the `flask-backend/` directory. Example content:

```bash
FLASK_APP=app.py
FLASK_ENV=development
```

#### Next.js Frontend

Create a `.env.local` file in the `nextjs-frontend/` directory. Example content:

```bash
NEXT_PUBLIC_API_URL=http://localhost:5000
```

### 5. Running the Full Application

To run the full application, you need to have both the **Flask backend** and the **Next.js frontend** running simultaneously.

#### Running the Flask Backend:

```bash
python app.py
```

#### Running the Next.js Frontend:

```bash
npm run dev
```

#### Port Conflicts

If a server fails to start due to a port conflict, modify the port settings in either the Flask or Next.js configuration.

### 7. License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Key Sections in the README:

1. **Prerequisites**: Lists necessary tools and versions.
2. **Project Structure**: Overview of the key files and folders in the project.
3. **Setup Instructions**: Provides clear steps to clone the repository, set up both the Flask backend and Next.js frontend, install dependencies, and run both applications.
4. **Environment Variables**: Explains where to configure `.env` files for both backend and frontend.
5. **Running the Full Application**: Instructions to run both backend and frontend servers together.
6. **Additional Notes**: Highlights things like CORS and possible future steps for production readiness.

This file should provide enough guidance for anyone pulling the project to set it up on their local machine!
