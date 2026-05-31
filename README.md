# Wedding-rsvp
# 💍 Serverless Wedding RSVP Web Application

A production-ready, high-performance static web application built to streamline guest management, event scheduling, and real-time response tracking. This site is fully deployed and actively serving real-world users.

## 🚀 Live Demo
[👉 Click here to view the live application](YOUR_DEPLOYED_GITHUB_PAGES_LINK_HERE)

## 🛠️ Tech Stack
* **Frontend:** HTML5, Tailwind CSS (via CDN), Google Fonts API
* **Javascript:** Vanilla JS (ES6+) for DOM manipulation and asynchronous networking
* **Backend Infrastructure:** Serverless architecture utilizing Google Apps Script (GAS)
* **Database/Ledger:** Google Sheets API for real-time data persistence

## ✨ Key Engineering & Architecture Features

### 1. Serverless Cloud Integration
Instead of provisioning a heavy, expensive server instance (like Node.js or Express) for a temporary event, the application leverages a **completely serverless architecture**. The frontend handles form processing and pipes the data directly into a Google Apps Script microservice endpoint via an asynchronous fetch request.

### 2. Asynchronous Network Handling & CORS Workaround
* Utilizes the browser `Fetch API` combined with `FormData` and `URLSearchParams` to format data packages into standard URL-encoded payloads.
* Implements a strategic `mode: 'no-cors'` configuration within the fetch request to bypass cross-origin browser limitations when communicating directly with Google’s script macro environment.

### 3. Dynamic UI Layouts & Event-Driven DOM Manipulation
* **Conditional Field Rendering:** Includes an event-driven listener tracking radio button input configurations, dynamically showing or hiding layout nodes (such as the guest count input matrix) based on the user's specific registration lifecycle context.
* **Aspect-Ratio Constraints:** Implements a calculated JavaScript window layout tracking engine (`resizeFrame`) that measures client text widths and programmatically calculates responsive visual aspect ratios for critical media containers on the fly.

### 4. Advanced Performance Optimization & Fluid Animations
* Leverages Tailwind CSS utility classes to achieve ultra-fast paint cycles and minimize layout shifts (CLS).
* Utilizes keyframe-driven CSS `@keyframes fadeIn` animations coupled with a programmatic JavaScript iteration loop to introduce staggered element entrance delays, maximizing visual aesthetic without freezing the main rendering thread.

## 📁 Project Architecture & Files
* `index.html` — Core application layout structure, components, styles, and script drivers.
* `logo2.png` / `marin2.jpg` — Static image assets optimized for web performance.
