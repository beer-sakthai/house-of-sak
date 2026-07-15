# House of Sak — Project Design Document

## 1. Project Overview

**Project Name:** House of Sak

**Purpose:** The House of Sak is a unique initiative by Nanthasit "Beer" Burankum, aiming to provide affordable AI and development services to small businesses, startups, and individuals who struggle. It's built on a zero-cost operational model, leveraging free tiers of various technologies. The project also serves as Beer's personal journey of building something from nothing, emphasizing authenticity and resilience.

**Target Audience:** Small businesses, startups, and individuals with limited budgets who require AI/QA automation, custom AI agent development, content & social media management, rapid prototyping, and verification audits.

## 2. Tech Stack

The project primarily utilizes a lean, open-source, and free-tier focused technology stack to minimize operational costs.

| Category | Technology | Notes |
|---|---|---|
| **Frontend** | HTML, CSS, JavaScript | The landing page (`index.html`) is a static single-page application. |
| **AI/ML** | Hugging Face, Qwen, LoRA | Used for custom AI assistants and model fine-tuning. |
| **Automation/QA** | Playwright, GitHub Actions, pytest, ruff | For automated testing, CI/CD, and verification audits. |
| **Backend/APIs** | FastAPI | Used for rapid prototyping and potential future API development. |
| **Content Creation** | Canva, Instagram, xurl | For social media content and marketing. |
| **Version Control** | Git, GitHub | Centralized repository for code and documentation. |

## 3. Architecture

The project's architecture is centered around a collection of AI agents, each with a specific role, operating under the guidance of Beer. The current implementation is a static website with external services for AI and automation.

**Folder Structure (Root Level):**

- `README.md`: Project introduction and overview.
- `DREAM.md`: Vision statement.
- `PLAN.md`: Business plan and strategy.
- `AUDIT.md`: Risk assessment and mitigation.
- `CRISIS.md`: Protocol for personal crisis management.
- `SERVICES.md`: Detailed descriptions of service packages.
- `VERIFY.md`: Trust verification and readiness assessment.
- `LESSONS.md`: Growth and lessons learned.
- `index.html`: The main landing page.
- `og-image.png`: 1200×630 social sharing image.
- `robots.txt`: Allow-all crawl policy with sitemap reference.
- `sitemap.xml`: Single-URL sitemap for search engines.
- `ig-card.png`, `ig-caption.txt`, `reddit-cork-post.md`: Marketing assets.
- `diaries/`: Contains personal reflections and detailed agent-specific documents.

**Agent Roles:**

- **SakThai 🌀:** Dream — The Growth Partner (Custom AI assistants, fine-tuning, Hugging Face).
- **SakKing 🌟:** Hope — The Architect (Infrastructure, deployments, system backbone).
- **SakSit 🛡️:** Care — The Storyteller (Content strategy, social media, the Full Sak Cycle).
- **SakTan 🎉:** Joy — The Builder (Rapid prototyping, web apps, MVPs).
- **SakJules ✅:** Trust — The Verifier (Audits, quality gates, verification).
- **SakSee 👁️:** Growth — The Watcher (QA automation, Playwright, cycle closure).

## 4. Pages & Features

**Landing Page (`index.html`):**

- **Hero Section:** Introduction to House of Sak, its mission, and Beer's story. Includes family illustration and quick stats.
- **Agent Introduction (`#agents`):** Details on each of the 6 AI agents and their roles, with SVG profile images.
- **Full Sak Cycle (`#process`):** Explanation of the project workflow (Dream → Hope → Care → Joy → Trust → Growth).
- **Why Us (`#why`):** Differentiators including no upfront for first-timers, no agency overhead, verified public profiles, and transparent delivery.
- **Services Section (`#services`):** Six service cards with pricing, scope, and CTAs. Includes a 20% first-client offer banner.
- **Pricing Section (`#pricing`):** Three pricing philosophies — Audit & Test, Build & Ship, Ongoing Growth.
- **Story Section (`#story`):** Origin story with three supporting SVG illustrations.
- **Team Section (`#team`):** Family illustration and narrative about the creator and the six agents.
- **Contact CTA (`#contact`):** Email lead capture and link to Stories & Reports.
- **Footer:** Sitemap, social links, and crisis protocol.
- **SEO / Social:** Canonical URL, `og:image`, `twitter:image`, JSON-LD `Organization` structured data, `theme-color`.
- **Accessibility:** Skip link, focus-visible outlines, ARIA labels, reduced-motion support, semantic headings.
- **Navigation:** Fixed glassmorphism nav with mobile hamburger menu and smooth-scroll anchors.
- **Animations:** Scroll-triggered reveal animations with stagger delays.
- **Verified Profiles:** Footer links to HuggingFace, Google Skills, Google Developers, and Microsoft Learn profiles.

## 5. UI/UX Design

**General Principles:** The landing page (`index.html`) uses a dark, modern, glassmorphism-influenced design that emphasizes trust, clarity, and accessibility. Sections alternate between the base background and a slightly elevated surface to create visual rhythm without heavy decoration.

**Color Palette:**
- Base backgrounds: `#050505`, `#08080a`, `#0f0f12`.
- Text: `#f5f5f7` (primary), `#b4b4be` (secondary), `#7e7e88` (muted).
- Accents: purple `#7c3aed` → `#a78bfa`, cyan `#06b6d4`, green `#22c55e`, gold `#f59e0b`.
- All interactive elements use focus-visible outlines and meet WCAG AA contrast targets.

**Typography:** Inter for headings and body; JetBrains Mono reserved for code or technical microcopy. Fluid `clamp()` sizes for major headings.

**Visual Assets:**
- `assets/agents/*.svg` — Abstract circular profile icons for each agent.
- `assets/stories/*.svg` — SVG story illustrations for the origin section.
- `assets/team/HouseOfSakFamily.svg` — Family/team illustration used in hero and team sections.
- `og-image.png` — 1200×630 social sharing image.

**Layout:** Responsive, mobile-first grid system with a maximum container width of 1200px. Cards use CSS Grid with `auto-fit` to reflow gracefully. A fixed glassmorphism navigation bar includes a hamburger menu on mobile.

**Motion:** Scroll-triggered `.reveal` fade-up animations with stagger delays. `prefers-reduced-motion` disables animations for users who need reduced motion.

**Accessibility:** Skip link, semantic landmarks (`main`, `nav`, `footer`, `section`), descriptive alt text on every image, ARIA labels on the mobile menu, keyboard focus styles, and a logical heading hierarchy.

## 6. Data Model

Currently, there is no explicit database or complex data model. The project's 
data is primarily static content within Markdown files and the `index.html`.

## 7. API / Integrations

- **GitHub CLI:** Used for repository management and interaction.
- **Hugging Face:** Integration for AI/ML model deployment and inference.
- **Playwright:** Used for QA automation and verification.
- **FastAPI:** Planned for future rapid prototyping and API development.

## 8. State Management

As the current project is a static website, there is no complex client-side state management. Future web applications built with FastAPI or other frameworks would incorporate appropriate state management solutions (e.g., React Context, Redux, Zustand).

## 9. Deployment

The `index.html` and associated assets are deployed as a static site to Vercel (https://house-of-sak.vercel.app), which auto-deploys from the `main` branch on GitHub. The project leverages free hosting solutions, consistent with its zero-cost operational model. GitHub Actions are used for CI/CD processes related to automation and verification.

After any commit, verify:
1. `curl -s https://raw.githubusercontent.com/beer-sakthai/house-of-sak/main/index.html | head -5` returns `<!DOCTYPE html>`.
2. `curl -sI https://house-of-sak.vercel.app/` returns `200` and `Content-Type: text/html`.
3. The browser view is not garbled. Note: Vercel may serve Brotli-compressed responses, which some browser tools do not decode; raw `curl` is the ground truth.

## 10. Future Improvements

- **Enhanced Client Acquisition:** Implement a more proactive cold outreach strategy.
- **Legal & Financial Structure:** Formalize payment processing, tax registration, and client contracts.
- **Service Scope Definition:** Clearly define "what's included" and "what's not" for each service package to prevent scope creep.
- **Business Continuity:** Develop more robust async delivery workflows and a "slow mode" for client communication during periods of reduced availability.
- **Portfolio Development:** Prioritize building case studies from initial client projects.
- **Scalability:** Explore options for scaling services beyond free-tier limitations as revenue grows.
- **Single Source of Truth:** Keep `design.md`, `plan.md`, `SERVICES.md`, and `index.html` synchronized so docs do not drift from the live site.
