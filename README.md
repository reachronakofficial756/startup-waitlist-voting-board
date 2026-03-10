# 🚀 Startup Waitlist & Feature Voting Board

A simple **full-stack application** that simulates a **startup pre-launch landing page** where users can:

* Join a **product waitlist**
* Vote for upcoming **product features**
* See features **automatically ranked by popularity**

This project demonstrates **basic full-stack development concepts** including form handling, REST APIs, vote aggregation, and dynamic UI updates.

---

# 📌 Project Overview

Many startups collect user interest **before launching a product**.

This application replicates that process:

1. Users enter their **email to join the waitlist**
2. Users can **upvote features they want**
3. Features are **sorted automatically by vote count**

Example:

| Feature    | Votes |
| ---------- | ----- |
| Dark Mode  | 12    |
| API Access | 8     |
| Mobile App | 5     |

---

# ✨ Features

* 📧 **Waitlist Registration**
  Users can submit their email to join the product waitlist.

* 👍 **Feature Voting**
  Users can upvote upcoming product features.

* 📊 **Automatic Sorting**
  Features are dynamically sorted by vote count.

* ⚡ **Fast UI Updates**
  The feature list refreshes after every vote.

* 🧩 **Simple REST API Architecture**

---

# 🛠 Tech Stack

## Frontend

* **Next.js**
* Client Components
* Fetch API
* Basic form validation

## Backend

* **Node.js**
* **Express.js**
* REST API structure

## Database

* **JSON file (mock database)**

Used for simplicity to store:

* Waitlist emails
* Feature vote counts

---

# 📂 Project Structure

```
startup-waitlist-voting-board
│
├── backend
│   ├── server.js
│   ├── routes
│   │   ├── waitlist.js
│   │   └── features.js
│   │
│   ├── controllers
│   │   ├── waitlistController.js
│   │   └── featureController.js
│   │
│   └── db
│       └── db.json
│
├── frontend
│   ├── app
│   │   └── page.js
│   │
│   └── components
│       ├── WaitlistForm.jsx
│       └── FeatureBoard.jsx
│
└── README.md
```

---

# 🔌 API Endpoints

## Join Waitlist

**POST**

```
/waitlist
```

Body:

```json
{
  "email": "user@example.com"
}
```

Adds the email to the waitlist.

---

## Get Features

**GET**

```
/features
```

Returns the list of features sorted by votes.

Example response:

```json
[
  {
    "id": 1,
    "name": "Dark Mode",
    "votes": 10
  }
]
```

---

## Upvote Feature

**POST**

```
/features/:id/upvote
```

Example:

```
/features/1/upvote
```

Increments the vote count of a feature.

---

# 💻 Running the Project Locally

## 1️⃣ Clone the repository

```
git clone https://github.com/your-username/startup-waitlist-voting-board.git
```

```
cd startup-waitlist-voting-board
```

---

## 2️⃣ Start Backend

```
cd backend
```

Install dependencies

```
npm install
```

Run server

```
npm run dev
```

Backend runs on:

```
http://localhost:5000
```

---

## 3️⃣ Start Frontend

Open new terminal.

```
cd frontend
```

Install dependencies

```
npm install
```

Run frontend

```
npm run dev
```

Frontend runs on:

```
http://localhost:3000
```

---

# 🎯 Learning Goals

This project helps practice:

* Building **REST APIs with Express**
* Handling **form submissions**
* Implementing **vote counters**
* Sorting data dynamically
* Connecting **Next.js frontend with backend APIs**
