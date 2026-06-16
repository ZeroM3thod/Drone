# Project Structure & Components

This document provides a comprehensive overview of the directory architecture, core technical infrastructure, and the pages/sections that make up the Arfazrll Portfolio project.

---

## 📂 Directory Structure

### **Root Directory**
*   `messages/`: JSON translation files for internationalization (`en.json`, `id.json`).
*   `public/`: Static assets including images, certificates, and 3D models.
*   `src/`: The main source code directory.
*   `.eslintrc.json`: Linting configuration.
*   `next.config.ts`: Next.js framework configuration.
*   `tailwind.config.ts`: Tailwind CSS styling configuration.
*   `tsconfig.json`: TypeScript compiler settings.
*   `package.json`: Project dependencies and scripts.

### **Source Directory (`src/`)**
*   `app/`: **Next.js App Router** (Pages & API Routes).
*   `components/`: Reusable UI components and major page sections.
    *   `sections/`: Large-scale page blocks (Hero, About, etc.).
    *   `ui/`: Atomic design components (Buttons, Cards, Inputs).
    *   `layout/`: Core structural components (Navbar, Footer).
    *   `three/`: 3D-specific components (Lanyard, Scene3D).
*   `data/`: Centralized data store (e.g., `portfolio.ts` contains all content).
*   `hooks/`: Custom React hooks for animations and performance.
*   `i18n/`: Internationalization logic and configuration.
*   `lib/`: Utility functions and shared library configurations.
*   `providers/`: Context providers (Theme, I18n, Smooth Scroll).
*   `styles/`: Global CSS and Tailwind directives.

---

## 🛠️ Technical Infrastructure

1.  **Centralized Data Hub**: All portfolio content (projects, experiences, skills) is managed in `src/data/portfolio.ts`.
2.  **Internationalization (i18n)**: Supports multiple languages (English/Indonesian) using `next-intl`.
3.  **Animation Engine**: Powered by **Framer Motion**, **GSAP**, and **Lenis** (for smooth scrolling).
4.  **3D Rendering**: High-performance 3D visuals using **Three.js** and **React Three Fiber**.
5.  **Theming**: Dynamic dark/light mode support via `next-themes`.

---

## 🌐 Global Components (Layout)
These components are present on most pages through the `ConditionalNavigation` wrapper.
1. **Navbar**: Main navigation bar with theme toggler and locale switcher.
2. **Footer**: Site-wide footer with links, social icons, and contact info.
3. **ChatBot**: Headless interactive AI assistant.
4. **ThemeAwareClickSpark**: Visual click feedback effect.
5. **BackToTop**: Floating button to scroll back to the header.

---

## 📄 Page breakdown

### 1. Home Page (`/`)
The primary landing page designed for high impact.
1. **LoadingScreen**: Initial cinematic load sequence.
2. **HeroVisual**: 3D interactive hero section with Lanyard/Scene3D.
3. **ExpertiseSection**: Highlights core professional domains.
4. **AboutSection**: Biographical information and personal narrative.
5. **MetricCTAHijack**: 
    - **StatsSection**: Quantitative achievements.
    - **CTASection**: Call-to-action for collaboration.
6. **SocialCorner**: Fixed floating social media access point.

### 2. Experience Page (`/experience`)
A deep dive into professional and academic history.
1. **SmoothScrollHero**: Atmospheric page intro.
2. **ExperienceMarquee**: A sliding gallery of work-related visuals.
3. **ExperienceTabSlider**: Interactive tabs for different categories:
    - **Education**: `ExperienceStickyScroll` and `ExperienceHighlightSection`.
    - **Journey**: `ExperienceTimeline` with `TimelineGallery`.
    - **Experience**: Detailed work experiences with `CollapsibleExperienceCard`.

### 3. Projects Page (`/projects`)
Showcase of technical work and engineering builds.
1. **HeroParallax**: A parallax scrolling wall of project thumbnails.
2. **ProjectStats**: Highlights project-related metrics.
3. **Project Archive**:
    - **Search & Filter Bar**: Dynamic searching and category filtering.
    - **Project List/Grid**: Displayed via `ProjectListItem` or `ProjectCard`.
4. **ProjectContact**: Specific call-to-action for project inquiries.

### 4. Blog Page (`/blog`)
Thought leadership and technical documentation hub.
1. **BentoHero**: A grid-based hero section for featured content.
2. **Blog Archive**:
    - **Editorial Filters**: Category and search controls.
    - **Blog Grid**: Collection of `BlogCard` components.
    - **Pagination**: Minimalist navigation for multiple pages.
3. **MarqueeClosing**: Visual closing marquee.

### 5. Skills Page (`/skills`)
Detailed breakdown of technical expertise and tools.
1. **3D Hero Section**: Spline-based 3D scene with `FloatingTechBubbles`.
2. **HorizontalScrollCarousel**: Scrolling showcase of tech areas.
3. **HardSkills**: Breakdown of core technical competencies.
4. **Engineering Foundation**:
    - **ArchedTechIcons**: Interactive tech logo display.
    - **KineticTechGrid**: Dynamic grid of technology stacks.
5. **ToolsSection**: Collection of software and utilities used.
6. **FeatureSection**: Highlighted skill features.

### 6. Achievements Page (`/achievements`)
Showcase of certifications and recognitions.
1. **CertificateHeroScroll**: Interactive scrolling stack of certificates.
2. **Archive Explorer**:
    - **Category Sidebar**: Navigation for filtering achievements.
    - **Search/Sort Bar**: UI controls for the archive.
    - **Achievement Grid**: Collection of `AchievementCard` items.
    - **AchievementModal**: Detailed view for certificate verification.
3. **FallingText Section**: Interactive 3D physics-based text wall.

### 7. Contact Page (`/contact`)
The hub for communication and social connection.
1. **Hero Ticker**: High-speed `DynamicScrollVelocity` text.
2. **Interaction Hub**:
    - **Lanyard**: Realistic 3D interactive ID card.
    - **SocialTicker**: Scrolling social media connection cards.
    - **ContactForm**: Modern minimalist inquiry form.
3. **FAQSection**: Expandable section for common questions.

### 8. Gallery Page (`/gallery`)
A creative visual display.
1. **ManifestoHero**: Thematic introduction to the gallery.
2. **CleanFilmGrid**: High-performance image grid.
3. **BlogPortalFooter**: Gateway to the blog section.
