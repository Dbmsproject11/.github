# Component Interaction Manager

A **Flask + Supabase backend** with a **React frontend** to manage components and their interactions. Each component is assigned a **random unique 4-digit ID**. Interactions are stored in a **many-to-many relationship**, allowing flexible linking between components.

---

## Table of Contents

* [Features](#features)
* [Tech Stack](#tech-stack)
* [Project Structure](#project-structure)
* [Setup & Installation](#setup--installation)
* [Environment Variables](#environment-variables)
* [API Endpoints](#api-endpoints)
* [Frontend](#frontend)
* [Future Enhancements](#future-enhancements)

---

## Features

* Create and manage components with unique 4-digit IDs.
* Create interactions between components (many-to-many).
* View components along with all their interactions.
* React frontend for user-friendly interaction management.
* Flask backend with Supabase PostgreSQL for persistent storage.

---

## Tech Stack

* **Backend:** Flask, Supabase, Python 3.12
* **Frontend:** React + TypeScript
* **Database:** Supabase (PostgreSQL)
* **Other:** Flask-CORS, dotenv

---

## Project Structure

```
project-root/
│
├─ backend/
│  ├─ app.py               # Flask app with routes
│  ├─ requirements.txt     # Python dependencies
│  └─ .env                 # Supabase URL & key
│
├─ frontend/
│  ├─ src/
│  │  ├─ App.tsx
│  │  ├─ components/
│  │  │  ├─ AddInteraction.tsx
│  │  │  └─ ComponentList.tsx
│  │  └─ services/
│  │     └─ api.ts
│  └─ package.json
│
└─ README.md
```

---

## Setup & Installation

### Backend

1. Clone the repository:

```bash
git clone https://github.com/your-org/component-manager.git
cd component-manager/backend
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Create a `.env` file:

```env
url=YOUR_SUPABASE_URL
key=YOUR_SUPABASE_ANON_KEY
```

4. Run Flask:

```bash
python app.py
```

By default, it runs on `http://127.0.0.1:5000`.

---

### Frontend

1. Navigate to the frontend folder:

```bash
cd ../frontend
```

2. Install dependencies:

```bash
npm install
```

3. Run Vite:

```bash
npm run dev
```

By default, the frontend runs on `http://localhost:5173`.

---

## Environment Variables

The backend requires:

* `url` → Supabase project URL
* `key` → Supabase anon/public key

Store these in a `.env` file in the backend folder.

---

## API Endpoints

| Method | Endpoint        | Description                            |
| ------ | --------------- | -------------------------------------- |
| GET    | `/components`   | Retrieve all components & interactions |
| POST   | `/components`   | Add a new component with a 4-digit ID  |
| POST   | `/interactions` | Add an interaction between components  |

---

## Frontend

* Lists all components and their interactions.
* Allows creating new components.
* Allows creating interactions between components.
* Uses `apiService` to communicate with Flask backend.

---

## Future Enhancements

* Add authentication & roles.
* Add bulk import/export of components & interactions.
* Visualize interactions as a graph/network.
* Add search & filtering of components.
* Deploy backend to Render / frontend to Vercel for production use.

---


