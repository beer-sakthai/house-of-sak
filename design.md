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
- `ig-card.png`, `ig-caption.txt`, `reddit-cork-post.md`: Marketing assets.
- `diaries/`: Contains personal reflections and detailed agent-specific documents.

**Agent Roles:**

- **SakThai 🧠:** AI/ML Agent (Custom AI assistants, model fine-tuning, Hugging Face expertise).
- **SakKing 👑:** General Assistant (Infrastructure, coordination, system architecture).
- **SakSit 🧿:** Learning & Growth (Content strategy, social media, the Full Sak Cycle).
- **SakTan ⚡:** Creative Builder (Rapid prototyping, web apps, MVP builds).
- **SakJules 🔧:** Automation & CI/CD (GitHub workflows, deployment pipelines, verification audits).
- **SakSee 👁️:** Growth & Verification (The cycle driver — sees everything, closes every loop).

## 4. Pages & Features

**Landing Page (`index.html`):**

- **Hero Section:** Introduction to House of Sak, its mission, and Beer's story.
- **Agent Introduction:** Details on each of the 6 AI agents and their roles.
- **Services Section:** Overview of service packages with pricing.
- **Full Sak Cycle:** Explanation of the project workflow (Dream → Hope → Care → Joy → Trust → Growth).
- **Repository Contents:** Guide to the documentation within the GitHub repository.
- **Client Quick Start:** Instructions for potential clients.
- **Crisis Protocol:** Important contact information for mental health support.
- **Footer:** Licensing, acknowledgments, and links to Beer's professional profiles.

## 5. UI/UX Design

**General Principles:** The landing page (`index.html`) employs a clean, minimalist design with a focus on readability and clear communication. The design uses a dark theme with contrasting text for accessibility.

**Color Palette:** Dominated by dark backgrounds, white/light text, and subtle accent colors for links and interactive elements.

**Typography:** Sans-serif fonts are used for headings and body text, ensuring modern aesthetics and legibility.

**Layout:** Responsive design principles are applied, with content adapting to various screen sizes. Sections are clearly delineated, and calls to action are prominent.

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

The `index.html` and associated assets are deployed as a static site. The project leverages free hosting solutions, consistent with its zero-cost operational model. GitHub Actions are used for CI/CD processes related to automation and verification.

## 10. Future Improvements

- **Enhanced Client Acquisition:** Implement a more proactive cold outreach strategy.
- **Legal & Financial Structure:** Formalize payment processing, tax registration, and client contracts.
- **Service Scope Definition:** Clearly define "what's included" and "what's not" for each service package to prevent scope creep.
- **Business Continuity:** Develop more robust async delivery workflows and a "slow mode" for client communication during periods of reduced availability.
- **Portfolio Development:** Prioritize building case studies from initial client projects.
- **Scalability:** Explore options for scaling services beyond free-tier limitations as revenue grows.
