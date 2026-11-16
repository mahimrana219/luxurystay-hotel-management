<div align="center">

# 🏨 LuxuryStay: Hotel Management System

### A complete hotel operations platform with 4 staff portals and a guest booking website

Online booking, walk-in reservations, room status tracking, billing, housekeeping, maintenance, staff management and reports, all role-based.

![React](https://img.shields.io/badge/React_19-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-404D59?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

![Admin Dashboard](screenshots/admin-dashboard.jpg)

</div>

---

## ✨ What it does

LuxuryStay runs the whole hotel from one system: guests book online, the front desk handles walk-ins, housekeeping keeps rooms ready, and management sees everything in live dashboards and reports.

### 👥 Role-based portals

| Role | Key features |
|---|---|
| **🛡️ Admin** | Dashboard, reports, full CRUD for rooms, staff and services, bookings overview, guest feedback & contacts, maintenance resolution, system settings |
| **📊 Manager** | Dashboard, reports, staff & services overview, maintenance reporting, guest feedback & contacts |
| **🛎️ Receptionist** | Walk-in guest + booking in one flow, booking status management, room availability, billing & invoices, maintenance reporting |
| **🧹 Housekeeping** | Cleaning task board, "Mark Available" room workflow, maintenance reporting |
| **🧳 Guest** | Register/login, browse & book rooms, manage/cancel bookings, view & pay invoices, payment confirmation email, feedback |

### 🔄 Smart room & booking lifecycle

```
Booking: pending → confirmed → checked-in → checked-out
Room:    Available → Occupied → Cleaning → Available
```
- Online bookings start as **pending** until the receptionist confirms them; walk-ins are **confirmed** instantly
- Check-in marks the room **Occupied**, check-out sends it to **Cleaning**, and housekeeping returns it to **Available**
- After check-out the receptionist generates the bill
- Walk-in guests automatically receive a **set-your-password email**

## 📸 Screenshots

| Guest website | About & rooms |
|---|---|
| ![Landing](screenshots/landing.jpg) | ![About](screenshots/about.jpg) |

| Room inventory | Bookings registry |
|---|---|
| ![Rooms](screenshots/room-inventory.jpg) | ![Bookings](screenshots/bookings-registry.jpg) |

| Walk-in reservation | Billing & invoices |
|---|---|
| ![Walk-in](screenshots/walk-in-booking.jpg) | ![Invoices](screenshots/billing-invoices.jpg) |

| Staff directory | Hotel services |
|---|---|
| ![Staff](screenshots/staff-directory.jpg) | ![Services](screenshots/services.jpg) |

| Manager dashboard | Housekeeping dashboard |
|---|---|
| ![Manager](screenshots/manager-dashboard.jpg) | ![Housekeeping](screenshots/housekeeping-dashboard.jpg) |

| Guest feedback |
|---|
| ![Feedback](screenshots/guest-feedback.jpg) |

## 🛠️ Tech stack

- **Frontend:** React 19, Vite, Tailwind CSS, React Router 7, Axios, Lucide icons, React Toastify
- **Backend:** Node.js, Express, MongoDB, JWT authentication with role-based authorization, email notifications
- **Auth:** separate guest and staff (management) login flows, password reset and set-password links

## 🏗️ Project structure

```
src/
├── Admin/          # Admin portal: dashboard, rooms, staff, services, reports, settings
├── Manager/        # Manager portal and reports
├── Receptionist/   # Front desk: bookings, walk-ins, invoices, availability
├── Housekeeping/   # Cleaning tasks and room status
├── Registration/   # Login, register, booking, profile, password flows
├── Components/     # Guest website sections (hero, rooms, FAQ, reviews…)
├── Pages/          # Guest website pages
└── api/            # Axios instance with JWT interceptor
```

## 🚀 Run locally

```bash
git clone https://github.com/mahimrana219/luxurystay-hotel-management.git
cd luxurystay-hotel-management
cp .env.example .env    # set VITE_API_URL to your backend
npm install
npm run dev
```

> ℹ️ This repository contains the **frontend**. The backend API (Node.js, Express, MongoDB) is kept private.

---

<div align="center">

**Mahim Rana** · Full-Stack Developer

[Portfolio](https://mahimrana-portfolio.vercel.app/) · [LinkedIn](https://www.linkedin.com/in/mahimrana219/) · [GitHub](https://github.com/mahimrana219)

</div>
