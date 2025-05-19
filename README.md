# Evently - Event Management Platform

![Evently Banner](public/assets/images/logo.svg)

A modern, full-stack event management platform built with Next.js 14, enabling users to create, discover, and manage events seamlessly.

## 📋 Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Environment Variables](#environment-variables)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## 🤖 Introduction

Evently is a comprehensive event management platform that allows users to create, discover, and manage events. Built with modern web technologies, it provides a seamless experience for both event organizers and attendees. The platform features secure authentication, real-time updates, and a beautiful, responsive user interface.

## ⚙️ Tech Stack

- **Frontend:**
  - Next.js 14
  - TypeScript
  - TailwindCSS
  - Shadcn UI Components
  - React Hook Form
  - Zod (Schema Validation)

- **Backend:**
  - Next.js API Routes
  - MongoDB with Mongoose
  - Clerk (Authentication)
  - Stripe (Payments)
  - UploadThing (File Uploads)

- **Development Tools:**
  - Git
  - Node.js
  - npm/yarn

## 🔋 Features

### Authentication & User Management
- Secure authentication using Clerk
- User profile management
- Role-based access control
- Social login integration

### Event Management
- Create, read, update, and delete events
- Event categorization and filtering
- Search functionality
- Image upload support
- Event details and descriptions

### User Experience
- Responsive design
- Modern UI with TailwindCSS
- Dark/Light mode support
- Mobile-first approach

### Additional Features
- Real-time updates
- File uploads with UploadThing
- Payment processing with Stripe
- MongoDB database integration
- API webhooks for Clerk and Stripe

## 🚀 Getting Started

### Prerequisites

- Node.js (v14 or higher)
- npm or yarn
- MongoDB database
- Clerk account
- Stripe account
- UploadThing account

### Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/evently.git
cd evently
```

2. Install dependencies:
```bash
npm install
# or
yarn install
```

3. Set up environment variables:
Create a `.env` file in the root directory with the following variables:
```env
# Next.js
NEXT_PUBLIC_SERVER_URL=

# Clerk
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=
NEXT_CLERK_WEBHOOK_SECRET=

# MongoDB
MONGODB_URI=

# UploadThing
UPLOADTHING_SECRET=
UPLOADTHING_APP_ID=

# Stripe
STRIPE_SECRET_KEY=
STRIPE_WEBHOOK_SECRET=
NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY=
```

4. Run the development server:
```bash
npm run dev
# or
yarn dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
evently/
├── app/                    # Next.js app directory
│   ├── (auth)/            # Authentication routes
│   ├── (root)/            # Main application routes
│   ├── api/               # API routes
│   └── layout.tsx         # Root layout
├── components/            # React components
│   ├── shared/           # Shared components
│   └── ui/               # UI components
├── constants/            # Application constants
├── lib/                  # Utility functions and configurations
│   ├── actions/         # Server actions
│   ├── database/        # Database configurations
│   └── utils.ts         # Utility functions
├── public/              # Static assets
├── types/               # TypeScript type definitions
└── middleware.ts        # Next.js middleware
```

## 🔗 API Documentation

The application uses Next.js API routes for backend functionality. Key endpoints include:

- `/api/webhook/clerk` - Clerk webhook handler
- `/api/webhook/clerk/stripe` - Stripe webhook handler
- `/api/uploadthing` - File upload handling

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

