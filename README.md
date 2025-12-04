# Spott 🎉

**Discover & Create Amazing Events**

Spott is a modern event discovery and creation platform that connects event organizers with attendees. Whether you're hosting a concert, conference, workshop, or community meetup, Spott makes every event memorable.

[Live Demo](#) • [Documentation](#) • [Report Bug](#) • [Request Feature](#)

---

## ✨ Features

### For Attendees

- 🔍 **Smart Event Discovery** - Find events based on your location and interests
- 🎯 **Personalized Recommendations** - Get featured and popular events tailored to you
- 📍 **Location-Based Search** - Discover local events in your city
- 🏷️ **Category Filtering** - Browse events across multiple categories
- 📱 **Responsive Design** - Seamless experience on desktop and mobile

### For Organizers

- 🎪 **Easy Event Creation** - Intuitive forms for creating and managing events
- 🎨 **Customization** - Theme colors and cover images for branding
- 📊 **Capacity Management** - Set event capacity and track registrations
- 💳 **Flexible Ticketing** - Support for both free and paid events
- 🌍 **Global Reach** - Create events for physical or online audiences
- 🏆 **Free & Premium** - Start with 1 free event, upgrade for more

### Core Capabilities

- 🔐 **Secure Authentication** - Clerk-powered authentication
- 🗺️ **Geolocation Support** - City/state/country-based event organization
- 📅 **Smart Scheduling** - Timezone-aware event management
- 🔗 **QR Code Integration** - Built-in QR code generation and scanning
- 🌙 **Dark Mode Support** - Theme switching with next-themes
- 🔍 **Full-Text Search** - Search events by title
- 🤖 **AI Assistance** - Google Generative AI integration for enhanced features

---

## 🛠️ Tech Stack

### Frontend

- **Next.js 16** - React framework with App Router
- **React 19** - UI library
- **TypeScript/JavaScript** - Type-safe development
- **Tailwind CSS 4** - Utility-first CSS framework
- **Radix UI** - Unstyled, accessible component primitives
- **React Hook Form** - Efficient form state management
- **Zod** - TypeScript-first schema validation

### Backend & Database

- **Convex** - Real-time backend-as-a-service platform
- **Clerk** - Authentication and user management
- **Google Generative AI** - AI capabilities

### Key Libraries

- **Lucide React** - Beautiful icon library
- **Date-fns** - Modern date utility library
- **Embla Carousel** - Headless carousel library
- **React Spinners** - Loading indicators
- **Sonner** - Toast notifications
- **html5-qrcode** - QR code scanning
- **react-qr-code** - QR code generation
- **Country-State-City** - Location data
- **Lodash** - Utility functions

---

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** 18+ and npm/yarn
- **Git** for version control
- A **Clerk** account for authentication
- A **Convex** account for backend services
- A **Google API key** for AI features (optional)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/arsh-kodr/spott.git
cd spott
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env.local` file in the root directory:

```env
# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key

# Convex Backend
NEXT_PUBLIC_CONVEX_URL=your_convex_url
CONVEX_DEPLOYMENT=your_convex_deployment

# Google Generative AI
GOOGLE_GENERATIVE_AI_KEY=your_google_ai_key

# Optional: Proxy settings
PROXY_URL=your_proxy_url
```

### 4. Set Up Convex

Initialize and deploy your Convex schema:

```bash
npx convex dev
```

This will sync your database schema and allow real-time sync during development.

### 5. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser. The app will automatically reload as you make changes.

---

## 📁 Project Structure

```
spott/
├── app/                      # Next.js App Router
│   ├── (auth)/              # Authentication pages
│   │   ├── sign-in/
│   │   └── sign-up/
│   ├── (public)/            # Public routes
│   │   └── explore/         # Event exploration
│   ├── (main)/              # Main authenticated routes
│   ├── layout.js            # Root layout
│   ├── page.js              # Landing page
│   └── globals.css          # Global styles
├── components/              # Reusable React components
│   ├── ui/                  # Radix UI components
│   ├── event-card.jsx       # Event display component
│   ├── header.jsx           # Navigation header
│   └── onboarding-modal.jsx # User onboarding flow
├── convex/                  # Backend functions & database
│   ├── schema.js            # Database schema
│   ├── users.js             # User queries & mutations
│   ├── explore.js           # Event discovery queries
│   ├── auth.config.js       # Authentication config
│   └── _generated/          # Auto-generated Convex types
├── hooks/                   # Custom React hooks
│   ├── use-convex-query.jsx # Convex query hook
│   ├── use-onboarding.jsx   # Onboarding logic
│   └── use-store-user.jsx   # User state management
├── lib/                     # Utility functions
│   ├── location-utils.js    # Location helpers
│   ├── data.js              # Static data & constants
│   └── utils.js             # General utilities
└── public/                  # Static assets
```

---

## 📚 Key Pages & Routes

| Route             | Description                          |
| ----------------- | ------------------------------------ |
| `/`               | Landing page with hero section       |
| `/explore`        | Event discovery with recommendations |
| `/explore/[slug]` | Detailed event view                  |
| `/sign-in`        | User authentication (Clerk)          |
| `/sign-up`        | New user registration (Clerk)        |

---

## 🔧 Available Scripts

```bash
# Development
npm run dev          # Start dev server with hot reload

# Production
npm run build        # Build for production
npm start           # Start production server

# Code Quality
npm run lint        # Run ESLint
```

---

## 📖 Usage Examples

### Exploring Events

Visit the `/explore` page to:

- See featured events in a carousel
- View local events based on your location
- Browse popular events across all categories
- Filter by event category

### Creating an Event

1. Sign up or log in with Clerk
2. Complete onboarding to set preferences
3. Navigate to event creation
4. Fill in event details (title, description, date, location)
5. Choose event type (physical or online)
6. Set capacity and ticketing options
7. Customize with cover image and theme color
8. Publish and share with attendees

### QR Code Integration

Events can include QR codes for:

- Ticket verification
- Quick event link sharing
- Contact-less registration

---

## 🗄️ Database Schema

### Users Table

- Email, name, profile image (Clerk integration)
- Onboarding status and user preferences
- Location (city, state, country)
- Interests (event categories)
- Event creation quota tracking

### Events Table

- Event details (title, description, category, tags)
- Organizer information
- Date, time, timezone
- Location (physical address or online)
- Capacity and registration count
- Ticketing configuration
- Customization (cover image, theme color)

### Registrations Table

- Tracks attendee registrations
- Ticket information
- Check-in status

---

## 🔐 Authentication

This project uses **Clerk** for authentication:

- Secure sign-up and sign-in flows
- Social login integration
- User profile management
- Session management

Configure Clerk in `convex/auth.config.js`.

---

## 🚀 Deployment

### Deploy on Vercel

The easiest way to deploy is using [Vercel](https://vercel.com):

1. Push your code to GitHub
2. Import your repository on Vercel
3. Set environment variables in Vercel dashboard
4. Deploy with a single click

[Vercel Deployment Guide](https://nextjs.org/docs/app/building-your-application/deploying)

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 💬 Support & Feedback

- 🐛 **Found a bug?** [Open an issue](https://github.com/arsh-kodr/spott/issues)
- 💡 **Have a feature request?** [Start a discussion](https://github.com/arsh-kodr/spott/discussions)
- 📧 **Need help?** Reach out to the maintainers

---

## 📚 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Convex Documentation](https://docs.convex.dev)
- [Clerk Documentation](https://clerk.com/docs)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Radix UI Documentation](https://www.radix-ui.com/docs)

---

**Made with ❤️ by [Arsh Kodr](https://github.com/arsh-kodr)**
