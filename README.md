# MediNotes Pro — AI Healthcare Consultation Assistant (SaaS)

MediNotes Pro is an AI-powered healthcare SaaS platform that transforms clinical consultation notes into:

- Professional summaries
- Action items
- Patient-friendly email communications

The platform uses AI to help clinicians save time, improve documentation quality, and streamline patient communication.

---

## Tech Stack

### Frontend
- Next.js (React + TypeScript)
- Clerk (authentication & subscription management)

### Backend
- FastAPI
- OpenAI API
- Pydantic
- fastapi-clerk-auth

### Infrastructure
- Vercel (frontend hosting)
- AWS (backend deployment planned)

---

## Features

- Secure authentication with Clerk
- Protected app routes
- AI-generated consultation summaries
- Automatic action item extraction
- Patient email drafting
- SaaS-ready architecture

---

## Project Structure

```text
saas/
│
├── pages/                # Next.js frontend pages
├── styles/               # Frontend styling
├── api/
│   ├── index.py          # FastAPI app entrypoint
│   └── .env.example      # Backend env template
│
├── public/
├── requirements.txt      # Python dependencies
├── package.json          # Node dependencies
├── .env.example          # Frontend env template
└── README.md
```

---

# Local Development Setup

## 1️⃣ Frontend (Next.js)

### Install dependencies
```bash
npm install
```

### Run development server
```bash
npm run dev
```

### Open in browser
```
http://localhost:3000
```

---

## 2️⃣ Backend (FastAPI)

### Install Python dependencies
```bash
python3 -m pip install -r requirements.txt
```

### Run API server
```bash
uvicorn api.index:app --reload --port 8000
```

### Backend runs at
```
http://127.0.0.1:8000
```

---

# Environment Variables

Create local environment files:

```bash
cp .env.example .env.local
cp api/.env.example api/.env
```

---

## Frontend (.env.local)

```
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_PUBLIC_API_URL=http://localhost:8000
```

---

## Backend (api/.env)

```
OPENAI_API_KEY=
CLERK_SECRET_KEY=
PORT=8000
ENV=development
```

---

# Deployment

## Frontend
- Vercel

## Backend (Recommended AWS Options)
- App Runner
- ECS / Fargate
- EC2 with Docker

---

# Author

Promise Emeziem Adiole  
AI Engineer | HealthTech Builder | Full-Stack Developer

---

# License

MIT License
