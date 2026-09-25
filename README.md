# IEEE Computational Intelligence Society — Student Chapter

### Velammal Institute of Technology

<p align="center">
  <strong>A modern, accessible, and dynamic digital platform for the IEEE CIS Student Chapter at Velammal Institute of Technology.</strong>
</p>

<p align="center">
  <a href="https://ieee-cis-1746jxnsb-leee23.vercel.app/">
    🌐 Visit Live Website
  </a>
  &nbsp;•&nbsp;
  <a href="https://github.com/purushothaman-tech/CIS-WEBSITE">
    💻 View Source Code
  </a>
</p>

---

## 🌐 Live Website

**IEEE CIS Student Chapter | Velammal Institute of Technology**

🔗 https://ieee-cis-1746jxnsb-leee23.vercel.app/

---

## 📖 About the Project

The **IEEE Computational Intelligence Society (IEEE CIS) Student Chapter Website** is a modern web platform developed for the IEEE CIS Student Chapter at **Velammal Institute of Technology**.

The platform serves as a centralized digital hub for students, faculty, members, and visitors to:

* Discover upcoming and past events
* Explore the chapter committee
* Access learning resources
* View achievements and activities
* Browse the chapter gallery
* Apply for membership
* Contact the chapter
* Manage chapter content through an administrative portal

The website combines a **premium modern interface** with a **dynamic backend architecture**, providing an extensible foundation for managing the chapter's digital presence.

---

## ✨ Key Features

### 🏠 Modern Landing Experience

* Premium, responsive landing page
* Modern visual design
* Glassmorphism-inspired interface
* Smooth animations and micro-interactions
* Responsive layouts across desktop, tablet, and mobile
* Developer-focused visual language

### 📅 Events Management

A dynamic event system for managing chapter activities.

**Includes:**

* Upcoming events
* Event announcements
* Countdown displays
* Event details
* Speaker information
* Agendas
* Venue/location information
* Past events
* Event resources and certificates

### 👥 Committee Directory

A structured directory for chapter leadership and coordinators.

**Features:**

* Faculty advisors
* Student officers
* Committee members
* Role-based organization
* Department categorization
* Academic-year filtering
* Search and filtering

### 📚 Learning Resources

A centralized resource library for students.

**Resources can include:**

* Learning roadmaps
* Lecture materials
* Cheatsheets
* Presentations
* Study resources
* Documents
* Categorized learning content

### 🖼️ Interactive Gallery

A visual archive of chapter activities.

**Features:**

* Masonry-style gallery
* Image previews
* Lightbox interface
* Keyboard navigation
* Responsive image layouts

### 🏆 Achievements

A dedicated section showcasing the chapter's:

* Achievements
* Milestones
* Activities
* Recognitions
* Major accomplishments

### 🤝 Membership

A dedicated membership interface allowing students to:

* Learn about membership
* Explore available membership information
* Submit applications
* Access relevant chapter information

### 📩 Contact System

A dedicated contact interface for communicating with the chapter.

The system supports centralized handling of submitted messages through the administrative interface.

### 🔐 Administrative Portal

The platform includes a protected `/admin` dashboard for authorized administrators.

**Administrative capabilities include:**

* Dashboard statistics
* Event management
* Committee management
* Membership/application management
* Contact/inbox management
* Content management
* System activity monitoring
* Audit logging

### 🛡️ Database Security

The backend uses **Supabase PostgreSQL** with **Row-Level Security (RLS)** to control database access.

Security mechanisms are used for areas including:

* Registrations
* Contact submissions
* Administrative operations
* Database access policies
* Audit records

---

# 🛠️ Technology Stack

| Layer          | Technology                    |
| -------------- | ----------------------------- |
| Framework      | Next.js 15+                   |
| Architecture   | Next.js App Router            |
| Language       | JavaScript                    |
| Styling        | CSS Modules / Custom CSS      |
| Animations     | Framer Motion                 |
| Icons          | Lucide React                  |
| Backend        | Supabase                      |
| Database       | PostgreSQL                    |
| Storage        | Supabase Storage              |
| Authentication | Supabase                      |
| Security       | PostgreSQL Row-Level Security |
| CI/CD          | GitHub Actions                |
| Deployment     | Vercel                        |

---

# 🏗️ Architecture

```text
┌──────────────────────────────────────────┐
│              User Interface              │
│       Next.js + React + CSS Modules      │
└─────────────────────┬────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────┐
│           Application Layer              │
│        Next.js App Router / APIs         │
└─────────────────────┬────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────┐
│              Supabase                    │
│                                          │
│  PostgreSQL Database                     │
│  Authentication                          │
│  Row-Level Security                      │
│  Storage                                 │
└─────────────────────┬────────────────────┘
                      │
                      ▼
┌──────────────────────────────────────────┐
│              Deployment                  │
│                 Vercel                   │
└──────────────────────────────────────────┘
```

---

# 📂 Project Structure

```text
CIS-WEBSITE/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── public/
│   └── Static assets and media
│
├── src/
│   ├── app/
│   │   ├── about/
│   │   ├── achievements/
│   │   ├── admin/
│   │   ├── committee/
│   │   ├── contact/
│   │   ├── events/
│   │   ├── gallery/
│   │   ├── membership/
│   │   ├── privacy/
│   │   ├── resources/
│   │   ├── layout.js
│   │   ├── page.js
│   │   ├── robots.js
│   │   └── sitemap.js
│   │
│   ├── components/
│   │   └── Reusable UI components
│   │
│   ├── contexts/
│   │   └── Application state and providers
│   │
│   └── services/
│       └── Supabase and storage services
│
├── supabase/
│   └── migrations/
│       └── schema.sql
│
├── .env.example
├── next.config.mjs
├── package.json
├── LICENSE
└── README.md
```

---

# 🚀 Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/purushothaman-tech/CIS-WEBSITE.git
```

Navigate into the project:

```bash
cd CIS-WEBSITE
```

---

## 2. Install Dependencies

```bash
npm install
```

---

## 3. Configure Environment Variables

Create a local environment file:

```bash
cp .env.example .env.local
```

Configure your Supabase credentials:

```env
NEXT_PUBLIC_SUPABASE_URL=https://your-project.supabase.co
NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

> Never commit `.env.local` or private credentials to the repository.

---

## 4. Configure Supabase

Open the Supabase SQL Editor and execute:

```text
supabase/migrations/schema.sql
```

This initializes the required database structure, policies, triggers, and related configuration.

---

## 5. Run the Development Server

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# 🧪 Production Build

To verify the application builds successfully:

```bash
npm run build
```

To start the production server locally:

```bash
npm start
```

---

# ☁️ Deployment

The application is designed for deployment using **Vercel**.

### Deployment Steps

1. Push the repository to GitHub.
2. Import the repository into Vercel.
3. Configure the required environment variables.
4. Connect the Supabase project.
5. Deploy the application.

### Production Website

🔗 **https://ieee-cis-1746jxnsb-leee23.vercel.app/**

---

# 🔐 Security

Security is an important part of the platform architecture.

The project uses:

* Supabase Authentication
* PostgreSQL Row-Level Security
* Protected administrative functionality
* Environment variables for credentials
* Supabase Storage access policies
* Database access policies
* Audit logging

Sensitive credentials should always remain outside the source repository.

---

# ♿ Accessibility

The platform is designed with accessibility in mind, including:

* Responsive layouts
* Keyboard-friendly interactions
* Semantic navigation
* Accessible interactive components
* Focus-aware UI elements
* Readable typography
* Responsive design across device sizes

Accessibility should continue to be tested as new features are introduced.

---

# 📱 Responsive Design

The website is designed to work across:

* 🖥️ Desktop
* 💻 Laptop
* 📱 Mobile
* 📟 Tablet

The interface adapts its layouts, navigation, cards, galleries, and content sections according to screen size.

---

# 🔄 CI/CD

GitHub Actions is used for automated project workflows.

```text
Developer
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions
    │
    ├── Validation
    └── Build Checks
    │
    ▼
Vercel Deployment
    │
    ▼
Production Website
```

---

# 🧑‍💻 Development

### Run development mode

```bash
npm run dev
```

### Build the project

```bash
npm run build
```

### Start production mode

```bash
npm start
```

### Run linting

```bash
npm run lint
```

---

# 🤝 Contributing

Contributions and improvements are welcome.

### Contribution workflow

```bash
git checkout -b feature/your-feature
```

Make your changes, test them locally, and commit:

```bash
git add .
git commit -m "Add: your feature"
```

Push the branch:

```bash
git push origin feature/your-feature
```

Then open a Pull Request.

---

# 📜 License

This project is licensed under the **MIT License**.

See the [`LICENSE`](./LICENSE) file for details.

---

# 🏛️ IEEE CIS Student Chapter

**IEEE Computational Intelligence Society Student Chapter**

**Velammal Institute of Technology**

### Department

**Artificial Intelligence and Data Science**

---

## 🌐 Connect With the Chapter

### Website

🔗 https://ieee-cis-1746jxnsb-leee23.vercel.app/

### Source Code

🔗 https://github.com/purushothaman-tech/CIS-WEBSITE

---

<p align="center">
  <strong>IEEE Computational Intelligence Society</strong>
  <br/>
  Student Chapter · Velammal Institute of Technology
  <br/><br/>
  Built with Next.js, Supabase & modern web technologies.
</p>
