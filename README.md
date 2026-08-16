# UniLink

A social networking platform built for university students and lecturers to share ideas, collaborate, and communicate.

![Status](https://img.shields.io/badge/status-beta-yellow)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Initial Setup](#initial-setup)
  - [Running the App](#running-the-app)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

UniLink is a full-stack social networking platform designed specifically for university communities — giving students and lecturers a shared space to post updates, exchange ideas, and communicate in real time, separate from general-purpose social networks.

It was built as a personal project to explore full-stack development with a real-time communication layer, combining a React frontend with an Express/Node.js backend, MySQL for persistence, WebSockets for live features, and JWT-based authentication.

## Screenshots

<!-- Add screenshots here once available, e.g.: -->
<!-- ![Home Feed](resources/screenshots/home-feed.png) -->
<!-- ![Profile Page](resources/screenshots/profile.png) -->

*(Screenshots coming soon)*

## Features

- User authentication (JWT-based sign up / login)
- Social feed for posting and sharing updates
- Real-time communication via WebSockets
- Separate roles for students and lecturers
- Profile management
- MySQL-backed persistent storage

*(Update this list to match the actual current feature set as the project evolves.)*

## Tech Stack

**Frontend**
- React
- Vite
- JavaScript / HTML / CSS

**Backend**
- Node.js
- Express.js
- WebSockets
- JWT (authentication)

**Database**
- MySQL

## Architecture

```
┌─────────────────┐        HTTP / REST        ┌──────────────────┐
│   React Frontend  │ ─────────────────────────▶ │  Express Backend   │
│   (Vite, :5173)    │ ◀─────────────────────────  │  (Node.js, :8080)  │
│                    │                              │                    │
│                    │        WebSocket             │                    │
│                    │ ◀────────────────────────▶  │                    │
└─────────────────┘                              └──────────────────┘
                                                            │
                                                            ▼
                                                   ┌──────────────────┐
                                                   │   MySQL Database   │
                                                   │   (localhost:3306) │
                                                   └──────────────────┘
```

## Getting Started

### Prerequisites

- Node.js and npm
- MySQL server (running locally on port `3306`)

### Initial Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/denethp/unilink.git
   cd unilink
   ```
2. Install backend dependencies:
   ```bash
   cd code/backend
   npm i
   ```
3. Install frontend dependencies:
   ```bash
   cd ../frontend
   npm i
   ```
4. Create a `config.env` file inside the `backend` directory with the required environment variables (database credentials, JWT secret, etc.).

### Running the App

1. Start your local MySQL server on port `3306`.
2. In the `backend` directory:
   ```bash
   npm start
   ```
3. In the `frontend` directory:
   ```bash
   npm run dev
   ```
4. The app will be served at [http://localhost:5173](http://localhost:5173).

> **Note:** Ensure no other services are running on ports `5173` and `8080` before starting.

## Project Structure

```
.
├── code/
│   ├── backend/          # Express.js API server, MySQL models, WebSocket handling
│   └── frontend/         # React (Vite) client application
├── resources/             # Supporting assets (design files, screenshots, docs)
├── CONTRIBUTING.md
└── README.md
```

*(Update this structure if the actual folder layout inside `code/` differs.)*

## Contributing

Contributions, issues, and feature requests are welcome. Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines before submitting a pull request.

## License

This repository is shared for portfolio and demonstration purposes. Please check the repository's license file or contact the author before reusing any part of this codebase.

---

*Built by Deneth Priyadarshana.*
