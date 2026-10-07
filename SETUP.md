# LOVE PDF — Local Setup Guide

1. Clone repository & install dependencies:
   `npm install`

2. Configure environment in `.env`:
   ```
   DATABASE_URL=postgresql://postgres:postgres@127.0.0.1:5432/app_db
   AUTH_SECRET=your_secret
   SAFEPAY_ENVIRONMENT=sandbox
   SAFEPAY_API_KEY=sec_sandbox_key
   SAFEPAY_MERCHANT_SECRET=sec_merchant_secret
   ```

3. Sync database schema & seed initial data:
   `npx drizzle-kit push`
   `npx tsx -r dotenv/config src/db/seed.ts`

4. Run Next.js App:
   `npm run dev`
