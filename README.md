# SaloSalo - Budget-Based Meal Planner

Capstone Project - OpenIT Summer Bootcamp 2026
Fullstack Development Track | MSEUF Lucena

---

## Project Overview

SaloSalo is a full-stack web application that helps Filipino families and individuals plan their weekly meals while staying within a set budget. Users can browse recipes, filter them by category and cost, build a personalized weekly meal plan, and track their total spending.

The name SaloSalo is a Filipino word meaning a communal gathering around food, representing an application built around sharing meals.

---

## The Problem

Many Filipino households struggle to plan meals in a way that is both nutritious and budget-conscious. Without a clear system, families often overspend on food or fail to plan ahead, leading to wasted ingredients and unbalanced meals.

SaloSalo provides a simple, organized solution where the budget is always front and center.

---

## Key Features

### Authentication
* Register and log in securely with email and password
* Sessions persist using HttpOnly cookies to maintain state across page refreshes
* All recipes and plans are tied to the user account

### Recipe Browser
* Browse available recipes with estimated cost per serving in PHP
* Filter by meal category: Breakfast, Lunch, Dinner, or Snack
* Set a weekly budget to automatically display recipes within price constraints
* Add custom recipes with name, category, description, instructions, and cost

### Weekly Meal Planner
* Monday through Sunday grid display showing all planned meals per day
* Add any recipe to any day of the week with one click
* Remove meals from the plan at any time
* Daily cost total and meal count breakdowns
* Weekly total tracker with warnings when exceeding the set budget
* Dynamic calculation of remaining budget or over-budget amounts

### Interface Customization
* Toggle between light and dark themes from the profile menu

---

## Tech Stack

| Layer | Technology |
| :--- | :--- |
| **Frontend** | React 19, Vite, CSS |
| **Backend** | ASP.NET Core (.NET 10) |
| **Authentication** | ASP.NET Identity with HttpOnly Cookies |
| **Database** | PostgreSQL with Entity Framework Core |
| **Icons** | React Icons |
| **API Communication** | Fetch API with cookie credentials |

---

## Architecture

The application follows a client-server architecture:

* **Frontend:** Built with React to handle UI rendering and user interactions in the browser.
* **Backend:** Built with ASP.NET Core to handle data operations, user sessions, recipes, and meal plans.
* **Communication:** REST API endpoints using JSON payloads.
* **Security:** HttpOnly session cookies managed automatically by the browser for authenticated requests.

---

## How to Run

### Backend

1. Navigate to the backend directory:
   ```bash
   cd backend

2. Restore dependencies:
   ```bash
   dotnet restore
   
3. Start the server:
   ```bash
   dotnet run
Runs on http://localhost:5000

### Frontend

1. Navigate to the frontend directory:
   ```bash
   cd frontend

2. Install dependencies:
   ```bash
   npm install
   
3. Start the development server:
   ```bash
   npm run dev
Runs on http://localhost:5173
