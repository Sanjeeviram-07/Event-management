# Event Management System - Client

Next.js frontend for an Event Management System. This is a statically exported application with hybrid rendering capabilities.

## 🚀 Getting Started

### Prerequisites
- Node.js v16+
- npm v8+
- Git

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/sanjeeviram-07/Event-management.git
   cd event-management/client
Install dependencies:

bash
npm install
Create environment file:

bash
cp .env.example .env.local
Edit .env.local with your actual environment variables.

Development
bash
npm run dev
Runs the app in development mode at http://localhost:3000

Production Build
bash
npm run build
Generates an optimized production build in the .next folder.

Static Export (For Static Hosting)
bash
npm run export
Generates static files in the out folder (requires proper configuration).

⚙️ Configuration
next.config.js
javascript
/** @type {import('next').NextConfig} */
const nextConfig = {
  output: 'export', // Enables static export
  trailingSlash: true, // Recommended for static exports
  images: {
    unoptimized: true, // Required for static exports
  },
  // Exclude dynamic routes from export
  exportPathMap: async function(defaultPathMap) {
    const paths = { ...defaultPathMap }
    delete paths['/admin/auth']
    delete paths['/users/signup']
    delete paths['/users/signin']
    return paths
  }
}

module.exports = nextConfig
Important Notes
Pages using getServerSideProps cannot be statically exported

API routes won't work with static exports

Authentication pages need client-side implementation

📂 Project Structure
/client
├── components/       # Reusable components
├── pages/            # Next.js pages
│   ├── api/          # API routes (not available in export)
│   ├── admin/        # Admin pages
│   └── users/        # User auth pages (client-side only)
├── public/           # Static files
├── styles/           # Global styles
├── next.config.js    # Next.js configuration
└── package.json
🛠 Troubleshooting
Common Issues
Static Export Errors:

Remove getServerSideProps from pages or convert to getStaticProps

Ensure all pages are export-compatible

Build Failures:

bash
rm -rf .next out node_modules/.cache
npm install
npm run build
Routing Issues:

Set trailingSlash: true in next.config.js

Use Next.js Link component for client-side navigation

🌐 Deployment
Vercel (Recommended)
Push to GitHub

Import project in Vercel

Set build command: npm run build

Static Hosting (Netlify, GitHub Pages, etc.)
Build and export:

bash
npm run build
npm run export
Deploy contents of out folder

🤝 Contributing
Fork the repository

Create a new branch (git checkout -b feature-branch)

Commit changes (git commit -m 'Add new feature')

Push to branch (git push origin feature-branch)

Open a Pull Request

📄 License
MIT


### Key Features of This README:
1. **Clear Installation Steps** - Guides users through setup
2. **Configuration Details** - Explains your custom Next.js config
3. **Static Export Notes** - Highlights limitations and solutions
4. **Troubleshooting Section** - Addresses common issues you encountered
5. **Deployment Options** - Covers both server and static hosting
6. **Project Structure** - Helps new developers navigate the codebase

You can customize this further by:
- Adding screenshots
- Including API documentation if applicable
- Adding badges for CI/CD status
- Expanding the testing section if you have tests
