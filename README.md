# SplitMint

A small Splitwise‑style group expense tracker built with Node.js, MongoDB and React.

## Features

- Email/password authentication (register, login)
- Groups (max 3 participants + primary user)
  - Create, edit, delete (cascade delete expenses)
  - Store participant details (name, color/avatar placeholder)
- Participants
  - Add, edit, remove (blocked if linked to expenses)
- Expenses
  - Amount, description, date, payer, group, participants
  - Split modes: equal or custom (percentage via custom)
  - Edit & delete
  - Automatic balance recalculation
  - Rounding consistency
- Balance engine
  - Per‑participant net balance
  - Who owes whom
  - Minimal settlement suggestions
- Visualizations
  - Summary cards (total spent, owed, owing)
  - Transaction history with filters (text, participant, date range, amount)
- Search & Filters
- AI‑ish MintSense (optional)
  - Converts simple natural language sentences into structured expenses

## Tech stack

- **Backend:** Node.js, Express, MongoDB (Mongoose), JWT
- **Frontend:** React (Vite), React Router, Axios

## Running locally

### Prerequisites

- Node.js >= 18
- MongoDB (local or cloud)

### Backend

```bash
cd backend
npm install
cp .env.example .env   # or create .env manually
# edit MONGO_URI and JWT_SECRET
npm run dev
