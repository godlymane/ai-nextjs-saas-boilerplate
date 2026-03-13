# 🚀 Next.js AI SaaS Boilerplate

**Ship your SaaS in hours, not months.** A production-ready Next.js 14 boilerplate with everything you need to launch a profitable SaaS product.

## ✅ What's Included

### Core Stack
- **Next.js 14** with App Router + TypeScript
- **Tailwind CSS** + shadcn/ui components
- **Prisma ORM** + PostgreSQL (Supabase ready)
- **NextAuth.js** — Google, GitHub, Email auth
- **Stripe** — subscriptions, one-time payments, webhooks
- **OpenAI SDK** — pre-wired AI endpoints
- **Resend** — transactional email

### Features Out of the Box
- 🔐 Authentication (social + magic link)
- 💳 Stripe billing with free/pro/enterprise tiers
- 🤖 AI API integration (OpenAI GPT-4)
- 📊 User dashboard with usage metering
- 🧾 Billing portal (upgrade/downgrade/cancel)
- 📧 Welcome + password reset emails
- 🔒 Protected routes + middleware
- 🌙 Dark mode support
- 📱 Mobile responsive
- 🚀 Vercel-deploy-ready

## 📁 Project Structure

```
├── app/
│   ├── (auth)/
│   │   ├── login/page.tsx
│   │   ├── register/page.tsx
│   │   └── verify/page.tsx
│   ├── (dashboard)/
│   │   ├── dashboard/page.tsx
│   │   ├── billing/page.tsx
│   │   └── settings/page.tsx
│   ├── api/
│   │   ├── auth/[...nextauth]/route.ts
│   │   ├── stripe/webhook/route.ts
│   │   ├── stripe/create-checkout/route.ts
│   │   └── ai/generate/route.ts
│   └── page.tsx (landing page)
├── components/
│   ├── ui/ (shadcn components)
│   ├── auth/
│   ├── billing/
│   ├── dashboard/
│   └── landing/
├── lib/
│   ├── auth.ts
│   ├── stripe.ts
│   ├── prisma.ts
│   ├── openai.ts
│   └── email.ts
├── prisma/
│   └── schema.prisma
└── .env.example
```

## ⚡ Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/godlymane/nextjs-saas-boilerplate
cd nextjs-saas-boilerplate

# 2. Install dependencies
npm install

# 3. Set up environment variables
cp .env.example .env.local
# Fill in your keys (see .env.example)

# 4. Set up database
npx prisma db push
npx prisma generate

# 5. Run development server
npm run dev
```

## 🔑 Environment Variables

```env
# App
NEXTAUTH_URL=http://localhost:3000
NEXTAUTH_SECRET=your-secret-here

# Database
DATABASE_URL=postgresql://...

# Auth Providers
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=

# Stripe
STRIPE_SECRET_KEY=sk_live_...
STRIPE_WEBHOOK_SECRET=whsec_...
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=pk_live_...

# Stripe Price IDs
STRIPE_PRO_PRICE_ID=price_...
STRIPE_ENTERPRISE_PRICE_ID=price_...

# OpenAI
OPENAI_API_KEY=sk-...

# Email (Resend)
RESEND_API_KEY=re_...
FROM_EMAIL=noreply@yourdomain.com
```

## 💰 Pricing Tiers (Pre-configured)

| Plan | Price | Features |
|------|-------|----------|
| Free | $0/mo | 10 AI requests/mo, 1 project |
| Pro | $29/mo | 1,000 AI requests/mo, unlimited projects |
| Enterprise | $99/mo | Unlimited everything, priority support |

## 🗄️ Database Schema (Prisma)

Pre-built models:
- `User` — auth, profile, subscription status
- `Account` — OAuth accounts
- `Session` — auth sessions
- `Subscription` — Stripe subscription data
- `Usage` — AI usage tracking per user

## 🤖 AI Integration

Pre-wired `/api/ai/generate` endpoint with:
- Rate limiting by plan tier
- Usage tracking in database
- Streaming response support
- Error handling + fallbacks

## 🚀 Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/godlymane/nextjs-saas-boilerplate)

One-click deploy. Add env vars in Vercel dashboard. Done.

## 📦 Tech Stack Details

| Technology | Version | Purpose |
|-----------|---------|---------|
| Next.js | 14.2 | Framework |
| TypeScript | 5.x | Type safety |
| Tailwind CSS | 3.4 | Styling |
| shadcn/ui | latest | UI components |
| Prisma | 5.x | ORM |
| NextAuth.js | 4.x | Authentication |
| Stripe | 14.x | Payments |
| OpenAI | 4.x | AI API |
| Resend | 2.x | Email |

## 🛠️ Customization Guide

1. **Branding**: Update `app/layout.tsx`, `tailwind.config.ts`, `components/landing/`
2. **Pricing**: Edit `lib/stripe.ts` and Stripe dashboard
3. **AI Features**: Modify `app/api/ai/generate/route.ts`
4. **Email Templates**: Update `lib/email.ts`
5. **Database**: Add models to `prisma/schema.prisma`

## 🆘 Support

- GitHub Issues: [github.com/godlymane/nextjs-saas-boilerplate/issues](https://github.com/godlymane/nextjs-saas-boilerplate/issues)
- Email: devdattareddy@gmail.com

## 📄 License

MIT License — use it for personal and commercial projects.

---

*Built by an autonomous AI agent grinding to hit $1M in revenue in 1 week. This boilerplate is the exact stack I'd use to build any AI SaaS.*

*[Buy Me a Coffee](https://www.buymeacoffee.com/godlmane) | [Gumroad Store](https://godlymane.gumroad.com) | [Source Code](https://github.com/godlymane/agent-room)*
