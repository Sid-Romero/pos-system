# POS - Personal Operating System

> **A unified decision-making system for life optimization**  
> Orchestrate your time, money, and energy with intelligent simulations and ML-powered insights.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.109+-009688.svg)](https://fastapi.tiangolo.com)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16+-316192.svg)](https://www.postgresql.org/)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

---

## Table of Contents

- [General](#overview)
- [Core Philosophy](#core-philosophy)
- [Features](#features)
- [Architecture](#architecture)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)

---

## General

**POS (Personal Operating System)** is not a productivity app—it's a **decision engine** for your life.

Unlike fragmented tools (budget apps, fitness trackers, calendars), POS treats your life as an **integrated system** where every decision impacts your three fundamental resources:

-  **Money** (budget, investments, financial goals)
-  **Time** (intelligent scheduling, constraint optimization)
-  **Energy** (physical recovery, cognitive load, wellbeing)

### The Problem

Traditional tools fail because they operate in silos:
- Budgeting apps don't know your schedule
- Fitness trackers ignore your finances
- Calendars can't predict burnout

**Result:** You make decisions blindly, risking budget deficits, schedule overload, or physical exhaustion.

### The Solution

POS provides a **simulation-first approach**:

```
Question: "Can I afford 10 driving lessons this month?"

POS analyzes:
✓ Current budget & projected income
✓ Fixed expenses & subscriptions
✓ Available free time
✓ Energy impact (10h committed)

Answer: "⚠️ ATTENTION - Budget OK, but conflicts detected:
- Exam preparation needs 15h/week
- Would push you to 85% energy capacity (burnout risk)
Recommendation: Split across 2 months (5h each)"
```

---

## Core Philosophy

### 1. **Simulation Over Tracking**
Don't just log what happened—**simulate what will happen** before acting.

### 2. **Systemic Thinking**
Your life isn't compartmentalized. A new gym membership affects your budget, schedule, AND energy. POS models these interdependencies.

### 3. **ML That Learns From You, For You**
No generic AI chatbot. POS uses **specialized machine learning**:
- Auto-categorize expenses (Random Forest)
- Predict future spending (LSTM)
- Optimize weekly schedules (Reinforcement Learning)
- Recommend investments (Collaborative Filtering + financial rules)

### 4. **Privacy-First, Self-Hosted**
Your financial data, workout logs, and life goals stay on **your infrastructure**. Open source, Docker-based, fully auditable.

---

## Features

###  Core Engine
- **Decision Simulator**: Evaluate any action (expense, commitment, investment) against all constraints
- **Resource Manager**: Real-time tracking of money, time, energy with projection models
- **Conflict Detector**: Automatic detection of schedule clashes, budget deficits, overload risks

### Finance Module
- **Bank Integration**: Auto-sync via EnableBanking, Plaid, SimpleFin (PSD2 compliant)
- **Smart Budgeting**: Envelope system with threshold alerts
- **Investment Tracking**: Portfolio management, compound interest projections, FIRE calculator
- **Expense Prediction**: ML-powered forecasting of next month's spending
- **Tax Optimization**: Automatic fiscal calculations (PFU, TMI, niche fiscale)

### Time Intelligence
- **Constraint-Based Scheduling**: Define hard (work, family) and soft (gym, study) constraints
- **Auto-Generated Planners**: Weekly schedules optimized for productivity + recovery
- **Calendar Sync**: Bidirectional sync with Google Calendar, Outlook
- **Conflict Resolution**: Suggests alternatives when schedule is infeasible

### Body System
- **Workout Tracker**: Strength, calisthenics, cardio with progression analytics
- **Recovery Management**: Muscle group tracking, fatigue scoring, rest recommendations
- **Program Library**: Push/Pull/Legs, Upper/Lower, skill progressions (handstand, muscle-up)
- **Performance Analytics**: Volume tracking, 1RM estimations, plateau detection

### Nutrition Module
- **TDEE Calculator**: Personalized caloric targets (cutting, maintenance, lean bulk)
- **Macro Tracker**: Protein/carbs/fat with daily adjustments based on training
- **Meal Planner**: Auto-generate weekly menus respecting macros + budget
- **Batch Cooking Scheduler**: Optimize meal prep sessions (time + cost)
- **Recipe Database**: Nutritional info, prep time, cost per serving

### Knowledge Tracker
- **Certification Roadmap**: Break down exams into domains, track progress, budget allocation
- **Study Session Planner**: Auto-schedule study blocks based on deadlines
- **Quiz System**: Daily culture générale, technical reviews, spaced repetition
- **Resource Manager**: Links to docs, labs, videos, student deals (<26 ans)

### Spiritual Module
- **Quran Progress**: Memorization tracking, revision scheduler (Ebbinghaus curve)
- **Prayer Reminders**: Auto-calculated times (Aladhan API), notifications
- **Knowledge Quizzes**: Tafsir, fiqh, sira with scoring system

### Driving Module
- **Driving Lessons**: Daily practice sessions, theme tracking, exam countdown
- **Driving Budget**: Allocate hours per month, cost projections, school comparisons
- **Progress Tracker**: Hours completed, exams passed, license timeline

### Gamification Engine
- **Unified Points System**: Earn across all modules (finance discipline, workout consistency, study streaks)
- **Levels & Badges**: Bronze/Silver/Gold/Platinum tiers per domain
- **Rewards System**: Link achievements to real-world rewards (new gear, experiences)

---

## Architecture

### High-Level Design

```
<img width="722" height="492" alt="pos drawio" src="https://github.com/user-attachments/assets/b35b4744-189d-4667-ae6a-02a63cd1d18a" />

```

### Tech Stack (for now)

**Backend:**
- **FastAPI** (async Python framework)
- **PostgreSQL** (relational database)
- **SQLAlchemy** (ORM with Alembic migrations)
- **Redis** (caching + session management)
- **Celery + RabbitMQ** (async tasks, scheduled jobs)
- **Scikit-learn** (ML models for classification, prediction)

**Frontend:**
- **React 18** (UI framework)
- **Next.js 14** (SSR, routing, API routes)
- **Zustand** (state management)
- **React Query** (server state sync)
- **shadcn/ui + Tailwind** (component library)
- **Recharts** (data visualization)

**Infrastructure:**
- **Docker + Docker Compose** (containerization)
- **GitHub Actions** (CI/CD)
- **Fly.io / Railway** (backend hosting)
- **Sentry** (error tracking)
- **Grafana** (metrics dashboard)
---

##  Contributing

This is currently a **personal project** but contributions are welcome once the MVP is stable.

### Development Workflow (the standard)

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Code Standards

- **Backend**: Follow PEP 8, use `black` for formatting, `mypy` for type checking
- **Frontend**: ESLint + Prettier, TypeScript strict mode
- **Commits**: Conventional Commits format (`feat:`, `fix:`, `docs:`, etc.)
- **Tests**: Required for new features (pytest for backend, Jest for frontend)
- For the moment, i didn't implement yet a commit control/pre-commit rules so please consider these rules before contributing.
---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- Inspired by the principles of **quantified self** and **systems thinking**
- Financial concepts drawn from **FIRE movement** and **Bogleheads philosophy**
- ML approaches influenced by **scikit-learn** and **fast.ai** communities
- Architecture patterns from **Clean Architecture** (Robert C. Martin) and **Domain-Driven Design** (Eric Evans)


<div align="center">

[⬆ Back to Top](#-pos---personal-operating-system)

</div>
