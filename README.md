# RidzzHub

RidzzHub is a responsive React + Vite storefront/PWA starter for two brands:
- RidzzPrints: 3D prints and custom print requests
- TipX Customisation: personalised stationery and products

## Run locally
1. Install Node.js 20 or newer.
2. Copy `.env.example` to `.env`.
3. Set `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` using the **publishable/anon key** from the RidzzHub Supabase project.
4. Run `npm install` then `npm run dev`.

## Backend
The Supabase project already has these tables and RLS policies:
`products`, `orders`, `order_items`, `custom_requests`.

The frontend uses only the publishable/anon key. Never put a Supabase secret/service-role key in this app.

## Deployment
Connect this repository to Cloudflare Pages. Build command: `npm run build`. Build output directory: `dist`. Add the two `VITE_` environment variables in Cloudflare Pages settings.

## Current stage
This is a working storefront foundation with catalogue loading, Supabase email/password auth, custom request submission, responsive navigation and PWA manifest. Add real product records and image URLs in Supabase. Live payment processing, image uploads, admin management screens and native Android packaging still need configuration/implementation. Never collect card details directly in this app.