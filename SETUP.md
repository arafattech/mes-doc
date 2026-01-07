# 🛠️ Hybritech MES Documentation - Setup Guide

This guide covers everything you need to know about setting up, running, and deploying the Hybritech MES Documentation.

## 📂 Project Structure

```
/var/www/html/mes-doc/
├── index.html              # Main HTML file (Docsify Config)
├── README.md               # Home page content
├── _coverpage.md           # Landing page content
├── _sidebar.md             # Navigation sidebar logic
└── sales-management/       # Module specific documentation
    ├── sales-analytics.md
    ├── pricing-plan.md
    └── ...
```

## ✅ Prerequisites

Before starting, ensure you have:
- **Node.js**: Version 18 or higher ([Download](https://nodejs.org/))
- **Git**: Version control

## 📥 Installation

1. **Clone the Repository**
   ```bash
   git clone <your-repo-url>
   cd mes-doc
   ```

2. **Install Dependencies (Optional)**
   It is recommended to use `npx`, but you can install the global CLI if preferred:
   ```bash
   npm install -g docsify-cli
   ```

## 🚀 Running Locally

You can preview the documentation instantly without installing global tools.

**Method 1: Using NPX (Recommended)**
```bash
npx docsify-cli serve .
```

**Method 2: Using Global CLI**
```bash
docsify serve .
```

> The server will start at **http://localhost:3000** automatically.

## 📦 Deployment

### Option 1: Vercel (Recommended)
This project is optimized for [Vercel](https://vercel.com). Code changes are deployed instantly.

**Manual Deployment via CLI:**
```bash
npx vercel --prod
```

### Option 2: Static Server
Since Docsify is a static site generator, you can host it on any web server (Apache, Nginx, etc.) just by uploading the files.

**Running with Python:**
```bash
python3 -m http.server 3000
```

## 📝 Managing Content

**Adding New Pages:**
1. Create a new `.md` file in the relevant folder.
2. Link the file in `_sidebar.md`.

**Editing Content:**
- Simply edit any Markdown (`.md`) file.
- Changes update immediately on refresh (no build step required).
