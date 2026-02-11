# Deployment Guide

## Vercel (Git Integration)

1. Sign in to Vercel and click "Add New" -> "Project".
2. Import this repository.
3. Framework preset: Next.js.
4. Build command: `bun run build`.
5. Install command: `bun install`.
6. Output directory: `.next` (default).
7. Set environment variables (Production):
   - `UPSTASH_REDIS_REST_URL`
   - `UPSTASH_REDIS_REST_TOKEN`
   - `UPSTASH_REALTIME_URL`
   - `UPSTASH_REALTIME_TOKEN`
   - `NEXT_PUBLIC_APP_URL` (your production URL)
   - `ROOM_EXPIRY_TIME`
8. Deploy.

## Notes

- Vercel will build on every push to the connected branch.
- If you use preview deployments, set the same env vars for Preview.
- Rotate tokens if any secrets were shared outside your local machine.
