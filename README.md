# ADITYA - Best Todo + Habit Tracker

ADITYA is a production-style responsive web app using Next.js + TypeScript + Tailwind. It supports role-based access (Admin/User), dark mode, habit charts, todo CRUD, and local persistence.

## Quickstart (local dev)

1. install deps

```bash
cd d:/TODOLIST/todolist
npm install
```

2. run dev

```bash
npm run dev
```

3. visit

```
http://localhost:3000
```

### Seed accounts

- Admin: `admin@aditya.app` / `Admin@123`
- User: `user@aditya.app` / `User@123`

## Build for production

```bash
npm run build
npm run start
```

## UI

- dashboard with cards + habit streak chart
- tasks page with status workflow
- habits page with daily entries
- admin panel for users (Admin only)
- settings with theme toggle
- full mobile responsive behavior

## Features implemented

- role-based UI state (Admin/User)
- localStorage persistence for users/tasks/habits/settings
- dark mode + system preference
- charting with Recharts
- modular components + utility functions
- strong accessibility structure (semantic sections, buttons)

## Deploy frontend to GitHub Pages

1. add `homepage` to package.json: `"https://<username>.github.io/<repo>"`
2. build

```bash
npm run build
```

3. copy `app/.next` output to `docs/` (or configure Vercel)

4. configure GitHub Pages to serve from `docs/`

## Backend guidance

This app is currently frontend-only in next app. For full RBAC and secure persistence, connect to backend API (Express + Prisma + Postgres) or Supabase with JWT.

## Security notes

- password hash placeholder uses base64 in utility; replace with bcrypt/argon2 for production
- protect APIs with server-side auth and sessions
- ensure HTTPS, CORS, CSP, and input validation

## folder structure now

```
app/
  components/
    HabitForm.tsx
    HabitItem.tsx
    HabitList.tsx
    TodoForm.tsx
    TodoItem.tsx
    TodoList.tsx
  globals.css
  layout.tsx
  page.tsx
  types.ts
  utils.ts
.github/workflows/
  ci.yml
  deploy.yml
next.config.ts
package.json
README.md
tsconfig.json
```

