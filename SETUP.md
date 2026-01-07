# Hybritech MES Documentation - Setup Guide

## Project Structure

```
/var/www/html/mes-doc/
├── index.html              # Main HTML file for Docsify
├── README.md               # Home page content
├── _sidebar.md             # Navigation sidebar
└── sales-management/       # Sales Management module docs
    ├── sales-analytics.md
    ├── pricing-plan.md
    ├── sales-order.md
    ├── sales-requests.md
    ├── audit-trail.md
    ├── expired-orders.md
# 🛠️ Project Setup Guide

This guide will help you set up the Hybritech MES Documentation project locally or on a server.

## ✅ Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js**: Version 18 or higher (Download from [nodejs.org](https://nodejs.org/))
- **Git**: To clone the repository

## 📥 Installation

1.  **Clone the Repository**
    ```bash
    git clone <your-repo-url>
    cd mes-doc
    ```

2.  **Install Dependencies (Optional)**
    You can install `docsify-cli` globally for easier usage, or run it via `npx` (recommended).

    *Option A: Global Install*
    ```bash
    npm install -g docsify-cli
    ```

## 🚀 Running the Project

You can run the documentation server using one of the following methods:

### Method 1: Using NPX (Recommended)
No installation required. Just run:
```bash
npx docsify-cli serve .
```

### Method 2: using Global CLI
If you installed docsify-cli globally:
```bash
docsify serve .
```

The server will start at **http://localhost:3000** automatically.

## 📦 Deployment

### Vercel Deployment
This project is configured for easy deployment on Vercel.

1.  Install Vercel CLI: `npm i -g vercel`
2.  Run deployment: `vercel --prod`

### Static Server
Since this is a static site, you can also serve it using any static file server like Nginx, Apache, or Python SimpleHTTPServer.

```bash
# Python example
python3 -m http.server 3000
```

### 3. Stop the Server
Press `Ctrl + C` in the terminal

## How to Add New Pages

1. Create a new `.md` file in the appropriate folder
2. Add the page link to `_sidebar.md`
3. The changes will be reflected immediately (no rebuild needed)

## How to Edit Content

Simply edit any `.md` file and save. Docsify will automatically reload the changes in your browser.

## Deployment

To deploy to production, simply copy all files to your web server. No build step required!
