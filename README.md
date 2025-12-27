
# 🚀 AI Website Generator

An **AI-powered full-stack web application** that enables users to generate, manage, preview, and version websites using AI.  
The platform follows a **SaaS-style architecture** with authentication, project management, AI integration, and extensible payment support.

🔗 **Live Demo:** https://site-builder-two.vercel.app

---

## 🧠 Problem Statement

Creating websites for ideas, prototypes, or small projects often involves repetitive setup and technical overhead.  
This project simplifies that process by providing a **centralized AI-driven platform** where users can generate and manage websites efficiently.

---

## ✨ Key Features

- 🔐 Secure user authentication using **Better Auth**
- 🤖 AI-powered website generation
- 📁 Project-based architecture with versioning
- 👀 Live preview and public read-only views
- 🌍 Community page for shared projects
- ⚡ Modern UI built with React 19 and Tailwind CSS

> 💡 **Note:** Payment functionality is not currently active. However, the backend architecture supports Stripe-based subscriptions and pricing for future implementation.

---

## 🏗️ Architecture Overview

```

Frontend (React + Vite)
|
| REST APIs
v
Backend (Express + TypeScript)
|
| Prisma ORM
v
PostgreSQL Database

```

AI requests are handled securely on the backend using the **OpenAI SDK**.

---

## 🛠️ Tech Stack

### Frontend
- React 19
- TypeScript
- Vite
- Tailwind CSS v4
- React Router DOM
- Better Auth UI
- Sonner (toast notifications)

### Backend
- Node.js
- Express v5
- TypeScript
- Prisma ORM
- PostgreSQL
- OpenAI SDK
- Stripe (planned integration)
- dotenv, CORS

---

## 📁 Project Structure

```

AI_website_generator/
├── client/
│   ├── src/
│   │   ├── pages/
│   │   ├── components/
│   │   ├── App.tsx
│   │   └── main.tsx
│   └── package.json
│
├── server/
│   ├── server.ts
│   ├── routes/
│   │   ├── projectRoutes.ts
│   │   └── userRoutes.ts
│   ├── prisma/
│   └── package.json
│
└── README.md

````

---

## 🧭 Frontend Routes

| Route | Description |
|------|------------|
| `/` | Landing page |
| `/pricing` | Pricing page (UI only) |
| `/projects` | User project dashboard |
| `/projects/:projectId` | Project workspace |
| `/preview/:projectId` | Live preview |
| `/preview/:projectId/:versionId` | Version-specific preview |
| `/view/:projectId` | Public read-only view |
| `/community` | Community projects |
| `/auth/:pathname` | Login / Signup |
| `/account/settings` | Account settings |

---

## 🔌 Backend Overview

### User APIs
- Authentication and session handling
- User profile management

### Project APIs
- Create and manage projects
- Trigger AI website generation
- Store and retrieve versions
- Fetch preview data

---

## 🤖 AI Integration

- AI generation is handled server-side using the OpenAI SDK
- Prompts and generation logic are encapsulated in backend routes
- Generated content is versioned per project
- Frontend communicates with the backend via REST APIs only

---

## 💳 Payments (Planned)

- Stripe is integrated at the backend level
- Payment flows are **not currently active**
- Architecture supports future subscription or usage-based plans

---

## ⚙️ Environment Variables

Create a `.env` file in the `server` directory:

```env
DATABASE_URL=
OPENAI_API_KEY=
STRIPE_SECRET_KEY=
PORT=
````

---

## 🚀 Getting Started

### Clone the repository

```bash
git clone https://github.com/ishasingh2704/AI_website_generator.git
cd AI_website_generator
```

### Install dependencies

```bash
cd client
npm install

cd ../server
npm install
```

### Run the backend

```bash
cd server
npm run server
```

### Run the frontend

```bash
cd client
npm run dev
```

Frontend runs on: `http://localhost:5173`

---

## 🔮 Future Improvements

* Enable Stripe payments and subscriptions
* Custom AI prompt builder
* Export generated websites as ZIP files
* Team collaboration features
* Analytics dashboard

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👩‍💻 Author

**Isha Singh**
CSE Undergraduate (5th Semester)
Jaypee Institute of Information Technology, Noida

---

### ⭐ Why this project matters

This project demonstrates **full-stack development, AI integration, authentication, and scalable backend design**, making it suitable for **internships, placements, and technical interviews**.


