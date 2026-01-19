# CoverageGrader

> A comprehensive insurance policy review and rating platform that helps users make informed decisions about their insurance coverage.

CoverageGrader is a modern web application that provides detailed reviews, ratings, and rankings of insurance providers and policies. The platform features a public-facing website for users to search, compare, and review insurance policies, along with a powerful admin dashboard for content management and analytics.

---

## 🚀 Tech Stack

### Core Technologies
- **Framework:** [Next.js 16](https://nextjs.org/) with Turbopack
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Runtime:** Node.js 20+

### Frontend Libraries
- **UI Framework:** React 19
- **Component Libraries:** 
  - [Material-UI (MUI)](https://mui.com/) - Core UI components
  - [Radix UI](https://www.radix-ui.com/) - Accessible primitives
  - [PrimeReact](https://primereact.org/) - Rich UI components
- **Styling:** [Tailwind CSS 4](https://tailwindcss.com/)
- **Icons:** Lucide React, React Icons, MUI Icons

### State Management & Data Fetching
- **State Management:** [Redux Toolkit](https://redux-toolkit.js.org/)
- **API Client:** RTK Query
- **HTTP Client:** Axios

### Forms & Validation
- **Form Management:** [React Hook Form](https://react-hook-form.com/)

### Data Visualization
- **Charts:** [Chart.js](https://www.chartjs.org/), [Recharts](https://recharts.org/)
- **Progress Indicators:** React Circular Progressbar, React Progress Bar

### Additional Features
- **Rich Text Editor:** [Quill](https://quilljs.com/)
- **Notifications:** [Sonner](https://sonner.emilkowal.ski/) (Toast notifications)
- **Alerts:** [SweetAlert2](https://sweetalert2.github.io/)
- **Date Picker:** React DatePicker
- **Theme:** next-themes (Dark/Light mode support)
- **Authentication:** Cookie-based auth with js-cookie

---

## ✨ Key Features

### Public Website
- 🔍 **Insurance Search & Rankings** - Search and compare insurance providers with detailed rankings
- ⭐ **User Reviews & Ratings** - Community-driven reviews and ratings system
- 📊 **Policy Comparison** - Side-by-side policy comparison and detailed information
- 📝 **Blog & Resources** - Educational content about insurance coverage
- ❓ **FAQ Section** - Comprehensive answers to common insurance questions
- 👤 **User Profiles** - Personal accounts for managing reviews and preferences
- 📱 **Responsive Design** - Fully responsive across all devices

### Admin Dashboard
- 📈 **Reports & Analytics** - Comprehensive analytics and reporting tools
- 👥 **User Management** - Manage user accounts and permissions
- 🏢 **Insurance Provider Management** - Add, edit, and manage insurance providers
- 📋 **Policy Management** - Create and maintain policy information
- ✍️ **Content Management** - Manage blog posts, FAQs, and static content
- 💬 **Review Moderation** - Monitor and moderate user reviews
- 🔔 **Notifications System** - Send and manage user notifications
- ⚙️ **Settings & Configuration** - Platform-wide settings and customization

### Authentication
- 🔐 **Secure Login/Signup** - User authentication system
- 🔑 **Password Management** - Change password functionality
- 👤 **Profile Updates** - User profile management

---

## 📁 Project Structure

```
Michaelcurtis_Fronend/
├── src/
│   ├── app/
│   │   ├── (website)/          # Public-facing pages
│   │   │   ├── page.tsx        # Homepage
│   │   │   ├── rankings/       # Insurance rankings
│   │   │   ├── search/         # Search functionality
│   │   │   ├── policies/       # Policy listings
│   │   │   ├── blog/           # Blog pages
│   │   │   ├── faq/            # FAQ section
│   │   │   ├── profile/        # User profiles
│   │   │   └── ...             # Other public pages
│   │   ├── (admin)/            # Admin panel
│   │   │   └── admin/
│   │   │       ├── page.tsx    # Admin dashboard
│   │   │       ├── user-management/
│   │   │       ├── policies-management/
│   │   │       ├── insurance-providers/
│   │   │       ├── blog/
│   │   │       ├── reviews/
│   │   │       ├── reports-analytics/
│   │   │       ├── notifications/
│   │   │       ├── content/
│   │   │       └── settings/
│   │   ├── (authentication)/   # Auth flows
│   │   │   └── auth/
│   │   │       ├── login/
│   │   │       └── sign-up/
│   │   ├── api/                # RTK Query API definitions
│   │   │   ├── admin/          # Admin API services
│   │   │   └── website/        # Public API services
│   │   ├── components/         # Shared components
│   │   ├── pages/              # Additional page components
│   │   ├── utility/            # Utility functions
│   │   ├── layout.tsx          # Root layout
│   │   ├── globals.css         # Global styles
│   │   └── store.ts            # Redux store configuration
│   ├── components/
│   │   └── ui/                 # Reusable UI components
│   ├── utility/
│   │   └── types/              # TypeScript type definitions
│   ├── helper/                 # Helper functions
│   └── lib/                    # Library configurations
├── public/                     # Static assets
├── .github/                    # GitHub workflows
├── Dockerfile                  # Docker configuration
├── next.config.ts              # Next.js configuration
├── tailwind.config.ts          # Tailwind CSS configuration
├── tsconfig.json               # TypeScript configuration
└── package.json                # Dependencies and scripts
```

---

## 🛠️ Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** 20.x or higher
- **npm** (comes with Node.js) or **yarn** or **pnpm**

---

## 📦 Installation

1. **Clone the repository**

```bash
git clone <repository-url>
cd Michaelcurtis_Fronend
```

2. **Install dependencies**

```bash
npm install
# or
yarn install
# or
pnpm install
```

3. **Configure environment variables**

Create a `.env.local` file in the root directory and add the required environment variables (see [Environment Variables](#-environment-variables) section below):

```bash
cp .env.example .env.local
```

Then edit `.env.local` with your actual values.

4. **Run the development server**

```bash
npm run dev
```

5. **Open your browser**

Navigate to [http://localhost:3000](http://localhost:3000) to see the application.

---

## 🔐 Environment Variables

This application requires the following environment variables to function properly. Create a `.env.local` file in the root directory based on the `.env.example` template.

### Required Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `NEXT_PUBLIC_API_BASE_URL` | Base URL for the backend API | `https://api.coveragegrader.com` |

### Example Configuration

See `.env.example` file for a template:

```env
# API Configuration
NEXT_PUBLIC_API_BASE_URL=https://api.example.com
```

> **⚠️ Security Warning:** Never commit your `.env.local` file or expose real API keys in your code. The `.env.local` file is already included in `.gitignore`.

---

## 📜 Available Scripts

In the project directory, you can run:

### `npm run dev`

Runs the app in development mode with Turbopack for faster compilation.  
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.

### `npm run build`

Builds the application for production with Turbopack optimization.  
Creates an optimized production build in the `.next` folder.

### `npm start`

Starts the production server.  
Must run `npm run build` first.

### `npm run lint`

Runs ESLint to check for code quality issues.

---

## 🐳 Docker Support

This project includes Docker support for containerized deployment.

### Build Docker Image

```bash
docker build -t coveragegrader .
```

### Run Docker Container

```bash
docker run -p 3000:3000 coveragegrader
```

The application will be available at [http://localhost:3000](http://localhost:3000).

---

## 📸 Screenshots

_Screenshots will be added here to showcase the application's interface and features._

### Homepage
> Coming soon

### Insurance Rankings
> Coming soon

### Admin Dashboard
> Coming soon

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**CoverageGrader Team**

For questions or support, please contact the development team.

---

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- UI components from [Material-UI](https://mui.com/), [Radix UI](https://www.radix-ui.com/), and [PrimeReact](https://primereact.org/)
- Icons from [Lucide](https://lucide.dev/) and [React Icons](https://react-icons.github.io/react-icons/)

---

**Made with ❤️ for better insurance decisions**
