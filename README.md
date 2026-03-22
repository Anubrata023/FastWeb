# FastWeb
# 🌌 StudyVerse — Cosmic Knowledge Hub

> *An anime-space themed, glassmorphic study resource management platform built entirely in vanilla HTML, CSS & JavaScript.*

---

## 📋 Table of Contents

1. [Project Overview](#-project-overview)
2. [Live Files](#-live-files)
3. [Design Philosophy](#-design-philosophy)
4. [Colour Palettes](#-colour-palettes)
5. [Page 1 — Study Nexus Dashboard](#-page-1--study-nexus-dashboard)
6. [Page 2 — Subject Study Page](#-page-2--subject-study-page)
7. [Features Summary](#-features-summary)
8. [Tech Stack](#-tech-stack)
9. [Fonts Used](#-fonts-used)
10. [File Structure](#-file-structure)
11. [How to Run](#-how-to-run)
12. [Roadmap — Upcoming Features](#-roadmap--upcoming-features)
13. [Design Iteration Log](#-design-iteration-log)

---

## 🚀 Project Overview

**StudyVerse** is a student-first web application designed to help learners organise, track, and access their study resources across multiple subjects. The platform combines productivity tools, gamification, wellness tracking, and social study features into one cohesive interface.

The project has been built across **two main pages** so far, with a complete anime-inspired space aesthetic that makes studying feel exciting rather than tedious.

### Core Problem it Solves
> Students often save dozens of useful links but can never find them when needed. They also lack a single place to track their chapter progress, upcoming tests, class schedules, and revision count all at once.

---

## 📁 Live Files

| File | Description |
|------|-------------|
| `study-nexus.html` | Main dashboard — resource organiser & link manager |
| `subject-study-page.html` | Subject deep-dive page — Physics (StudyVerse theme) |

Both files are **self-contained** — no build tools, no dependencies, no server required. Just open in a browser.

---

## 🎨 Design Philosophy

The entire UI is built around three overlapping aesthetic pillars:

### 1. Anime-Space Theme
The interface draws from anime visual language — glowing energy rings, particle effects, orbital animations, and motivational quotes styled after shonen manga. Every element feels like it belongs in a futuristic study dimension.

### 2. Glassmorphism
Cards, panels, and overlays use `backdrop-filter: blur()` with semi-transparent backgrounds to create depth and layering. Borders are subtle rgba values that let the animated background breathe through.

### 3. Gamification
Learning is presented as a progression system — XP bars, level badges, streaks, chapter mastery tiers, and score tracking. This is directly inspired by RPG and anime progression mechanics.

---

## 🖌️ Colour Palettes

The project went through **three colour palette iterations**, each requested by the user:

### Iteration 1 — Cosmic Dark (Original)
```
#03010a  — Void Black (background)
#00f5ff  — Pulsar Cyan (primary accent)
#8b5cf6  — Aurora Violet (secondary)
#ff2d78  — Nova Pink (highlights)
#ffd700  — Comet Yellow (stars)
#e8f0ff  — Star White (text)
```
*Deep space purple-cyan aesthetic. Heavy use of neon glow effects.*

---

### Iteration 2 — Deep Ocean Blue
```
#0a1931  — Navy Void (background)
#1a3d63  — Deep Navy (surfaces)
#4a7fa7  — Steel Blue (accent)
#b3cfe5  — Ice Blue (text/highlights)
#f6fafd  — Near White (primary text)
```
*Calmer, professional blue palette. More suited to focused study sessions.*

---

### Iteration 3 — Purple Dusk (Current — Study Nexus)
```
#190019  — Deep Void (background)
#2B124C  — Royal Purple (deep surfaces)
#522B5B  — Mid Violet (cards)
#854F6C  — Rose Mauve (labels/accents)
#DFB6B2  — Soft Blush (text/highlights)
#FBE4D8  — Warm Petal (primary text)
```
*Warm purple-to-rose gradient. Dreamlike and editorial. Most distinctive.*

---

### Subject Page Palette — StudyVerse Theme
```
#121212  — Ink Black (background)
#30475e  — Steel Navy (surfaces/borders)
#f05454  — Vivid Red (primary accent)
#f5f5f5  — Soft Cream (text)
```
*High contrast. Punchy and editorial. Inspired by the uploaded StudyVerse design file.*

---

## 📄 Page 1 — Study Nexus Dashboard

**File:** `study-nexus.html`

This is the main resource hub where students save and organise links to study materials.

### 🔑 Core Features

#### Resource Management
- **Add Resource** — Enter title, URL, category, and tags. Press Enter to add multiple tags.
- **Favicon Preview** — Auto-fetches site favicon from Google's S2 API using the domain.
- **Display Grid** — All resources shown in an animated card grid with staggered entrance animations.
- **Open Links** — Every card has an "↗ Open Resource" button that opens in a new tab.
- **Delete Resources** — One-click removal with toast confirmation.

#### Organisation
- **6 Categories** — Math 🔢, Science 🧪, Coding 💻, History 📜, Language 📚, Other 🌐
- **Category Filter Tabs** — One-click filtering by category
- **Starred / Important** — Mark resources as priority with ⭐ toggle (gold highlight border)
- **Tag System** — Add multiple custom tags per resource (press Enter after each)
- **Sort Options** — Newest First, Oldest First, A→Z, Starred First
- **Live Search** — Real-time filtering across title, URL, and tags simultaneously
- **Starred Filter** — Dedicated tab to see only priority resources

#### Stats Dashboard
| Stat | Description |
|------|-------------|
| Total Resources | Count of all saved links |
| Starred | Number marked as important |
| Categories | Unique subject categories in use |
| Unique Tags | Total distinct tags across all resources |

#### Persistence
- All data is saved to **localStorage** — resources survive page refresh and browser close.
- Seed data (4 sample resources) is pre-loaded on first visit.

### 🎨 Visual & Animation Features
- **Animated splash screen** — Triple orbital rings + glowing core + progress bar
- **Star canvas** — 300+ twinkling stars drawn on HTML5 Canvas with glint effect
- **Floating particles** — 35 coloured particles rising up the screen
- **3 animated nebula blobs** — Slow-drifting radial gradients giving depth to background
- **3 orbit rings** — Slowly rotating circles at different speeds (60s, 90s, 130s)
- **Shooting stars** — Periodic diagonal streaks across the viewport
- **Smooth cursor** — Custom lagging cursor ring with dot
- **Mouse-reactive card glow** — Each card glows at the exact position of your cursor
- **Animated gradient nav line** — Flowing red-to-cream shimmer under the navbar

---

## 📄 Page 2 — Subject Study Page

**File:** `subject-study-page.html`

This page opens when a student selects a specific subject (currently pre-built for **Physics**). It provides a complete subject management cockpit.

### 🔑 Core Features

#### Subject Hero
- Subject name, board, stream, and chapter count
- **Level Orb** — Animated glowing circle showing current mastery level (Lv.7)
- **XP Progress Bar** — Animated fill showing progress toward next level (3,400 / 5,000 XP)
- **Breadcrumb Nav** — Dashboard → My Subjects → Physics

#### Stats Strip (5 columns)
| Stat | Value |
|------|-------|
| Tests Given | 18 (+3 this week) |
| Revisions Done | 32 (+5 this week) |
| Assignments | 9 |
| Avg Test Score | 76% (+4% vs last month) |
| Total Study Time | 47h |

#### Class Schedule Panel
- Weekly schedule with Day, Time, Topic, and Teacher
- **Live class badge** — Pulsing red dot for currently active classes
- Status badges: Done ✅, Live 🔴, Upcoming, Test

#### Deadlines Panel
- Color-coded urgency system:
  - 🔴 Red border + red countdown = 1–3 days
  - 🟡 Amber border + amber countdown = 4–7 days
  - 🟢 Green countdown = 8+ days
- Deadline types: Test, Assignment, Submission
- **Add Deadline Form** — Expandable inline form:
  - Title input
  - Type selector (Test / Assignment / Submission)
  - Date picker
  - Submit → instantly appears in the deadline list

#### Chapter Cards (10 chapters)
Each chapter card contains:

| Element | Description |
|---------|-------------|
| Chapter number | Formatted as 01, 02, 03... |
| Icon | Unique emoji per chapter |
| Title | Chapter name |
| Urgency badge | Red "Test" or Amber "Assignment" badge if deadline approaching |
| Status badges | ✓ Done, New |
| Stats row | Tests done, Revisions, Assignments, Avg Score |
| Progress bar | Mini horizontal bar showing % complete |
| Left colour bar | Colour indicates mastery: Blue=Beginner, Gradient=Intermediate, Red=Advanced, Red-Orange=Master |
| 👥 Squad button | Opens invite modal for that chapter |

**Click any chapter body → expands inline** showing:
- 4 detailed stats (Level, Tests, Revisions, Progress%)
- First 4 topics with completion dots
- "Open Full Chapter View" button

**Highlighted chapters:** Cards with upcoming tests/assignments have a glowing red border and animated top line.

#### Chapter Filter Controls
- All / In Progress / ⚠ Urgent / Completed

#### Full Chapter View (Slide-In Panel)
Opens as a full-screen slide-in overlay:
- Chapter number tag, full title, subject/board metadata
- 4 stats: Level letter, Tests count, Revisions count, Avg Score
- **Interactive topic checklist** — Click any topic checkbox to mark it complete/incomplete (with toast feedback)
- Two CTAs: ▶ Start Studying | 🎯 Take a Test

#### 👥 Study Squad / Friends Invite
Per-chapter invite system:
- Generates a unique session link per chapter
- **Copy to clipboard** with visual feedback
- Share options: WhatsApp, Email, Copy Link, Instagram
- Expiry note: "Link expires in 24 hours · Max 6 friends"

#### Motivation Banner
- Anime-inspired motivational quotes
- `↻` Refresh button cycles through 5 quotes
- Large decorative quotation mark in background

#### Resources Section
Three resource cards: Video Lectures, Short Notes, Practice Sets — each with item count and category badge.

#### Wellness Panel
Four wellness cards: Meditation, Hydration reminder, Stretch Break, Lo-Fi Music.

#### Today's Session Plan
Mini timetable showing morning, live, afternoon, and evening study blocks.

### 🛠️ Productivity Tools

#### ⏱️ Pomodoro Timer (Modal)
- Three modes: Focus 25, Short Break 5, Long Break 15
- Animated SVG ring showing time remaining
- Controls: Start, Pause, Reset
- Accessible from FAB button, sidebar, or direct link

#### 🎯 Focus Mode (Fullscreen Overlay)
- Blacks out the entire screen
- Running clock showing total focus time in current session
- Inspirational quote displayed
- Exit button to return

#### 😊 Mood Tracker (Sidebar)
- 5 mood options: 😫 😐 🙂 🔥 😎
- Saves selected mood with description text
- Toast notification on mood change

#### ✦ FAB (Floating Action Button)
Expandable menu at bottom-right with:
- Pomodoro Timer
- Focus Mode
- Flashcards (placeholder)
- Lo-Fi Music (placeholder)
- Quick Notes (placeholder)

#### 👤 Profile Dropdown
- Name, rank, class displayed
- Dropdown: My Profile, Leaderboard, Settings, Sign Out

---

## ✨ Features Summary

### Implemented ✅

| Feature | Page |
|---------|------|
| Add / Delete Resources | Dashboard |
| Category Filtering | Dashboard |
| Live Search | Dashboard |
| Tag System | Dashboard |
| Favicon Preview | Dashboard |
| Star / Priority Marking | Dashboard |
| Sort Options | Dashboard |
| Stats Counter | Dashboard |
| LocalStorage Persistence | Dashboard |
| Animated Splash Screen | Dashboard |
| Custom Cursor | Both |
| Star Canvas (twinkling) | Both |
| Shooting Stars | Dashboard |
| Floating Particles | Both |
| Nebula Background | Both |
| Subject Hero + Level/XP | Subject Page |
| Class Schedule | Subject Page |
| Deadlines Panel | Subject Page |
| Add Deadline Form | Subject Page |
| Chapter Cards (10) | Subject Page |
| Chapter Expand/Collapse | Subject Page |
| Urgency Highlighting | Subject Page |
| Chapter Filter Tabs | Subject Page |
| Full Chapter View | Subject Page |
| Topic Checklist | Subject Page |
| Squad Invite Modal | Subject Page |
| Copy Invite Link | Subject Page |
| Motivation Quotes | Subject Page |
| Pomodoro Timer | Subject Page |
| Focus Mode | Subject Page |
| Mood Tracker | Subject Page |
| Sidebar Navigation | Subject Page |
| FAB Menu | Subject Page |
| Profile Dropdown | Subject Page |
| Wellness Panel | Subject Page |
| Resources Grid | Subject Page |
| Toast Notifications | Both |

---

## 🛠️ Tech Stack

| Technology | Usage |
|------------|-------|
| **HTML5** | Structure and semantic markup |
| **CSS3** | All styling — no framework used |
| `backdrop-filter` | Glassmorphism on cards/panels |
| `CSS Custom Properties` | Theme variables for colours |
| `CSS Animations / @keyframes` | All motion effects |
| `CSS Grid & Flexbox` | All layout |
| **Vanilla JavaScript** | All interactivity |
| `localStorage API` | Data persistence (Dashboard) |
| `Clipboard API` | Copy invite links |
| `HTML5 Canvas` | Star field rendering |
| `Google Fonts API` | Font loading |
| `Google Favicon API` | `s2/favicons` for link previews |

**Zero dependencies. Zero build tools. Zero frameworks.**

---

## 🔤 Fonts Used

### Dashboard (Study Nexus)
| Font | Weight | Usage |
|------|--------|-------|
| `Orbitron` | 400, 600, 700, 900 | Headings, logo, stats |
| `Exo 2` | 300, 400, 500, 600 | Body text |
| `Share Tech Mono` | 400 | Labels, codes, tags |

### Subject Page (StudyVerse Theme)
| Font | Weight | Usage |
|------|--------|-------|
| `Playfair Display` | 700, 900, 700i | Section titles, hero, panel titles |
| `DM Sans` | 300, 400, 500, 600 | Body text, buttons |
| `DM Mono` | 400, 500 | Stats, timestamps, badges, code |

---

## 📂 File Structure

```
studyverse/
│
├── study-nexus.html           # Page 1 — Resource Dashboard
│   ├── Splash screen
│   ├── Top navigation
│   ├── Hero section
│   ├── Stats row (4 cards)
│   ├── Add resource panel (form)
│   ├── Filter + search controls
│   └── Resource card grid
│
├── subject-study-page.html    # Page 2 — Subject Study Page
│   ├── Top navigation (breadcrumbs)
│   ├── Sidebar (nav + mood tracker)
│   ├── Subject hero (level + XP)
│   ├── Stats strip (5 cells)
│   ├── Class schedule panel
│   ├── Deadlines panel + add form
│   ├── Motivation quote banner
│   ├── Chapter cards grid (10 chapters)
│   ├── Resources section
│   ├── Wellness + session plan
│   ├── Friends/Squad modal
│   ├── Chapter view overlay
│   ├── Pomodoro modal
│   ├── Focus mode overlay
│   └── FAB menu
│
└── README.md                  # This file
```

---

## ▶️ How to Run

No setup required. Both files are completely standalone.

### Option 1 — Direct Browser Open
1. Download `study-nexus.html` and/or `subject-study-page.html`
2. Double-click the file to open in your browser
3. Everything works offline except Google Fonts (requires internet for correct typography)

### Option 2 — Local Dev Server (Recommended)
```bash
# Using Python
python -m http.server 8000

# Using Node.js (npx)
npx serve .

# Using VS Code
# Install "Live Server" extension → Right-click file → Open with Live Server
```

Then visit `http://localhost:8000`

### Browser Requirements
| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full support |
| Firefox 88+ | ✅ Full support |
| Safari 14+ | ✅ Full support |
| Edge 90+ | ✅ Full support |

> **Note:** `backdrop-filter` (glassmorphism) requires a modern browser. Older browsers will show solid backgrounds instead of glass effect.

---

## 🗺️ Roadmap — Upcoming Features

The following features are planned for future development:

### 🔜 Next Up — High Priority

#### Authentication & User Profiles
- [ ] Sign up / Login page (email + Google OAuth)
- [ ] Persistent user profiles with avatar upload
- [ ] Multiple student accounts per device

#### Multi-Subject Dashboard
- [ ] Subject selector screen (grid of all subjects)
- [ ] Per-subject colour coding
- [ ] Cross-subject stats overview

#### Enhanced Chapter System
- [ ] Chapter-level notes editor (rich text)
- [ ] Flashcard generator per chapter
- [ ] Auto-generate summary from notes

#### Real Flashcards
- [ ] Create / edit / delete flashcard sets
- [ ] Spaced repetition algorithm (SM-2)
- [ ] Flip animation on cards
- [ ] Track flashcard mastery per topic

---

### 📅 Medium Priority

#### Test & Quiz Engine
- [ ] Create custom MCQ tests per chapter
- [ ] Auto-timer during test
- [ ] Detailed results with wrong answer review
- [ ] Score history graph per chapter

#### Study Groups / Rooms
- [ ] Create a live study room with shareable code
- [ ] Real-time presence indicators (who's online)
- [ ] Shared whiteboard / notes area
- [ ] Group chat within a study session

#### Analytics Dashboard
- [ ] Study time heatmap (like GitHub contributions)
- [ ] Weekly progress chart
- [ ] Subject-wise performance radar chart
- [ ] Streak calendar with daily goals

#### Notification System
- [ ] Deadline reminders (browser notifications)
- [ ] Daily study reminders at custom time
- [ ] Upcoming test alerts (3 days / 1 day / day-of)

---

### 🌟 Future Vision

#### AI Study Assistant
- [ ] "Ask a Doubt" AI chatbot per chapter
- [ ] Auto-generate practice questions from chapter notes
- [ ] Summarise long PDF notes into key points
- [ ] Personalised weak-area detection

#### Mobile App (PWA)
- [ ] Service Worker for full offline support
- [ ] Add to Home Screen (PWA manifest)
- [ ] Mobile-optimised layouts
- [ ] Push notifications for deadlines

#### Gamification Expansion
- [ ] Badges and achievements system
- [ ] Class/school leaderboard
- [ ] Daily challenges and quests
- [ ] Study coins that can be "spent" on rewards

#### Content Integration
- [ ] Embed YouTube lecture videos directly in chapter view
- [ ] PDF viewer built into resource cards
- [ ] Google Drive integration for notes
- [ ] Import timetable from Google Calendar

---

## 📝 Design Iteration Log

| Version | Change | Reason |
|---------|--------|--------|
| v1.0 | Initial dashboard built with Cosmic palette (cyan/purple) | Starting aesthetic direction |
| v1.1 | Colour palette changed to Deep Ocean Blue | User requested blue palette from uploaded image |
| v1.2 | Colour palette changed to Purple Dusk | User requested purple palette from uploaded image |
| v1.3 | Added more animations, nebula layers, orbit rings | User requested enhanced space theme |
| v2.0 | Subject study page built (custom theme) | New page with all subject management features |
| v2.1 | Subject page rebuilt to match StudyVerse theme | User uploaded StudyVerse.html as design reference |

---

## 💡 Design Decisions

### Why no framework?
The entire project is pure HTML/CSS/JS to keep it lightweight, teachable, and deployable anywhere — including GitHub Pages, Netlify, or a simple file share. No build step, no node_modules, no configuration.

### Why LocalStorage?
For a student tool used primarily on one device, localStorage provides instant, zero-setup persistence. For a multi-device or collaborative version, this would migrate to a backend API (Supabase / Firebase).

### Why two separate files?
The Dashboard and Subject Page serve different purposes and could eventually be different routes in a full SPA. Keeping them separate makes each file self-contained and independently shareable.

### Why anime theme?
Students (especially in India, the primary target audience) deeply resonate with shonen anime's themes of growth, hard work, and surpassing limits. The aesthetic makes studying feel like a hero's journey — not a chore.

---

## 👨‍💻 Credits

Built with ❤️ using:
- [Google Fonts](https://fonts.google.com) — Typography
- [Google Favicon API](https://www.google.com/s2/favicons) — Link previews
- Inspiration: Anime study culture, JEE/NEET student workflows, Notion-style dashboards


## Team Members
-Anubrata Paul
-Sakshi Sharma
-Kislay Kumar
-Aman Sagar


---

*"Like Naruto becoming Hokage through relentless training — you too shall conquer through unwavering consistency."*
*— StudyVerse Daily Scroll* 🌌
