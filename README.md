# Login Authentication System

## 📌 Project Overview
A complete client‑side authentication system featuring user registration, login validation, and a protected dashboard. Built with HTML5, CSS3, and vanilla JavaScript, it includes password hashing using SHA‑256, duplicate user checks, session management with localStorage, and a clean, responsive interface.

## 🛠️ Tech Stack
- **HTML5** – Semantic structure
- **CSS3** – Flexbox, custom properties, responsive design
- **JavaScript (Vanilla)** – DOM manipulation, localStorage, Web Crypto API (SHA‑256 hashing)
- **Font Awesome** – Icons for visual enhancement
- **Google Fonts** – Inter typeface

## ✅ Features Implemented
### Core Features
- [x] Registration page with username, email, password, and Register button
- [x] Password validation – minimum 8 characters and at least 1 number
- [x] Duplicate username/email check – displays error if user already exists
- [x] Login page with email, password, and Login button
- [x] Incorrect credential handling – generic error message (doesn't reveal which field is wrong)
- [x] Protected dashboard – only accessible after successful login
- [x] Redirect to login page if dashboard is accessed directly without a session
- [x] Logout button – clears session and redirects to login

### Security Features
- [x] Passwords are **not stored in plain text** – hashed using SHA‑256 via Web Crypto API
- [x] No sensitive data exposed – generic error messages
- [x] Session stored securely in localStorage

### User Experience
- [x] Auto‑redirect after successful registration/login
- [x] Clear success and error messages with icons
- [x] Smooth page transitions
- [x] Fully responsive – works on desktop and mobile

## 🔐 How Authentication Works

### Registration
1. User submits username, email, and password
2. Password is validated (min 8 chars + at least 1 number)
3. System checks for duplicate username/email
4. Password is hashed using SHA‑256 (via `crypto.subtle`)
5. User data is stored in `localStorage` under `auth_users`

### Login
1. User submits email and password
2. System finds user by email
3. Entered password is hashed and compared with stored hash
4. On success, a session is created in `localStorage` (`auth_session`)
5. User is redirected to the dashboard

### Dashboard (Protected)
1. On load, the system checks for an active session
2. If no session exists, redirects to login
3. If session exists but user was deleted, session is cleared
4. Displays user's name and avatar (first letter)

### Logout
1. Clears the session from `localStorage`
2. Redirects to login page

## 🎨 Design Highlights
- Clean, minimal interface with a modern colour palette
- Smooth transitions between pages
- Responsive design – adapts to mobile screens
- Clear visual feedback with colour‑coded messages (success, error, info)

## 👩‍💻 Author
**Mudupu Sravya**  
- [GitHub](https://github.com/MudupuSravyaReddy)  
- [LinkedIn](https://www.linkedin.com/in/sravya-mudupu-8860a3389)

## 📅 Date
02 September 2026
