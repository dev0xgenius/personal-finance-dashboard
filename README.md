# Personal Finance Dashboard

A full-stack financial management dashboard built with Next.js 15, Prisma, PostgreSQL, and Redux Toolkit. Track accounts, transactions, budgets, and savings goals in one place.

---

## Features

- Account management with balance tracking
- Transaction history with category filters
- Budget planning with monthly limits
- Savings goals with progress tracking
- Responsive sidebar UI with shadcn/ui components
- PostgreSQL database with Prisma ORM

## Tech Stack

- **Framework:** Next.js 15 (App Router, Turbopack)
- **Language:** TypeScript
- **State:** Redux Toolkit
- **Database:** PostgreSQL + Prisma ORM
- **UI:** shadcn/ui (Radix primitives), Tailwind CSS v4, lucide-react
- **Components:** Sidebar, Sheet, Dialog, Tooltip, Skeleton

## Getting Started

### Prerequisites
- Node.js 18+, PostgreSQL

### Installation

```bash
git clone https://github.com/dev0xgenius/personal-finance-dashboard.git
cd personal-finance-dashboard
npm install
```

### Environment (.env)

```env
DATABASE_URL="postgresql://user:password@localhost:5432/finance_db"
```

### Database Setup

```bash
npx prisma migrate dev
```

### Run

```bash
npm run dev
```

## Database Schema

- **User** - name, email (unique)
- **Account** - user_id, name, type, balance (Decimal)
- **Transaction** - account_id, amount, date, category, description
- **Budget** - user_id, category, monthly_limit, month_year
- **Goal** - user_id, name, target_amount, current_amount, deadline

## Project Structure

```
app/
  page.tsx        # Dashboard overview
prisma/
  schema.prisma   # Database models
  migrations/     # Migration history
components/
  ui/             # shadcn/ui components
lib/
  store.ts        # Redux store configuration
  hooks.ts        # Custom hooks
  utils.ts        # Utility functions
```

## Author

**0xgenius** - [GitHub](https://github.com/dev0xgenius)
