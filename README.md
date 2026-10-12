# Full Stack Task Manager

A task and reminder app built for my M.Sc. Computer Science software engineering module (2024). Users create an account, log in, and manage tasks with a reminder time and a status of *remaining* or *completed*.

![React](https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-5-646CFF?logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-Express-339933?logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb&logoColor=white)

## Features

- Sign up and log in with **JWT** authentication; passwords are hashed with **bcrypt**
- Create, edit, complete and delete tasks, each with a description and reminder time
- Separate views for all, remaining and completed tasks
- Protected routes on both the frontend (React context) and the API (auth middleware)

## Architecture

```
frontend/   React 18 + Vite, React Router, MUI, Tailwind CSS, react-toastify
api/        Node.js + Express REST API, Mongoose models, JWT middleware
            MongoDB (Atlas or local) for users and tasks
```

### API endpoints

| Method | Route | Purpose |
|---|---|---|
| POST | `/register` | Create an account |
| POST | `/login` | Log in, returns a JWT |
| GET | `/validate-token` | Check the current session |
| GET | `/tasks` | List the user's tasks |
| GET | `/tasks/remaining` · `/tasks/completed` | Filter by status |
| GET | `/tasks/:taskId` | Get one task |
| POST | `/tasks` | Create a task |
| PUT | `/tasks/edit/:taskId` | Edit a task |
| PUT | `/tasks/status` | Mark complete or remaining |
| POST | `/tasks/delete` | Delete a task |

## Run it locally

```bash
# API
cd api
cp .env.example .env      # then fill in your own values
npm install
npm start                 # http://localhost:4000

# Frontend (second terminal)
cd frontend
npm install
npm run dev               # http://localhost:5173
```

## Author

**Manicharan Ravi** · Software Engineer, Cloud & Full Stack · Mainz, Germany
[LinkedIn](https://linkedin.com/in/manicharan-ravi) · [GitHub](https://github.com/manicharan0485)
