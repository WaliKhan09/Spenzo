# Spenzo - AI-Powered Personal Finance Management Platform

<div align="center">
  <img src="public/logo.png" alt="Spenzo Logo" width="200"/>
  
  [![Live Demo](https://img.shields.io/badge/Live_Demo-View_Online-22c55e?style=for-the-badge&logo=vercel)](https://spenzo.vercel.app/)
  [![Next.js](https://img.shields.io/badge/Next.js-15.4.4-black?style=for-the-badge&logo=next.js)](https://nextjs.org/)
  [![React](https://img.shields.io/badge/React-19.0.0-blue?style=for-the-badge&logo=react)](https://reactjs.org/)
  [![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue?style=for-the-badge&logo=typescript)](https://www.typescriptlang.org/)
  [![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.1-38B2AC?style=for-the-badge&logo=tailwind-css)](https://tailwindcss.com/)
  [![Prisma](https://img.shields.io/badge/Prisma-6.0.1-2D3748?style=for-the-badge&logo=prisma)](https://www.prisma.io/)
  [![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13+-336791?style=for-the-badge&logo=postgresql)](https://www.postgresql.org/)
  [![Clerk](https://img.shields.io/badge/Clerk-Auth-6C47FF?style=for-the-badge)](https://clerk.com/)
  [![Google AI](https://img.shields.io/badge/Google_AI-Gemini-4285F4?style=for-the-badge)](https://ai.google.dev/)
</div>

## 🌐 Live Demo

**Visit the live application:** [https://spenzo.vercel.app/](https://spenzo.vercel.app/)

Experience the full features of Spenzo including AI-powered receipt scanning, smart transaction categorization, and intelligent budget management.

## 📊 Overview

Spenzo is a modern, AI-powered personal finance management platform that helps users track expenses, manage budgets, and gain insights into their financial habits. Built with Next.js 15, React 19, and powered by Google's Generative AI, Spenzo provides a comprehensive solution for personal financial management with advanced features like receipt scanning, automated categorization, and intelligent budget recommendations.

## ✨ Key Features

### 🎯 Core Financial Management
- **Multi-Account Support** - Manage multiple bank accounts and credit cards in one place
- **Smart Transaction Tracking** - Automatically categorize and track all your transactions
- **Budget Planning & Monitoring** - Create and manage budgets with intelligent recommendations
- **Recurring Transactions** - Automatically handle recurring payments and income
- **Real-time Balance Updates** - Instant account balance synchronization
- **Transaction History** - Comprehensive transaction history with filtering and search

### 🤖 AI-Powered Features
- **Smart Receipt Scanner** - Extract data automatically from receipts using Google's Generative AI
- **Automated Categorization** - AI automatically categorizes your transactions
- **Intelligent Insights** - Receive AI-powered financial insights and recommendations
- **Predictive Analytics** - Forecast spending patterns and budget recommendations
- **Smart Data Extraction** - Extract transaction details from receipt images

### 📱 User Experience
- **Modern UI/UX** - Beautiful, responsive design built with Tailwind CSS and Radix UI
- **Real-time Updates** - Instant synchronization across all devices
- **Dark/Light Mode** - Toggle between themes for comfortable viewing
- **Mobile Responsive** - Optimized for all device sizes
- **Intuitive Navigation** - Clean and easy-to-use interface

### 🔐 Security & Performance
- **Rate Limiting** - ArcJet integration for API protection
- **Secure Authentication** - Clerk-powered authentication system
- **Data Validation** - Zod schema validation for all inputs
- **Optimized Performance** - Turbopack for fast development builds

## 🛠️ Tech Stack

### Frontend
- **Next.js 15** - React framework with App Router and Server Components
- **React 19** - Latest React with concurrent features
- **Tailwind CSS** - Utility-first CSS framework
- **Radix UI** - Accessible component primitives
- **Lucide React** - Beautiful icons
- **Recharts** - Data visualization library
- **React Hook Form** - Performant forms with validation

### Backend & Database
- **Prisma** - Type-safe database ORM
- **PostgreSQL** - Reliable relational database
- **Clerk** - Authentication and user management
- **Inngest** - Background job processing
- **ArcJet** - Rate limiting and security

### AI & External Services
- **Google Generative AI** - AI-powered features and receipt scanning
- **Resend** - Email delivery service
- **React Email** - Email template system

### Development Tools
- **ESLint** - Code linting
- **PostCSS** - CSS processing
- **Turbopack** - Fast bundler for development

## 🗄️ Database Schema

The application uses PostgreSQL with the following main models:

### User Model
- User authentication and profile management
- One-to-many relationships with accounts, transactions, and budgets

### Account Model
- Multiple account types (Current, Savings)
- Balance tracking with automatic updates
- Default account designation

### Transaction Model
- Income and expense tracking
- Recurring transaction support
- Receipt URL storage
- Category-based organization
- Status tracking (Pending, Completed, Failed)

### Budget Model
- Budget amount tracking
- Alert system for budget limits
- User-specific budget management

## 🚀 Getting Started

### Prerequisites
- Node.js 18+ 
- PostgreSQL database
- Clerk account for authentication
- Google AI API key (for AI features)
- Resend account (for email features)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/WaliKhan09/spenzo.git
   cd spenzo
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**
   Create a `.env.local` file in the root directory:
   ```env
   # Database
   DATABASE_URL="postgresql://username:password@localhost:5432/spenzo"
   DIRECT_URL="postgresql://username:password@localhost:5432/spenzo"
   
   # Authentication (Clerk)
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   CLERK_SECRET_KEY=your_clerk_secret_key
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
   NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
   NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding
   
   # AI Services (Google Generative AI)
   GEMINI_API_KEY=your_google_ai_api_key
   
   # Email (Resend)
   RESEND_API_KEY=your_resend_api_key
   
   # Security (ArcJet)
   ARCJET_KEY=your_arcjet_key
   
   # Background Jobs (Inngest)
   INNGEST_EVENT_KEY=your_inngest_event_key
   INNGEST_SIGNING_KEY=your_inngest_signing_key
   ```

4. **Set up the database**
   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. **Seed the database (optional)**
   ```bash
   npm run seed
   ```

6. **Run the development server**
   ```bash
   npm run dev
   ```

7. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📁 Project Structure

```
spenzo/
├── app/                    # Next.js App Router
│   ├── (auth)/            # Authentication pages
│   │   ├── sign-in/       # Sign in pages
│   │   └── sign-up/       # Sign up pages
│   ├── (main)/            # Main application pages
│   │   ├── dashboard/     # Dashboard components
│   │   │   └── _components/
│   │   │       ├── account-card.jsx
│   │   │       ├── budget-progress.jsx
│   │   │       └── transaction-overview.jsx
│   │   ├── account/       # Account management
│   │   │   └── [id]/      # Individual account pages
│   │   └── transaction/   # Transaction management
│   │       ├── create/    # Add transaction page
│   │       └── _components/
│   │           ├── transaction-form.jsx
│   │           └── receipt-scanner.jsx
│   └── api/               # API routes
│       ├── inngest/       # Background job handlers
│       └── seed/          # Database seeding
├── components/            # Reusable UI components
│   ├── ui/               # Base UI components (shadcn/ui)
│   ├── header.jsx        # Application header
│   ├── hero.jsx          # Landing page hero
│   └── create-account-drawer.jsx
├── lib/                  # Utility libraries
│   ├── prisma.js         # Database client
│   ├── arcjet.js         # Rate limiting
│   ├── inngest/          # Background jobs
│   └── utils.js          # Utility functions
├── actions/              # Server actions
│   ├── account.js        # Account management
│   ├── budget.js         # Budget operations
│   ├── dashboard.js      # Dashboard data
│   ├── transaction.js    # Transaction CRUD
│   ├── send-email.js     # Email functionality
│   └── seed.js           # Database seeding
├── data/                 # Static data
│   ├── categories.js     # Transaction categories
│   └── landing.js        # Landing page data
├── hooks/                # Custom React hooks
├── emails/               # Email templates
├── prisma/               # Database schema and migrations
└── public/               # Static assets
```

## 🔧 Available Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run email` - Start email preview server
- `npm run seed` - Seed database with sample data

## 📊 Features in Detail

### Transaction Management
- **Create/Edit Transactions** - Add new transactions with detailed information
- **Receipt Scanning** - Upload receipt images for automatic data extraction
- **Recurring Transactions** - Set up automatic recurring payments
- **Category Management** - Comprehensive category system with subcategories
- **Transaction History** - View and filter transaction history

### Account Management
- **Multiple Accounts** - Manage current and savings accounts
- **Balance Tracking** - Real-time balance updates
- **Account Overview** - Visual account cards with key metrics
- **Default Account** - Set primary account for transactions

### Budget System
- **Budget Creation** - Set monthly budgets with alerts
- **Progress Tracking** - Visual budget progress indicators
- **Smart Alerts** - Get notified when approaching budget limits
- **Budget Analytics** - Detailed budget insights and recommendations

### AI Features
- **Receipt Scanning** - Extract transaction details from images
- **Smart Categorization** - Automatic transaction categorization
- **Financial Insights** - AI-powered spending analysis
- **Predictive Budgeting** - Intelligent budget recommendations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Guidelines
- Follow the existing code style and structure
- Add proper TypeScript types where applicable
- Include tests for new features
- Update documentation for API changes

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Next.js](https://nextjs.org/) for the amazing React framework
- [Tailwind CSS](https://tailwindcss.com/) for the utility-first CSS framework
- [Prisma](https://www.prisma.io/) for the type-safe database ORM
- [Clerk](https://clerk.com/) for authentication
- [Radix UI](https://www.radix-ui.com/) for accessible components
- [Google AI](https://ai.google.dev/) for AI-powered features

## 📞 Support

If you have any questions or need help, please open an issue on GitHub or contact me at walikhanait@gmail.com.

---

<div align="center">
  <p>Made with ❤️ by Mohammad Wali Khan</p>
  <p>Track your finances smarter with AI</p>
</div>
