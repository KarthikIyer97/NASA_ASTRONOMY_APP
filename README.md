# 🌌 NASA Astronomy Web Application 🚀  

A **full-stack web application** that provides insights into:  
- **Astronomy Picture of the Day (APOD)**
- **Near-Earth Object (NEO) Tracker**
- **Global Wildfire Tracking**  
with **interactive visualizations**, **real-time updates**, and a **responsive UI**.

---

## Table of Contents
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [Using the Application](#using-the-application)
- [Available Routes](#available-routes)
- [Future Improvements](#future-improvements)
- [Component Breakdown](#component-breakdown)


## 🌟 Features

### 🔥 Wildfire Tracker (Interactive Map with Filters)
- **Tracks global wildfire events** using **NASA’s EONET API**.
- **Real-Time Interactive Map**:
  - Uses **Leaflet.js** with **OpenStreetMap tiles**.
  - **Custom Fire Icons** indicate wildfire locations.
  - Clicking on a marker **shows wildfire details (name, date, coordinates)**.
- **Advanced Filtering System**:
  - **Filter by Year** (e.g., **2024, 2025, All**).
  - **Filter by Month** (last **6 months** dynamically generated).
  - **Filter by Country** (e.g., **USA, Australia, Brazil, India, etc.**).
- **Marquee Loading Animation**:
  - When the map loads, a **scrolling text animation** notifies users.
- **Fully Responsive**:
  - Works **seamlessly across all screen sizes**.
  - **Mobile-friendly sidebar** for filters.

### 🪐 Astronomy Picture of the Day (APOD) + Interactive Chatbot
- **Fetches NASA’s Astronomy Picture of the Day** from the **APOD API**.
- **Dynamic Background Image:**  
  - The **homepage updates daily** with NASA’s latest space image.  
  - **Brightness filter** enhances text readability.  
- **Read More Feature:**  
  - Users can **expand/collapse** the **APOD description** with an **animated effect**.  
  - **Scrollable modal** for long explanations.  
- **AI Chatbot (Powered by OpenAI)**:
  - Users can **ask astronomy-related questions**.  
  - **Quick Message Options**:
    - 🔭 **Astronomy Fact**
    - ✨ **Inspirational Space Quote**
    - ☄️ **Asteroid Information**
  - **Real-time AI responses**.  
  - **Smooth scrolling & typing indicator**.  
  - **Prevents main page scrolling when using chatbot**.  

### ☄️ Asteroid Tracker (NEO Tracker)
- Uses **NASA's NEO-WS API** to fetch asteroid data.
- **Dynamic 3D Coverflow Card Display**:
  - **Auto-scrolling NEO Cards** with **continuous rotation effect**.
  - Cards **flip and rotate** using **Framer Motion**.
- **Closest Approach Date Filter**:
  - Filters NEOs **by their nearest approach date**.
  - Requires selecting **Start Date** and **End Date** first.
  - **React Toastify Notifications** if no dates are selected.
- **Hazardous Asteroids Filter**:
  - View only **Potentially Hazardous Asteroids** (PHAs).
- **Interactive & Real-Time Dashboard**:
  - **Live charts** dynamically update when filters change.
  - **Bar, Pie, Line, Scatter, and Doughnut charts** for asteroid data.
  - **Velocity Distribution & Closest Approach Data Graphs**.
  - **Heatmap visualization** for size vs velocity.

---

## 🛠 Technologies Used

### 📌 **Frontend:**
- **React** (UI)
- **React-Router** (Navigation)
- **Framer Motion** (3D animations)
- **Chart.js** (Graphs & Visualizations)
- **Leaflet.js + React-Leaflet** (Interactive Map)
- **React Toastify** (Notifications)
- **Tailwind CSS** (Styling)
- **Chatbot UI Kit** (for chat interface)
- **React Icons** (LinkedIn, GitHub, and Portfolio links)

### 📌 **Backend:**
- **Node.js + Express.js** (Server)
- **Axios** (API Calls)
- **NASA APIs**:
  - **NEO-WS API** (Asteroid Data)
  - **APOD API** (Daily Astronomy Picture)
  - **EONET API** (Wildfire Events)
- **OpenAI API** (Chatbot Responses)

---


---

## Features

1. **Astronomy Picture of the Day (APOD)**: Displays the picture of the day and its description on the home screen using the APOD API.
2. **NEO Data**: Fetches and displays Near-Earth Objects approaching Earth using the NEO-WS API.
3. **Asteroid Visualization**: Displays charts (Bar, Pie, Line, and Scatter) showing asteroid size, hazardous status, and maximum diameter.
4. **Filters**: Allows users to filter NEO data by the nearest approach date and hazardous state.
5. **Background Image Carousel**: Automatically changes the background image on the homepage.
6. **Interactive Map**: Displays wildfire events on a world map using Leaflet.js. When the user hovers over the wildfire icons, a dialog box shows the title, location, and full date of the event.
7. **Responsive Design**: The app is fully responsive, adapting to different screen sizes across devices.

---


---

## Installation

### Prerequisites

- **Node.js**: Download and install Node.js from [nodejs.org](https://nodejs.org/).
- **npm**: Node Package Manager, which comes with Node.js.

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/NASA_ASTRONOMY_APP.git
Install frontend and backend dependencies: You will need to install the required packages in both the frontend and backend directories.

# Asteroid Tracker Web Application

## Installation

### Frontend:
    cd frontend
    npm install
  
### Backend:

    cd backend
    npm install
    
## Setting Up NASA API Keys
This project uses NASA’s APIs, so you need to obtain an API key.

Visit NASA API and sign up to get an API key.
After obtaining your key, create a .env file in the root of the backend directory:
```bash
NASA_API_KEY=your-nasa-api-key
```
### Running the Application
To run the application, follow these steps:

Install CORS (Cross-Origin Resource Sharing)
The frontend and backend need to communicate, so you’ll need to install CORS in the backend.

```bash
npm install cors
```

### Start the frontend:
```bash
cd frontend
npm run dev
```
### Start the backend:
```bash
cd backend
node server.js
```
Now the application should be running on:

Frontend: http://localhost:5173
Backend: http://localhost:5000

## 🚀 Using the Application

### 🔥 Wildfire Tracker (Interactive Map with Filters)
- **Tracks global wildfire events** using **NASA’s EONET API**.
- **Real-Time Interactive Map**:
  - Uses **Leaflet.js** with **OpenStreetMap tiles**.
  - **Custom Fire Icons** indicate wildfire locations.
  - Clicking on a marker **shows wildfire details**:
    - **Name**
    - **Date**
    - **Geographical coordinates**.
- **Advanced Filtering System**:
  - **Filter by Year** (e.g., **2024, 2025, All**).
  - **Filter by Month** (last **6 months dynamically generated**).
  - **Filter by Country** (e.g., **USA, Australia, Brazil, India, etc.**).
- **Marquee Loading Animation**:
  - When the map loads, a **scrolling text animation** notifies users.
- **Fully Responsive**:
  - Works **seamlessly across all screen sizes**.
  - **Mobile-friendly sidebar** for easy filtering.

---

### 🪐 Astronomy Picture of the Day (APOD) + Interactive Chatbot
- **Fetches NASA’s Astronomy Picture of the Day** from the **APOD API**.
- **Dynamic Background Image**:
  - The **homepage updates daily** with NASA’s **latest space image**.
  - **Brightness filter** enhances text readability.
- **Read More Feature**:
  - Users can **expand/collapse** the **APOD description** with an **animated effect**.
  - **Scrollable modal** for long explanations.
- **AI Chatbot (Powered by OpenAI)**:
  - Users can **ask astronomy-related questions**.
  - **Quick Message Options**:
    - 🔭 **Astronomy Fact**
    - ✨ **Inspirational Space Quote**
    - ☄️ **Asteroid Information**
  - **Real-time AI responses**.
  - **Smooth scrolling & typing indicator**.
  - **Prevents main page scrolling when using chatbot**.

---

### ☄️ Asteroid Tracker (NEO Tracker)
- Uses **NASA's NEO-WS API** to **fetch asteroid data**.
- **Dynamic 3D Coverflow Card Display**:
  - **Auto-scrolling NEO Cards** with **continuous rotation effect**.
  - **Cards flip and rotate smoothly** using **Framer Motion**.
- **Closest Approach Date Filter**:
  - Filters NEOs **by their nearest approach date**.
  - **Requires selecting Start Date and End Date first**.
  - **React Toastify Notifications** if no dates are selected.
- **Hazardous Asteroids Filter**:
  - View only **Potentially Hazardous Asteroids (PHAs)**.
- **Interactive & Real-Time Dashboard**:
  - **Live charts dynamically update when filters change**.
  - **Bar, Pie, Line, Scatter, and Doughnut charts** for asteroid data.
  - **Velocity Distribution & Closest Approach Data Graphs**.
  - **Heatmap visualization** for **size vs velocity**.

---

## Future Improvements
1) Pagination for Large Datasets: If the NEO dataset is large, implementing pagination or infinite scrolling could improve performance.
2) User Authentication: Allow users to save their preferences or track specific NEOs by adding user authentication.
3) New APIs and Visualizations: Integrate additional NASA APIs and create more visualizations.

## Component Breakdown
1. App.js
Purpose: Main entry point for the React application, managing route navigation and consistent elements like the Navbar and Footer.
2. Home.js
Purpose: Displays the Astronomy Picture of the Day (APOD) on the homepage.
Responsibilities: Fetches the daily picture and description using the APOD API.
3. AsteroidTracker.js
Purpose: Main component for tracking Near-Earth Objects (NEOs).
Responsibilities: Fetches NEO data, integrates filters, and visualizes asteroid data.
4. DatePicker.js
Purpose: Allows users to select a date range for filtering NEO data.
5. NeoFilters.js
Purpose: Filters NEOs based on their approach date and hazardous status.
6. NeoCard.js
Purpose: Displays details of individual NEOs, including size and approach date.
7. NeoCardContainer.js
Purpose: A carousel-like container for navigating between NEO cards.
8. NeoChart.js
Purpose: Renders charts visualizing NEO data using Chart.js.
9. NeoDetails.js
Purpose: Displays detailed information about a selected NEO in a modal.
10. NeoList.js
Purpose: Renders a list of filtered NEOs using NeoCardContainer.
11. Map.js
Purpose: Displays wildfire events on an interactive map using Leaflet.js.
12. Navbar.js
Purpose: Provides navigation links to different routes in the application.
13. Footer.js
Purpose: Displays a footer with information about the app.
Backend Components
14. server.js
Purpose: Main entry point for the backend, setting up the Express server and defining API routes for NEO, EONET, and APOD data.
15. apodRoutes.js, eonetRoutes.js, neoRoutes.js
Purpose: These route files handle API requests from the frontend and fetch data from NASA’s APIs.
16. apodController.js, eonetController.js, neoController.js
Purpose: Controllers for handling the actual logic for interacting with NASA's APIs using Axios.
17. .env
Purpose: Stores sensitive data like the NASA API key, keeping it out of the source code

