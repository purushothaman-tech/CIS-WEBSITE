# IEEE Computational Intelligence Society (IEEE CIS) Student Chapter Website

Official high-performance, accessible, and premium technology website built for the **IEEE CIS Student Chapter of Velammal Institute of Technology**. Designed like a modern developer-first SaaS landing page (inspired by Vercel, Linear, and Stripe) and backed by a dynamic and secure Supabase database.

---

## 🚀 Key Features

- **Cinematic Experience**: Immersive custom vector-art background overlays, glassmorphism card panels, and smooth micro-animations.
- **Dynamic Events Engine**: Renders active announcements, upcoming countdown clocks, speaker profiles, agenda details, maps, past events lists, and certificate resources.
- **Committee Directory**: Filterable search catalogs grouping Faculty Advisors and Student Coordinators by year, department, and category roles.
- **Learning Resource Library**: Accessible roadmaps, lecture cheatsheets, and presentation files filterable by tag elements and study categories.
- **Interactive Lightbox Gallery**: Masonry layouts with full keyboard-navigable Lightbox modal controls.
- **Admin Management Portal (`/admin`)**: Secure gatekeeper login, statistics overview charts, CRUD systems for events and committee directory, application reviewers, inbox controllers, and system audit logs.
- **Row-Level Security (RLS)**: Enforced PostgreSQL database access controls that secure registrations, contact lists, and admin logging.

---

## 🛠️ Technology Stack

- **Framework**: [Next.js 15+ (App Router)](https://nextjs.org)
- **Styling**: CSS Modules (Vanilla CSS custom design tokens)
- **Animations**: [Framer Motion](https://www.framer.com/motion/)
- **Icons**: [Lucide React](https://lucide.dev)
- **Backend Database**: [Supabase (PostgreSQL)](https://supabase.com)
- **File Storage**: Supabase Storage Buckets (`events`, `gallery`, `committee`, `resources`, `documents`)
- **CI/CD**: GitHub Actions

---

## 📂 Project Directory Structure

```
├── .github/
│   └── workflows/
│       └── ci.yml             # GitHub Actions configuration
├── public/                    # Static image/media assets
├── src/
│   ├── app/
│   │   ├── about/             # About Page
│   │   ├── achievements/      # Achievements Timeline Page
│   │   ├── admin/             # Admin Dashboard Page
│   │   ├── committee/         # Committee Directory Page
│   │   ├── contact/           # Contact Form Page
│   │   ├── events/            # Events Page & Dynamic Events [id] Page
│   │   ├── gallery/           # Masonry Lightbox Gallery Page
│   │   ├── membership/        # Tiers & Applications Page
│   │   ├── privacy/           # Terms & Privacy Page
│   │   ├── resources/         # Download Library Page
│   │   ├── layout.js          # Root layout with Providers
│   │   ├── page.js            # Cinematic home landing page
│   │   ├── robots.js          # SEO search engine rules
│   │   └── sitemap.js         # Dynamic sitemap routing
│   ├── components/            # Reusable UI component elements
│   ├── contexts/              # Auth, Theme, and Search state providers
│   └── services/              # Supabase bindings and storage services
└── supabase/
    └── migrations/
        └── schema.sql         # SQL migrations and database schema
```

---

## ⚙️ Setup & Installation

### 1. Clone & Install Dependencies
```bash
git clone https://github.com/your-repo/ieee-cis-vit.git
cd ieee-cis-vit
npm install
```

### 2. Configure Environment Variables
Copy `.env.example` to `.env.local` and add your credentials:
```bash
cp .env.example .env.local
```
Update parameters inside `.env.local`:
```env
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

### 3. Initialize Database Schema
Copy and execute the contents of `supabase/migrations/schema.sql` directly inside your **Supabase SQL Editor** to construct the tables, trigger functions, RLS policies, and default categories.

---

## 🧑‍💻 Running Locally

Run the development compiler server:
```bash
npm run dev
```
Open [http://localhost:3000](http://localhost:3000) with your browser.

- **Offline Simulation Fallback**: If the `.env.local` variables are left blank, the application automatically activates local fallbacks, saving credentials, mock applications, and message details in `localStorage` for testing.

---

## 📦 Building & Deployment

### Compile Production Build
```bash
npm run build
```

### Deploy to Vercel
1. Link your GitHub repository to [Vercel](https://vercel.com).
2. Configure the Environment Variables (`NEXT_PUBLIC_SUPABASE_URL`, `NEXT_PUBLIC_SUPABASE_ANON_KEY`).
3. Deploy! The project compiles statically and dynamically out-of-the-box.

---

## 🛡️ License

This project is licensed under the [MIT License](LICENSE).
