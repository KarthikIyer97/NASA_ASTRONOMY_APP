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

## 🌟 Features  

### 🪐 Astronomy Picture of the Day (APOD)  
- Fetches and displays the **daily astronomy image** from **NASA's APOD API**.  
- Includes a **detailed description** explaining the significance of the image.  
- Updates automatically **every 24 hours**.  

### ☄️ Near-Earth Object (NEO) Data  
- Retrieves real-time data on **asteroids approaching Earth** using **NASA’s NEO-WS API**.  
- Displays key details such as **size, velocity, approach date, and hazardous status**.  

### 📊 Asteroid Data Visualization  
- Provides **interactive charts** to analyze asteroid properties:  
  - **Bar Chart** – Compares asteroid sizes.  
  - **Pie Chart** – Highlights hazardous vs. non-hazardous asteroids.  
  - **Line Chart** – Tracks asteroid size variations over time.  
  - **Scatter Plot** – Displays asteroid **size vs. velocity** for pattern analysis.  

### 🎯 Advanced Filtering System  
- **Closest Approach Date Filter** – Users can filter NEOs by their **nearest approach date** within a **7-day range**.  
- **Hazardous Status Filter** – View only **potentially hazardous asteroids** for better risk assessment.  
- **Real-time updates**: Filtering dynamically updates the displayed asteroid data and charts.  

### 🌌 Dynamic Background Image Carousel  
- The homepage features a **rotating background image** that updates automatically **every 5 seconds**.  
- Creates an immersive space-themed experience with high-quality images.  

### 🌍 Interactive Wildfire Tracker  
- Uses **NASA’s EONET API** to **map wildfire events across the globe**.  
- **Leaflet.js Interactive Map:**  
  - Displays wildfire locations with **hover tooltips** for details.  
  - Clicking an event provides **full information**, including **title, location, and event date**.  

### 📱 Fully Responsive & Mobile-Friendly  
- **Seamless experience** across **all devices** (desktop, tablet, mobile).  
- UI adapts to different screen sizes **without compromising usability**.  
- **Optimized for performance** to ensure smooth rendering across platforms.  


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


### OpenAI API Key Setup (For Chatbot)
Get an API Key:

Sign up at OpenAI
Generate a new API key from the API settings.
Add the OpenAI API key to your .env file in the backend directory:

.env file
```bash
OPENAI_API_KEY=your-openai-api-key
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
# 🚀 Available Routes

The application provides the following routes:

| **Route**               | **Description** |
|-------------------------|----------------|
| `/`                     | Home - Displays Astronomy Picture of the Day (APOD) & Chatbot. |
| `/asteroidtracker`      | Near-Earth Object (NEO) Tracker with filters and visualizations. |
| `/map`                  | Global Wildfire Map (EONET API) for tracking wildfire events. |

---
## 📌 Future Improvements  
The **Asteroid Tracker Web Application** is already packed with powerful features, but there’s always room for enhancement. Below are some planned improvements:

### 🚀 1. Pagination & Infinite Scrolling for Large Datasets  
- **Issue:** Currently, all asteroid data for the selected range is loaded at once.  
- **Solution:** Implement **pagination** or **infinite scrolling** to optimize performance and improve user experience.  

### 🔐 2. User Authentication & Preferences Storage  
- **Allow users to:**  
  - Save their **favorite NEOs**.  
  - Customize **filters & dashboard views**.  
  - Track specific asteroids over time.  
- **Implementation:** Integrate **Firebase/Auth0** for authentication and use **MongoDB/PostgreSQL** to store user data.  

### 📊 3. More NASA APIs & Data Integrations  
- **Expand the application with additional space-related data:**  
  - **Exoplanet Exploration API** – View planets outside our solar system.  
  - **Mars Rover Photos API** – Fetch the latest images from Mars rovers.  
  - **NASA Weather Data** – Get real-time space weather insights.  

### 🌓 4. Dark Mode Support  
- **Current State:** The UI follows a light-themed design.  
- **Future Update:** Add a **toggle button** for **Dark Mode** using Tailwind CSS dark mode utilities.  

### 📅 5. Calendar-Based NEO Selection  
- **Enhancement:** Improve date selection by integrating a **calendar-based UI** instead of a manual date picker.  
- **Goal:** Provide a more user-friendly experience when selecting a date range.  

### 🌍 6. Multi-Language Support  
- **Why?** Expand accessibility for a global audience.  
- **How?** Implement **i18n (Internationalization)** with language options like **English, Spanish, French, Hindi, etc.**  

### 📡 7. Live NEO Tracking & Push Notifications  
- **Real-Time Alerts:** Allow users to set alerts when **a potentially hazardous asteroid** is approaching Earth.  
- **Implementation:** Use **WebSockets or Firebase Cloud Messaging (FCM)** to push notifications.  

### 🎨 8. Improved 3D Visualizations  
- **Upgrade:** Enhance the **3D coverflow effect** with **Three.js or D3.js** for better asteroid visualizations.  
- **Goal:** Provide a more immersive and interactive way to explore asteroid data.  

### 📍 9. Asteroid Impact Simulation  
- **New Feature:** A **simulation tool** where users can input an asteroid’s size & velocity to see potential impact scenarios.  
- **Visualization:** Use **real-time physics-based models** to simulate impact effects.  

### 🧠 10. AI-Powered Asteroid Predictions  
- **Machine Learning Integration:**  
  - Use historical asteroid data to **predict future NEO approaches**.  
  - Display **risk assessment scores** to indicate potential asteroid threats.  
- **Implementation:** Train an AI model on past NEO data and visualize **predicted asteroid trajectories**.  

These improvements will significantly enhance the **user experience, scalability, and real-time insights** of the Asteroid Tracker Application. 🚀✨  


---

# 🏗 Component Breakdown

## 🌟 **Frontend Components**
| **Component**          | **Purpose** |
|-----------------------|-------------|
| `App.js`             | Main entry point for the React application, managing route navigation and shared elements like the Navbar and Footer. |
| `Home.js`            | Displays Astronomy Picture of the Day (APOD) with chatbot integration. Fetches daily images from NASA’s APOD API. |
| `AsteroidTracker.js` | Main component for tracking Near-Earth Objects (NEOs). Fetches NEO data, applies filters, and visualizes asteroid insights. |
| `DatePicker.js`      | Allows users to select a date range for filtering NEO data. |
| `NeoFilters.js`      | Filters NEOs based on their approach date and hazardous status. |
| `NeoCard.js`        | Displays individual NEOs with details like size, velocity, and closest approach date. |
| `NeoCardContainer.js` | A carousel-style container for navigating between NEO cards. |
| `NeoChart.js`       | Renders data visualizations (Bar, Pie, Line, Scatter, Doughnut) using **Chart.js**. |
| `NeoDetails.js`     | Displays detailed information about a selected NEO in a modal view. |
| `NeoList.js`        | Lists and renders filtered NEOs using `NeoCardContainer.js`. |
| `Map.js`            | Displays wildfire events on an interactive world map using **Leaflet.js**. |
| `Navbar.js`         | Provides navigation links to different routes in the application. |
| `Footer.js`         | Displays footer content with project and developer details. |

---

## ⚙️ **Backend Components**
| **File**               | **Purpose** |
|------------------------|-------------|
| `server.js`           | Main entry point for the backend, setting up **Express.js server** and managing API endpoints. |
| `apodRoutes.js`       | Handles requests related to NASA's **APOD API** to fetch the Astronomy Picture of the Day. |
| `eonetRoutes.js`      | Fetches wildfire event data from NASA’s **EONET API** and serves it to the frontend. |
| `neoRoutes.js`        | Manages API calls related to Near-Earth Objects (NEOs) using NASA’s **NEO-WS API**. |
| `chatbotRoutes.js`    | Routes chatbot interactions and connects with **OpenAI API** to generate responses. |

### 🔍 **Controllers**
| **File**                | **Purpose** |
|-------------------------|-------------|
| `apodController.js`    | Fetches **Astronomy Picture of the Day (APOD)** and formats data for the frontend. |
| `eonetController.js`   | Handles **wildfire event tracking** and processes data from NASA’s EONET API. |
| `neoController.js`     | Manages fetching and processing of **NEO data**, including filtering and hazardous asteroid tracking. |
| `chatbotController.js` | Manages AI chatbot responses using **OpenAI’s GPT API**, providing real-time astronomy insights. |

---

# 🚀 **Full NASA App Deployment**
The application has been **fully deployed**, allowing users to explore:
- **Live asteroid tracking** via NASA’s NEO-WS API.
- **Daily space images** from APOD.
- **Wildfire monitoring** using EONET API.
- **An AI chatbot** that provides astronomy insights.

**Stay tuned for future enhancements!** 🚀

---

## 🔐 **Environment Variables & API Keys**
For the application to work, ensure that your `.env` file (in the `backend` directory) contains:

```env
# NASA API Key for fetching space data
NASA_API_KEY=your-nasa-api-key

# OpenAI API Key for AI chatbot responses
OPENAI_API_KEY=your-openai-api-key
