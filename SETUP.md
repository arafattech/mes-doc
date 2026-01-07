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
    └── market-price-history.md
```

## Technology Used

**Docsify** - A magical documentation site generator that:
- Doesn't require building static files
- Renders Markdown files on-the-fly
- Has a beautiful, responsive theme
- Includes search functionality

## How to Run

### 1. Install Docsify CLI (One-time setup)
```bash
npm install -g docsify-cli
```

### 2. Start the Development Server
```bash
cd /var/www/html/mes-doc
docsify serve .
```

The documentation will be available at: **http://localhost:3000**

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
