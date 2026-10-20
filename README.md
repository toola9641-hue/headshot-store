# Headshot Store — free starter package

## What this is
A mobile-first storefront prototype with:
- Headshot Store branding
- Product cards with placeholder poster artwork, price and validity
- Product details screen
- Product-specific chat UI
- Demo messages saved locally in the same browser/device

## This is NOT yet a live private chat
The included chat is only a frontend preview. Messages do not reach you or another visitor. Do not publish it as a working private messaging service until a backend is connected.

## Free deployment plan
1. Create a free GitHub account and a repository.
2. Upload `index.html` to the repository.
3. Deploy the repository as a static site on Cloudflare Pages (free plan supports static assets; see official plan limits).
4. For real chat, create a Supabase free project and configure authentication/access control, a messages table, row-level security (RLS), and Realtime. Never expose the service-role key in browser code.
5. Connect the frontend to Supabase using only the public anon/publishable key and strict RLS policies.
6. Test in two different browsers/devices: one as store owner, one as visitor.
7. Add the final live URL to Instagram bio.

Official plan references:
- Cloudflare Pages limits: https://developers.cloudflare.com/pages/platform/limits/
- Supabase pricing and free limits: https://supabase.com/pricing
- Supabase Realtime limits: https://supabase.com/docs/guides/realtime/limits

## Before publishing
- Replace the three sample product entries in the `products` array inside `index.html`.
- Replace placeholder art with your own product poster images.
- Add actual prices, validity, terms, delivery details and contact expectations.
- Configure a real backend for messaging. The chat history must be stored server-side to sync across devices.
- Protect the owner's chat with authentication. A secret URL alone is not a strong access-control mechanism.
- Add a privacy policy and basic abuse/reporting controls if visitors can message you.

## Security truth
A normal website cannot guarantee prevention of screenshots, external screen recording, or someone photographing the screen with another device. Text selection restrictions are a minor deterrent, not real security. Do not promise users that screenshots are impossible.
