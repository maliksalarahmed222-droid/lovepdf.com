# LOVE PDF — Architecture Documentation

## System Flow
Browser / Mobile
  ↓
Next.js 16 (App Router)
  ↓
Authentication & Role Middleware
  ↓
PDF Processing Engine (`pdf-lib`)
  ↓
Safepay Gateway & Webhooks (`/api/webhooks/safepay`)
  ↓
PostgreSQL Database (Drizzle ORM)

## Webhook Architecture & Idempotency
1. Safepay issues webhook payload to `/api/webhooks/safepay`.
2. Webhook handler checks `payment_webhook_events` table for duplicate `eventId`.
3. Validates HMAC signature via `verifySafepayWebhookSignature`.
4. Executes transaction to update user `plan`, `subscriptions`, `payments`, and `invoices`.
