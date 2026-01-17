# Scheduly

A modern Next.js application with Clerk authentication integration.

## Features

- Next.js 16 with App Router
- Clerk authentication
- Tailwind CSS for styling
- TypeScript support
- Geist font family

## Getting Started

### Prerequisites

1. Create a Clerk account at [clerk.com](https://clerk.com)
2. Get your Publishable Key and Secret Key from the [API keys page](https://dashboard.clerk.com/last-active?path=api-keys)

### Environment Setup

Create a `.env.local` file in the root directory:

```bash
# .env.local
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=YOUR_PUBLISHABLE_KEY
CLERK_SECRET_KEY=YOUR_SECRET_KEY
```

Replace `YOUR_PUBLISHABLE_KEY` and `YOUR_SECRET_KEY` with your actual Clerk keys.

### Installation

Install dependencies:

```bash
npm install
```

### Running the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Authentication

This application uses Clerk for authentication. The authentication flow includes:

- Sign In and Sign Up buttons for unauthenticated users
- User button for authenticated users
- Protected routes using Clerk middleware

## Project Structure

```
src/
├── app/
│   ├── layout.tsx      # Root layout with ClerkProvider
│   ├── page.tsx        # Home page
│   └── globals.css     # Global styles
└── proxy.ts            # Clerk middleware
```

## Technologies Used

- **Next.js 16** - React framework
- **Clerk** - Authentication service
- **Tailwind CSS** - Styling framework
- **TypeScript** - Type safety
- **Geist** - Font family

## Learn More

To learn more about the technologies used:

- [Next.js Documentation](https://nextjs.org/docs)
- [Clerk Documentation](https://clerk.com/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme).

Check out the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.
