# 🍽️ SaloSalo — Budget-Based Meal Planner
**Capstone Project — OpenIT Summer Bootcamp 2026**
*Fullstack Development Track | MSEUF Lucena*

---

## 📖 Project Overview

**SaloSalo** is a full-stack web application that helps Filipino families and individuals plan their weekly meals while staying within a set budget. Users can browse recipes, filter them by category and cost, build a personalized weekly meal plan, and track their total spending — all in one place.

The name *SaloSalo* is a Filipino word meaning a communal gathering around food — fitting for an app built around sharing meals with the people you care about.

---

## ❗ The Problem

Many Filipino households struggle to plan meals in a way that is both nutritious and budget-conscious. Without a clear system, families often overspend on food or fail to plan ahead — leading to wasted ingredients and unbalanced meals.

**SaloSalo provides a simple, organized solution where the budget is always front and center.**

---

## ✅ Key Features

### 🔐 Authentication
- Register and log in securely with email and password
- Sessions persist using **HttpOnly cookies** — no need to log in again after refreshing the page
- All recipes and plans are tied to the user's account

### 🍳 Recipe Browser
- Browse a list of available recipes with estimated cost per serving (₱)
- Filter by meal category: **Breakfast, Lunch, Dinner, or Snack**
- Set a **weekly budget** — only recipes within that budget are shown automatically
- Add your own personal recipes with name, category, description, instructions, and cost

### 📅 Weekly Meal Planner
- A **Monday to Sunday table** showing all planned meals per day
- Add any recipe to any day of the week with one click
- Remove meals from the plan at any time
- Each day shows a **cost total** and meal count
- The **weekly total** is displayed at the top — turns red and warns you if you exceed your budget
- Shows exactly how much budget is **remaining** or how much **over** you are

### 🌙 Dark Mode
- Toggle between light and dark themes from the profile dropdown

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19, Vite, CSS |
| Backend | ASP.NET Core (.NET 10) |
| Authentication | ASP.NET Identity with HttpOnly Cookies |
| Database | PostgreSQL with Entity Framework Core |
| Icons | React Icons |
| API Communication | Fetch API with cookie credentials |

---

## 🏗️ Architecture

The app follows a clean **client-server architecture**:

- The **Frontend** (React) runs in the browser and handles everything the user sees and interacts with
- The **Backend** (ASP.NET Core) runs on the server and handles all data — saving users, recipes, and meal plans to the database
- They communicate through a **REST API** — the frontend sends HTTP requests, the backend responds with JSON data
- Security is handled through **cookies** — when you log in, the server sets a secure HttpOnly cookie the browser automatically sends with every future request

---

## 🚀 How to Run

### Backend
```bash
cd backend
dotnet restore
dotnet run
```
Runs on `http://localhost:5000`

### Frontend
```bash
cd frontend
npm install
npm run dev
```
Runs on `http://localhost:5173`

---

## 👥 Contributors

| Name | Role |
|---|---|
| **Kyla Dequito** | Backend Developer |
| **Lester Altamira** | Frontend Developer |

*Made during OpenIT's Summer Bootcamp 2026 (Fullstack Development Track) at MSEUF Lucena*

---

## 📌 Notes

- You must be **logged in** to use the Meal Planner and Plans pages
- The weekly plan is **automatically created** the first time you visit the Plans page
- Budget filtering happens **instantly in the browser** — no extra loading needed
- Meals added to the plan are saved to the **database** so they persist across sessions
