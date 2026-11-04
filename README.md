# EduTools Portal 🎓

A modern, responsive Single Page Application (SPA) designed as a unified launchpad and dashboard for the **EduTools** suite of interactive classroom and collaborative learning applications.

---

## 🌟 Overview

EduTools Portal brings together individual interactive web applications into a single, cohesive hub. Educators and students can discover, launch, and interact with all tools from one place without having to remember or bookmark multiple distinct URLs.

---

## 🚀 Hosted Applications & Tools

| Tool | Live URL | Category | Description |
| :--- | :--- | :--- | :--- |
| **WordCloud** | [WordCloud App](https://ericpang.github.io/edutools_wordcloud) | Brainstorming / Visuals | Dynamic word cloud generator for vocabulary, brainstorming, and feedback visualization. |
| **Pin Board** | [Pin Board App](https://ericpang.github.io/edutools_pinboard/) | Collaboration | Virtual corkboard for organizing sticky notes, ideas, and group activities. |
| **Padlet** | [Padlet App](https://ericpang.github.io/edutools_padlet/) | Content Board | Interactive multimedia bulletin board for sharing resources and student posts. |
| **Mind Map** | [Mind Map App](https://ericpang.github.io/edutools_mindmap) | Ideation / Planning | Concept mapping and visual hierarchy builder for complex topics. |
| **Spin the Wheel** | [Spin the Wheel App](https://ericpang.github.io/edutools_spinthewheel/) | Gamification | Interactive random picker and decision wheel for classroom games and student selection. |
| **Live Poll** | [Live Poll App](https://ericpang.github.io/edutools_livepoll/) | Assessment / Feedback | Real-time polling tool for quick formative checks and audience engagement. |

---

## 🎯 Key Features & Requirements

### 1. Modern Card Grid & Dashboard
- **Visual Cards**: Distinct card for each application with custom icons, badges, descriptions, and category tags.
- **Dual Launch Modes**:
  - **Direct Launch**: Open app in a new browser tab.
  - **Embedded Modal / Frame**: Launch app seamlessly inside an overlay / iframe without leaving the portal.
- **Quick Actions**: Copy link to clipboard, mark as favorite, or enter fullscreen.

### 2. Search & Filtering
- **Instant Search**: Real-time filter by tool name, keywords, or description.
- **Category Filter Tabs**: Filter by *All*, *Collaboration*, *Brainstorming*, *Gamification*, *Assessment*.
- **Favorites & Recents**: Track pinned/favorited apps and recently visited tools using browser `localStorage`.

### 3. Responsive & Accessible Design
- **Mobile First**: Optimized layout adapting smoothly across smartphones, tablets, and desktop displays.
- **Keyboard Navigation & Accessibility (a11y)**: Accessible focus states, ARIA roles, and screen-reader-friendly structure.
- **Theme Support**: Clean modern aesthetic (e.g., Linear/Vercel inspired typography and soft shadows) with optional dark/light mode toggle.

---

## 🛠️ Recommended Tech Stack

- **Option A (Zero-Build Vanilla SPA - Recommended for GitHub Pages):**
  - **HTML5 & Vanilla JavaScript (ES Modules)**
  - **Tailwind CSS (via CDN)** or Modern CSS variables
  - **Lucide Icons** (via CDN / SVG)
  - *Benefits:* Instant deployment, zero dependencies, no build step required.

- **Option B (Component Framework):**
  - **Vite + React / Vue 3 + Tailwind CSS**
  - Static site generation exported to `dist/` for GitHub Pages hosting.

---

## 📁 Proposed Project Structure

```text
edutools/
├── index.html              # Main SPA landing page
├── README.md               # Project documentation & specs
├── css/
│   └── styles.css          # Custom styling & overrides
├── js/
│   ├── app.js              # Application logic & state management
│   ├── data.js             # Data configuration for tools list & metadata
│   └── modal.js            # In-app iframe modal & fullscreen handling
└── assets/
    ├── icons/              # App icons and SVG assets
    └── previews/           # Screenshots / preview thumbnails of each app
```

---

## 📋 Data Schema (`js/data.js`)

```javascript
export const tools = [
  {
    id: "wordcloud",
    title: "WordCloud",
    category: "Brainstorming",
    url: "https://ericpang.github.io/edutools_wordcloud",
    description: "Generate dynamic visual word clouds for brainstorming and vocabulary exercises.",
    icon: "cloud",
    tags: ["Brainstorming", "Vocabulary", "Visualization"]
  },
  {
    id: "pinboard",
    title: "Pin Board",
    category: "Collaboration",
    url: "https://ericpang.github.io/edutools_pinboard/",
    description: "Virtual pinboard for sticky notes, brainstorming sessions, and team activities.",
    icon: "pin",
    tags: ["Collaboration", "Notes", "Ideas"]
  },
  {
    id: "padlet",
    title: "Padlet",
    category: "Collaboration",
    url: "https://ericpang.github.io/edutools_padlet/",
    description: "Interactive multimedia board for discussions, reflections, and content curation.",
    icon: "layout-grid",
    tags: ["Content Sharing", "Bulletin Board", "Classroom"]
  },
  {
    id: "mindmap",
    title: "Mind Map",
    category: "Ideation",
    url: "https://ericpang.github.io/edutools_mindmap",
    description: "Structured mind mapping tool for visual thinking and concept breakdowns.",
    icon: "network",
    tags: ["Concept Map", "Planning", "Structure"]
  },
  {
    id: "spinthewheel",
    title: "Spin the Wheel",
    category: "Gamification",
    url: "https://ericpang.github.io/edutools_spinthewheel/",
    description: "Customizable random picker wheel for student participation and classroom games.",
    icon: "disc",
    tags: ["Randomizer", "Gamification", "Games"]
  },
  {
    id: "livepoll",
    title: "Live Poll",
    category: "Assessment",
    url: "https://ericpang.github.io/edutools_livepoll/",
    description: "Real-time voting and instant polling tool for formative checks and quick feedback.",
    icon: "bar-chart-2",
    tags: ["Polling", "Assessment", "Audience"]
  }
];
```

---

## 🚢 Deployment (GitHub Pages)

1. Ensure the entry point is located at the root as `index.html`.
2. Commit and push changes to GitHub:
   ```bash
   git add .
   git commit -m "feat: Add EduTools Portal SPA"
   git push origin main
   ```
3. In the GitHub repository settings:
   - Navigate to **Settings > Pages**.
   - Under **Build and deployment > Source**, choose **Deploy from a branch**.
   - Select the `main` branch and `/ (root)` folder.
   - Click **Save**.
4. Your EduTools portal will be published at `https://ericpang.github.io/edutools/`.

---

## 🔮 Roadmap & Future Enhancements

- [ ] PWA (Progressive Web App) support for offline launching.
- [ ] Direct quick-launch keyboard shortcuts (e.g., `Cmd/Ctrl + K` command palette).
- [ ] Custom tool onboarding (allowing teachers to add external web tools to their personal dashboard).
- [ ] QR code generator on each tool card for instant mobile sharing in the classroom.

