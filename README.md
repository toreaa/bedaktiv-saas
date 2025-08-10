# BedAktiv SaaS Platform

En multitenant aktivitetsplattform for norske bedrifter.

## 🏗️ Teknologi Stack

- **Frontend:** Next.js 14 + TypeScript
- **Styling:** Tailwind CSS + Shadcn/ui
- **Database:** Supabase (PostgreSQL)
- **Auth:** Supabase Auth
- **Hosting:** Vercel
- **Email:** Resend

## 📁 Prosjektstruktur

```
bedaktiv-saas/
├── src/
│   ├── app/                    # Next.js App Router
│   │   ├── (auth)/            # Auth group routes
│   │   ├── admin/             # Superadmin routes
│   │   ├── org/               # Organization routes
│   │   └── page.tsx           # Landing page
│   ├── components/            # React components
│   │   ├── ui/                # Shadcn/ui components
│   │   ├── auth/              # Auth components
│   │   ├── admin/             # Admin components
│   │   └── shared/            # Shared components
│   ├── lib/                   # Utilities
│   │   ├── supabase/          # Database client
│   │   ├── auth/              # Auth helpers
│   │   └── utils.ts           # General utilities
│   ├── types/                 # TypeScript types
│   └── hooks/                 # Custom React hooks
├── supabase/
│   ├── migrations/            # Database migrations
│   ├── seed.sql              # Initial data
│   └── config.toml           # Supabase config
├── docs/                     # Documentation
└── README.md
```

## 🎯 MVP Funksjoner

### Superadmin (Oss)
- [x] Organisasjons-administrasjon
- [x] Bruker-oversikt på tvers av orgs
- [x] System-statistikk
- [x] Billing-oversikt

### Org Admin (Bedrifter)
- [x] Bruker-invitasjoner
- [x] Aktivitetstype-administrasjon
- [x] Organisasjons-innstillinger
- [x] Rapporter og statistikk

### Brukere (Ansatte)
- [x] Manuell aktivitetsregistrering
- [x] Personlig dashboard
- [x] Leaderboards og konkurranser
- [x] Profil-administrasjon

## 🚀 Quick Start

```bash
# Clone repository
git clone [repository-url]
cd bedaktiv-saas

# Install dependencies
npm install

# Setup environment variables
cp .env.example .env.local

# Run development server
npm run dev
```

## 📊 Database Schema

Standard aktivitetstyper med poeng:
- **Gåing:** 3000-8000=1p, 8000-14000=2p, 14000+=3p (skritt)
- **Løping:** 2-5=1p, 5-8=2p, 8+=3p (km)  
- **Sykling:** 5-15=1p, 15-35=2p, 35+=3p (km)
- **Svømming:** 400-1000=1p, 1000-2000=2p, 2000+=3p (meter)

## 🔧 Development

### Environment Setup
1. Supabase project med database
2. Resend email service
3. Vercel deployment

### Code Standards
- TypeScript strict mode
- ESLint + Prettier
- Conventional commits
- Component composition pattern

## 📈 Roadmap

### MVP (v1.0)
- Grunnleggende multitenant funksjonalitet
- Manuell aktivitetsregistrering
- Email-invitasjoner
- Månedlige konkurranser

### Post-MVP (v2.0)
- Strava/Garmin integrasjoner
- Team-baserte konkurranser
- Avanserte analytics
- Mobile PWA

## 🤝 Contributing

1. Create feature branch fra `main`
2. Utvikle feature med tests
3. Submit pull request
4. Code review og merge

## 📄 License

Private - BedAktiv AS
