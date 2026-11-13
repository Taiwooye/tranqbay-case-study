# TranqBay Health — Frontend Engineering Case Study

> **Role:** Founding Frontend Engineer · **When:** 2024 – January 2026 · **Remote**
> **Product:** [tranqbay.health](https://tranqbay.health) — an online therapy platform connecting clients with licensed therapists in Nigeria and beyond, on web, iOS and Android.

The TranqBay codebase is private and belongs to the company, so this repo contains **no company code**. It documents what I built, how I approached it, and what I learned.

---

## Overview

I joined TranqBay on day one of the idea and wrote the first lines of the frontend. I built much of the client-facing product: therapist discovery, public and private provider profiles, the full booking flow and the TranqBay Care website. Later I also built features in the internal back-office used to run the platform.

### Tech stack

| Area | Tools |
|---|---|
| Framework | Next.js (App Router and Pages Router), React, TypeScript |
| Styling / UI | Tailwind CSS, Material UI, Emotion |
| State and data | Redux Toolkit, TanStack Query, Axios |
| Forms | React Hook Form, Yup |
| Internationalisation | next-i18next, multi-currency pricing by country and locale |
| Scheduling and charts | react-big-calendar, date-fns, Chart.js |
| Platform | Feature flags (Flagsmith), Google Analytics 4, OpenTelemetry |
| Tooling | ESLint, Husky and lint-staged, Jest, Docker, GitHub Actions |
| Backend integration | NestJS REST APIs |

---

## What I built

### 1. Booking flow: single and multiple sessions
The core of the product: how a client goes from "I need help" to a confirmed session.

- **Single-session booking.** Pick a therapist, choose a session type (video or audio), select an open slot on their calendar, pay and get confirmation.
- **Multiple-session booking.** Book several sessions in one flow, picking slots across different dates with one checkout.
- Live availability from each therapist's calendar, with timezone handling for clients and therapists in different regions.
- Fees shown in the client's local currency.
- Validation, loading and error states throughout, so a dropped connection never leaves a client unsure whether they've booked.

### 2. Provider profile (therapist-facing app)
_Repo: `tranqbay/provider-profile` (private)._ I built this standalone Next.js app, which provides a profile page for each therapist on the platform.

- Profile page with tabbed sections and responsive styling.
- Server-side rendering wired to the profile API, so profiles load fast and are indexable.
- Contact details, licensing, specialties, languages and fees.
- A full design upgrade and a rewritten landing page with a content carousel.

### 3. Public therapist profiles and discovery
- Therapist profile pages showing specialties, licensing body, languages, ratings, response time and fees.
- Browsing by concern (anxiety, depression, trauma, relationships…), by therapy type (individual, couples, family, child and adolescent) and by location.
- Shareable, SEO-friendly profile URLs.

### 4. TranqBay Care website
- Built the TranqBay Care website as part of the wider TranqBay product.

### 5. Back-office (internal admin)
_Repo: `tranqbay/backoffice` (private)._ Features I built in the internal tool the team uses to manage clients and therapists:

- **Client sessions page.** A responsive view of each client's therapy sessions.
- **Client details.** A full client record view, wired to new API endpoints.
- **Client filtering.** Fixed and improved filtering across the client list.
- **Therapist licence state.** Tracking the verification and licence status of providers.

---

## Engineering highlights

- **Built from zero.** Set up the frontend architecture, project structure and component patterns the product grew on.
- **Multi-currency and multi-language.** Prices shown in the client's local currency, with i18n support across the UI.
- **SEO and performance.** Server-rendered profiles and content pages, so therapists and topics are discoverable through search.
- **Sensitive data handled with care.** Built with mental-health privacy in mind, keeping personal information out of URLs and handling it carefully in the UI.
- **Team workflow.** Feature branches and pull requests, pre-commit linting with Husky, and Docker and GitHub Actions for deployment.

---

## What I learned

- Owning a product's frontend from first commit to production, and shaping it as the business changed.
- Designing booking and scheduling UX where mistakes cost users real money and time.
- Working closely with backend and product to ship quickly in an early-stage startup.

---

**Live product:** [tranqbay.health](https://tranqbay.health) · **Get in touch:** [LinkedIn](https://www.linkedin.com/in/oyedokun-taiwo)
