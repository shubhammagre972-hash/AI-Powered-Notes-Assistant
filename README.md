# 🎓 AI-Powered Notes Assistant

<div align="center">

![AI-Powered Notes Assistant](https://img.shields.io/badge/AI--Powered-Notes%20Assistant-6366F1?style=for-the-badge&logo=google&logoColor=white)

**Smart Academic Assistant for Lecture Summarization**

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-Visit_App-6366F1?style=for-the-badge)](https://ai-powered-notes-app-swart.vercel.app)
[![GitHub](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/shubhammagre972-hash/AI-Powered-Notes-Assistant)
[![Vercel](https://img.shields.io/badge/Deployed_on-Vercel-000000?style=for-the-badge&logo=vercel)](https://vercel.com)

![React](https://img.shields.io/badge/React-19-61DAFB?style=flat-square&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=flat-square&logo=typescript)
![Vite](https://img.shields.io/badge/Vite-6.4-646CFF?style=flat-square&logo=vite)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.0-38B2AC?style=flat-square&logo=tailwind-css)
![Google Gemini](https://img.shields.io/badge/Google_Gemini-AI-4285F4?style=flat-square&logo=google)

</div>

---

## 📖 About The Project

The **AI-Powered Notes Assistant** is a web-based academic tool built for students to efficiently manage, organize, and summarize lecture notes using **Google Gemini AI**. It helps students save time by generating concise AI summaries from lengthy lecture content.

> 🎓 **College Project** — MIT Marathwada Institute of Technology  
> 📚 **Course** — B.Voc Software Development, 3rd Year 6th Semester (2025–2026)  
> 👤 **Developer** — Shubham Avchitrao Magre | Roll No: 27  

---

## 🌐 Live Demo

### 👉 [https://ai-powered-notes-app-swart.vercel.app](https://ai-powered-notes-app-swart.vercel.app)

---

## ✨ Features

| Feature | Description |
|---|---|
| 📝 **Note Management** | Create, edit, and organize lecture notes |
| 🤖 **AI Summarization** | Generate concise summaries using Google Gemini 1.5 Flash |
| 📊 **Dashboard** | View total notes, AI summaries count and avg understanding |
| ⭐ **Understanding Rating** | Rate your understanding of each lecture (1–5 stars) |
| 📋 **Project Plan** | Track academic milestones and project features |
| 🎤 **Voice Recording** | Record lectures directly in the app |
| 📱 **Responsive Design** | Works perfectly on mobile, tablet and desktop |

---

## 🛠️ Technology Stack

### Frontend
| Technology | Version | Purpose |
|---|---|---|
| React.js | 19.x | UI component library |
| TypeScript | 5.x | Type-safe JavaScript |
| Vite | 6.4 | Build tool & dev server |
| Tailwind CSS | 3.x | Utility-first styling |
| React Router v7 | 7.x | Client-side routing |

### AI & API
| Technology | Purpose |
|---|---|
| Google Gemini AI | Lecture summarization (gemini-1.5-flash) |
| @google/genai | Official Google AI SDK |

---

## 📁 Project Structure

```
AI-Powered Notes Assistant/
├── frontend/
│   ├── index.html              ← Entry HTML file
│   ├── vite.config.ts          ← Vite configuration
│   ├── tsconfig.json           ← TypeScript config
│   ├── package.json            ← Dependencies
│   ├── .env.local              ← API keys (hidden)
│   └── src/
│       ├── main.tsx            ← React entry point
│       ├── App.tsx             ← Main app component
│       ├── types.ts            ← TypeScript types
│       ├── pages/
│       │   ├── Dashboard.tsx   ← Home dashboard
│       │   ├── Editor.tsx      ← Note editor + AI
│       │   └── ProjectPlan.tsx ← Project charter
│       └── services/
│           └── geminiService.ts ← Gemini AI integration
├── .gitignore                  ← Git ignore rules
├── README.md                   ← This file
└── metadata.json               ← App metadata
```

---

## 🗄️ Database Design (ERD)

The application uses **browser localStorage** for data persistence.

### Note Entity

| Field | Type | Description |
|---|---|---|
| id | string | Unique identifier (UUID) |
| title | string | Lecture note title |
| content | string | Full lecture text |
| summary | string | AI-generated summary |
| subject | string | Subject / Course name |
| understanding | number | Self-rating score (1–5) |
| hasSummary | boolean | AI summary generated flag |
| createdAt | Date | Creation timestamp |
| updatedAt | Date | Last modified timestamp |

### Entity Relationships
```
USER (1) ──────── (many) NOTE
NOTE (1) ──────── (0 or 1) AI_SUMMARY
USER (1) ──────── (many) PROJECT_PLAN
PROJECT_PLAN (1) ─────── (many) MILESTONE
```

---

## 🚀 Run Locally

### Prerequisites
- Node.js 18+
- Google Gemini API Key ([Get free key here](https://aistudio.google.com))

### Installation

**Step 1 — Clone the repository:**
```bash
git clone https://github.com/shubhammagre972-hash/AI-Powered-Notes-Assistant.git
cd AI-Powered-Notes-Assistant
```

**Step 2 — Install dependencies:**
```bash
cd frontend
npm install
```

**Step 3 — Set up environment variables:**
```bash
# Create .env.local file in frontend folder
GEMINI_API_KEY=your_gemini_api_key_here
```

**Step 4 — Start development server:**
```bash
npm run dev
```

**Step 5 — Open in browser:**
```
http://localhost:3000
```

---

## 📱 Screenshots

### Dashboard
The main dashboard shows total notes, AI summaries count and average understanding score.

### Note Editor
Create lecture notes with AI-powered summarization panel on the right side.

### AI Summary
Google Gemini 1.5 Flash generates concise bullet-point summaries from lecture content.

### Project Plan
Academic milestone tracking with wireframes and user stories.

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────┐
│         React Frontend              │
│  Dashboard → Editor → ProjectPlan   │
└──────────────┬──────────────────────┘
               │ Direct API Call
               ▼
┌─────────────────────────────────────┐
│       Google Gemini AI API          │
│     gemini-1.5-flash model          │
│   Lecture Summarization Engine      │
└─────────────────────────────────────┘
               │
               ▼
┌─────────────────────────────────────┐
│      Browser localStorage           │
│    Notes · Summaries · Settings     │
└─────────────────────────────────────┘
```

---

## ⚠️ Limitations

- No user authentication system
- Data stored in browser localStorage only
- Single-user only — no collaboration
- Requires internet for AI summarization

---

## 🔮 Future Scope

- [ ] User authentication with JWT
- [ ] MongoDB / Firebase cloud database
- [ ] Voice-to-text note input
- [ ] Multi-language summarization
- [ ] Mobile app with React Native
- [ ] Note sharing and collaboration

---

## 📚 References

- [React Documentation](https://react.dev)
- [Google Gemini AI API](https://ai.google.dev)
- [Vite Build Tool](https://vitejs.dev)
- [Tailwind CSS](https://tailwindcss.com)
- [React Router v7](https://reactrouter.com)

---

## 👤 Developer

**Shubham Avchitrao Magre**

- 🎓 B.Voc Software Development — 3rd Year, 6th Semester
- 🏫 MIT — Marathwada Institute of Technology
- 📅 Academic Year: 2025–2026
- 🔢 Roll Number: 27

---

## 📄 License

This project is created for academic purposes at MIT — Marathwada Institute of Technology.

---

<div align="center">

Made with ❤️ by Shubham Avchitrao Magre | MIT Marathwada Institute of Technology

⭐ Star this repository if you found it helpful!

</div>
