# Cooking Masterclass Catalogue

## Project Overview
Cooking Masterclass Catalogue is a responsive, single-page prototype web application built with Vue.js. The application allows users to browse an interactive selection of upcoming cooking workshops hosted by expert chefs, see pricing, and track skill levels. 

This application serves as an interactive catalogue for food enthusiasts to explore available courses, track registration availability, and manage a real-time wishlist counter. It is designed as a standalone frontend layout to act as a foundation for future e-commerce features.

The application handles local data states to dynamically manage a real-time wishlist counter, tag "Sold Out" workshops, disable unavailable interactions, and allow users to filter listings to display available masterclasses instantly.

### Key Features Implemented
* **Dynamic Grid Layout:** Renders workshop cards dynamically from local data arrays without hardcoded duplicates.
* **Wishlist Counter:** A live counter in the application header tracks saved workshops.
* **Real-time Filtering:** Users can filter between viewing all courses or only currently available workshops.
* **Visual Availability States:** Clean "Sold Out" badges and conditional disabled buttons prevent interactions on fully booked sessions.
* **Responsive Styling:** Designed with CSS Grid and Flexbox to deliver a seamless layout

---

## Interface Preview

![main page image](https://i.ibb.co/zTYWXBNH/Cookiing-masterclass-catalogue.png)
---

## Tech Stack
**Framework:** Vue.js 
**Build Tool:** Vuex 
**Styling:** Custom CSS

---

## i. Installation and Run Instructions

Follow these step-by-step terminal commands to clone the source code, configure the project environment, and launch the development server locally on your machine:

### 1. Prerequisites
Ensure you have **Node.js** (version 16.0 or higher recommended) and **npm** installed on your system

### 2. Clone the Repository
git clone https://github.com/YOUR_GITHUB_USERNAME/cooking-masterclass-catalogue.git

### 3. Install Dependencies
cd cooking-masterclass-catalogue
npm install

### 4. Run the Application
npm run dev

### 5. Preview the Application
Once compilation completes successfully, hold down your keyboard's Ctrl key and click the local development URL address provided in the terminal output (typically http://localhost:5173/) to open and interact with your catalogue in your web browser!


