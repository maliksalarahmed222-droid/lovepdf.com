# LOVE PDF
## Powerful PDF Tools. Simple by Design.

Love PDF is a full-stack AI-powered PDF SaaS productivity platform built with Next.js (App Router), TypeScript, Tailwind CSS, PostgreSQL, Drizzle ORM, pdf-lib processing engine, Safepay payment gateway integration, and AI document chat.

### Logo Concept
Love PDF features an original brand mark consisting of an injured heart pierced diagonally by an arrow SVG icon alongside dark charcoal and coral typography ("LOVE PDF").

---

## Features
- **50+ Real PDF Tools**: Merge, Split, Compress, Extract Pages, Rotate, Watermark, Sign, Protect, Images to PDF, Text to PDF, OCR Searchable PDF.
- **AI PDF Workspace**: Upload PDF and ask context-aware questions with exact page-level citations.
- **Safepay Pakistan & Billing Architecture**: Real checkout session generation, HMAC webhook verification (`/api/webhooks/safepay`), idempotency checks, automated database user plan upgrades.
- **Developer API Platform**: Issue REST API keys, rate limits, interactive documentation & cURL code snippets.
- **User Dashboard & Teams Workspace**: Recent job logs, cloud document storage, team member invitations.
- **Admin Control Panel**: Real PostgreSQL metrics for total users, subscriptions, payments, and PDF engine jobs.

---

## Tech Stack
- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **Database**: PostgreSQL with Drizzle ORM
- **PDF Engine**: `pdf-lib` server-side & client canvas
- **Payments**: Safepay Payment Gateway (with sandbox testing mode)
- **Authentication**: JWT HttpOnly sessions with bcrypt password hashing

---

## Development Setup
```bash
# Install dependencies
npm install

# Push database schema
npx drizzle-kit push

# Seed initial admin & settings
npx tsx -r dotenv/config src/db/seed.ts

# Start development server
npm run dev
```

---

## Build & Healthcheck Validation
```bash
npm run typecheck
npm run build
```
