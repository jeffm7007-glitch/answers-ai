# Answers.AI — Deployment Guide

## What Was Built
- Clean, focused landing page for AI Virtual Receptionist
- Live demo CTA: "Call Our AI Agent" → tel:+18134913590
- Pricing: $499 Starter / $999 Growth
- Link to free calculator
- Mobile-responsive design

## Files Created
- `answers-ai/index.html` — Main landing page
- `answers-ai/CNAME` — Custom domain configuration

## Deploy to Netlify

### Option 1: Netlify Drop (Quickest)
1. Go to https://app.netlify.com/drop
2. Drag and drop the `answers-ai/` folder
3. Netlify will give you a temporary URL
4. Go to Site Settings → Domain Management
5. Add custom domain: `answers-ai.app`
6. Follow DNS instructions

### Option 2: Git Push (Recommended)
1. Create new GitHub repo (e.g., `answers-ai-site`)
2. Push the `answers-ai/` folder to that repo
3. In Netlify: New Site → Import from Git
4. Select the repo
5. Build command: (none, static site)
6. Publish directory: `/`
7. Add custom domain: `answers-ai.app`

## Cloudflare DNS Configuration

In your Cloudflare dashboard for `answers-ai.app`:

1. Go to DNS → Records
2. Add CNAME record:
   - Name: `www`
   - Target: `[your-netlify-site-url].netlify.app`
   - Proxy status: DNS only (gray cloud)

3. Add A record for root:
   - Name: `@`
   - Target: `75.2.60.5` (Netlify's load balancer)
   - Or use CNAME flattening if available

## What to Expect
- Site will be live at `https://answers-ai.app`
- All CTAs point to Telnyx number: +1 (813) 491-3590
- Calculator links open in new tab

## Next Steps
1. Deploy to Netlify
2. Add custom domain in Netlify
3. Configure Cloudflare DNS
4. Test all links and phone number
