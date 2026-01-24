# Scheduly

A smart meeting scheduling platform that eliminates the back-and-forth of finding meeting times. Connect your Google Calendar, set your availability, and let others book time with you instantly.

## Features

- **Smart Scheduling**: Visual drag-and-drop calendar for setting availability
- **Google Calendar Integration**: Sync multiple calendars and prevent double bookings
- **Automatic Video Meetings**: Every booking generates a Google Meet link
- **Timezone Intelligence**: Automatic timezone detection for global meetings
- **Multiple Meeting Types**: Create different meeting types with custom durations
- **Real-Time Updates**: Track booking status and attendee responses
- **Public Booking Pages**: Share your personalized booking link
- **User Authentication**: Secure authentication with Clerk
- **Plan-Based Limits**: Free, Starter, and Pro tiers with different features

## Tech Stack

- **Next.js 15** with App Router
- **TypeScript** for type safety
- **Clerk** for authentication and user management
- **Sanity CMS** for content management and data storage
- **Tailwind CSS** for styling
- **Lucide React** for icons
- **Google Calendar API** for calendar integration
- **date-fns** for date manipulation

## Getting Started

### Prerequisites

1. Create a Clerk account at [clerk.com](https://clerk.com)
2. Get your Publishable Key and Secret Key from the [API keys page](https://dashboard.clerk.com/last-active?path=api-keys)
3. Create a Google Cloud project and enable the Google Calendar API
4. Create OAuth 2.0 credentials for Google Calendar integration
5. Create a Sanity project at [sanity.io](https://sanity.io)

### Environment Setup

Create a `.env.local` file in the root directory:

```bash
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=YOUR_PUBLISHABLE_KEY
CLERK_SECRET_KEY=YOUR_SECRET_KEY

# Google Calendar API
GOOGLE_CLIENT_ID=YOUR_GOOGLE_CLIENT_ID
GOOGLE_CLIENT_SECRET=YOUR_GOOGLE_CLIENT_SECRET

# Sanity CMS
NEXT_PUBLIC_SANITY_PROJECT_ID=YOUR_SANITY_PROJECT_ID
NEXT_PUBLIC_SANITY_DATASET=YOUR_SANITY_DATASET
SANITY_API_READ_TOKEN=YOUR_SANITY_READ_TOKEN
SANITY_API_WRITE_TOKEN=YOUR_SANITY_WRITE_TOKEN
```

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

## Project Structure

```
src/
├── app/
│   ├── (app)/                 # Authenticated routes
│   │   ├── availability/      # Availability management page
│   │   └── settings/          # Settings and account management
│   ├── layout.tsx             # Root layout with ClerkProvider
│   ├── page.tsx               # Landing page
│   └── globals.css            # Global styles
├── components/
│   ├── landing/               # Landing page components
│   ├── settings/              # Settings page components
│   └── ui/                    # Reusable UI components
├── lib/
│   ├── features.ts            # Plan limits and feature flags
│   └── ...                    # Utility functions
├── sanity/
│   ├── lib/                   # Sanity client configuration
│   ├── queries/               # GROQ queries
│   └── schemaTypes/           # Sanity schema definitions
└── proxy.ts                   # Clerk middleware
```

## How It Works

1. **Authentication**: Users sign up/in with Clerk
2. **Calendar Connection**: Connect Google Calendar accounts in settings
3. **Availability Setup**: Use the visual calendar to set available time slots
4. **Meeting Types**: Create different meeting types (15min, 30min, 60min, etc.)
5. **Share Link**: Get a public booking link to share with others
6. **Bookings**: Guests select time slots and book meetings instantly
7. **Calendar Events**: Events are automatically created in Google Calendar with Google Meet links

## API Integrations

- **Google Calendar API**: For calendar sync and event creation
- **Clerk Backend API**: For user authentication and subscription management
- **Sanity API**: For content management and data storage

## Deployment

### Environment Variables for Production

Make sure to set all environment variables in your hosting platform:

- Clerk keys for authentication
- Google OAuth credentials for calendar integration
- Sanity project credentials for CMS

### Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme).

Check out the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## License

This project is licensed under the MIT License.
