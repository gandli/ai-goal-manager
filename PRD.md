# PRD — AI Goal Manager

## 1. Overview

**Product Name:** AI Goal Manager
**Tagline:** AI-powered personal goal management — from dream to done.
**Target Users:** Professionals, students, and self-improvement enthusiasts who struggle to turn goals into consistent action.

## 2. Problem Statement

Most people set goals but fail to follow through. Existing tools (Notion, Todoist) offer task management but lack:
- Intelligent goal decomposition
- Adaptive replanning when life gets in the way
- Reflection-driven insights that connect effort to outcomes

## 3. Core Features

### 3.1 SMART Goal Parser
- User inputs a goal in natural language (e.g., "I want to learn Spanish")
- AI generates SMART breakdown with milestones, weekly targets, and daily actions
- User can adjust any part of the plan

### 3.2 Daily Check-in
- 60-second daily log: What did you do? How do you feel? Any blockers?
- AI-generated reflection prompts based on recent progress
- Streak tracking with gentle nudges (not guilt trips)

### 3.3 Progress Dashboard
- Visual progress bars per goal and sub-goal
- Weekly/monthly trend charts
- Milestone celebrations with shareable achievement cards

### 3.4 AI Weekly Review
- Auto-generated weekly summary: what worked, what didn't
- Pattern detection: "You're most productive on Tuesdays"
- Adaptive suggestions: reschedule, break down further, or pivot

### 3.5 Achievement System
- Badges for streaks, milestones, and consistency
- XP system with levels
- Optional social sharing

## 4. Technical Architecture

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│   React App  │────▶│  Node.js API │────▶│   Supabase   │
│  (Frontend)  │     │  (Backend)   │     │  (Database)  │
└──────────────┘     └──────┬───────┘     └──────────────┘
                            │
                     ┌──────▼───────┐
                     │   LLM API    │
                     │ (Goal Parse) │
                     └──────────────┘
```

## 5. MVP Scope

| Feature | MVP | V2 |
|---------|-----|----|
| Goal input + SMART parse | ✅ | |
| Daily check-in | ✅ | |
| Progress dashboard | ✅ | |
| AI weekly review | | ✅ |
| Achievement system | | ✅ |
| Social sharing | | ✅ |

## 6. Success Metrics

- Daily active check-in rate > 60%
- Goal completion rate > 30% (industry avg ~8%)
- 7-day retention > 40%

## 7. Risks & Mitigations

| Risk | Mitigation |
|------|-----------|
| Users abandon after initial excitement | Gentle nudges + streak mechanics |
| AI suggestions feel generic | Personalize based on journal history |
| Competitive market (Notion AI, etc.) | Focus on goal-specific UX, not general productivity |
