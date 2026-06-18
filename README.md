<div align="center">

# ✅ Todo List 

### A personal dashboard where you can log in, manage your to-do list, and check the weather — all in one place.

🔗 **[Video](https://drive.google.com/file/d/1gz44BAqBBFseQyRlyznZ0s59etuMC2R1/view?usp=sharing)**
🔗 **[Presentation Slide](https://docs.google.com/presentation/d/1_dh759QHrZ4paa9hS9C7uuUshbN8xZx3GkriJi7DGKE/edit?usp=sharing)**

<br>

![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Redux](https://img.shields.io/badge/Redux_Toolkit-593D88?style=for-the-badge&logo=redux&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=reactrouter&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![OpenWeather](https://img.shields.io/badge/OpenWeather-EB6E4B?style=for-the-badge&logo=openweathermap&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

</div>

---

## 📖 About

Productivity Dashboard is a web app that brings together a few everyday tools behind a single login. After signing in, users land on a dashboard where they can add and manage their to-do items, check the weather for any city, and view their profile. Authentication is handled by Firebase, to-dos are saved through a backend API, and weather data comes from OpenWeatherMap.

---

## ✨ Features

- 🔐 **Login & sign up** — Email/password and Google sign-in via Firebase Auth
- ✅ **To-do management** — Add, view, edit, and delete tasks with a title, content, and deadline
- 🌤️ **Weather lookup** — Search any city and see its current weather
- 📊 **Dashboard** — A central hub with a navbar to move between pages
- 👤 **Profile page** — View your account info
- 📱 **Responsive UI** — Built with React-Bootstrap for phone and desktop

---

## 🧩 Pages & Data

The app is organized into a few routed pages:

| Route | Page | Description |
|-------|------|-------------|
| `/login` | Login | Sign up or log in (email/password or Google) |
| `/dashboard` | Dashboard | View and manage your to-do list |
| `/weather` | Weather | Search a city and view current weather |
| `/profile` | Profile | View your account details |

Each to-do sent to the backend has this shape:

| Field | Type | Description |
|-------|------|-------------|
| `title` | string | Short name of the task |
| `content` | string | Details of the task |
| `deadline` | date | When the task is due |
| `user_id` | string | The owner of the task (from the auth token) |

> ℹ️ To-dos are stored through a **separate backend API** (not included in this repo). Weather data is fetched live from the **OpenWeatherMap API**.

---

## 🚀 Installation

### Prerequisites

- [Node.js](https://nodejs.org/) (v18 or higher)
- A [Firebase](https://firebase.google.com/) project (with Authentication enabled)
- A backend server that provides the to-do endpoints
- An [OpenWeatherMap API key](https://openweathermap.org/api)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/NKX0802/capstone-project.git
   cd capstone-project
   ```
2. **Install dependencies**
   ```bash
   npm install
   ```
3. **Set up environment variables** (see Configuration below)
4. **Run the development server**
   ```bash
   npm run dev
   ```
5. Open your browser at `http://localhost:5173`

---

## ⚙️ Configuration

Create a `.env` file in the root folder and add your Firebase keys:

```env
VITE_API_KEY=your_firebase_api_key
VITE_AUTH_DOMAIN=your_firebase_auth_domain
VITE_PROJECT_ID=your_firebase_project_id
VITE_STORAGE_BUCKET=your_firebase_storage_bucket
VITE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
VITE_APP_ID=your_firebase_app_id
```

You'll also need to set:

- The **to-do backend URL** (`BASE_URL` in `src/features/posts/postsSlice.js`)
- The **OpenWeatherMap API key** (currently in `src/components/WeatherPageMid.jsx`)

> ⚠️ **Never commit your `.env` file to GitHub.** Make sure `.env` is listed in your `.gitignore`. It's also a good idea to move the weather API key and backend URL into the `.env` file instead of hardcoding them.

---

## 🚸 How to Use

1. **Sign up / Sign in** with email and password, or with Google
2. **Add a to-do** — Enter a title, details, and deadline on the dashboard
3. **Manage to-dos** — Edit or delete tasks as needed
4. **Check the weather** — Go to the Weather page and search for a city
5. **View your profile** and log out when you're done

---

## 🐛 Future Improvements

- 🔑 **Move secrets to `.env`** — Keep the weather key and backend URL out of the source code
- ✔️ **Mark tasks complete** — Add a done/checked state for to-dos
- 🔔 **Deadline reminders** — Notify users when a task is due soon
- 📅 **Multi-day forecast** — Show more than just the current weather

---

## 📜 License

This project is licensed under the MIT License — feel free to use and modify it.
