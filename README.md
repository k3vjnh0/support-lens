# SupportLens

An AI-powered support work platform designed to streamline documentation, provide evidence-based guidelines, and enable safe client support through a dual-role system.

## Overview

SupportLens is a comprehensive web application that empowers support workers and their clients through intelligent automation and evidence-based practices. The platform features two distinct portals:

### Support Worker Portal
Professional tools for case documentation and evidence-based support:
- Upload and transcribe session audio with AI-powered risk detection
- Find similar cases and access evidence-based guidelines
- Create structured SOAP notes with citations
- Export comprehensive reports as PDF
- Access a psychoeducation library
- Manage client conversations and cases
- Calendar and scheduling functionality
- Recording management and playback

### Client Portal
Safe, guided access to mental health information and support:
- Secure messaging with support workers
- Guided access to mental health resources
- Protected communication channels

## Technology Stack

This project is built with modern web technologies:

- **Frontend Framework**: React with TypeScript
- **Build Tool**: Vite
- **Styling**: Tailwind CSS
- **UI Components**: shadcn-ui (Radix UI primitives)
- **Backend**: Supabase (Authentication, Database, Edge Functions)
- **State Management**: TanStack React Query
- **Routing**: React Router
- **Form Handling**: React Hook Form with Zod validation
- **Date Management**: date-fns
- **Rich Text**: Lexical Editor
- **Audio Processing**: Wavesurfer.js
- **Charts**: Recharts
- **Icons**: Lucide React

## Getting Started

### Prerequisites

- Node.js (v18 or higher) - [Install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating)
- npm or bun package manager

### Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd role-lens-assist-main
```

2. Install dependencies:
```bash
npm install
# or
bun install
```

3. Set up environment variables:
Create a `.env` file in the root directory with your Supabase credentials:
```env
VITE_SUPABASE_URL=your_supabase_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

4. Start the development server:
```bash
npm run dev
# or
bun run dev
```

The application will be available at `http://localhost:5173`

## Project Structure

```
role-lens-assist-main/
├── src/
│   ├── components/          # React components
│   │   ├── auth/           # Authentication components
│   │   ├── recorder/       # Audio recording functionality
│   │   ├── supportlens/    # Core application components
│   │   └── ui/             # shadcn-ui components
│   ├── hooks/              # Custom React hooks
│   ├── integrations/       # Third-party integrations
│   │   └── supabase/       # Supabase client and queries
│   ├── lib/                # Utility functions and helpers
│   │   ├── audio/          # Audio processing utilities
│   │   ├── auth/           # Authentication logic
│   │   ├── clients/        # Client management
│   │   ├── messages/       # Messaging functionality
│   │   └── recordings/     # Recording management
│   └── pages/              # Application pages/routes
│       ├── auth/           # Authentication pages
│       └── sw/             # Support worker pages
├── supabase/
│   ├── functions/          # Supabase Edge Functions
│   └── migrations/         # Database migrations
└── public/                 # Static assets
```

## Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run build:dev` - Build for development environment
- `npm run lint` - Run ESLint
- `npm run preview` - Preview production build

## Features

### AI-Powered Transcription
Upload audio recordings of support sessions and receive automatic transcription with intelligent risk detection and case similarity analysis.

### Evidence-Based Guidelines
Access relevant research, best practices, and evidence-based guidelines matched to your specific cases.

### SOAP Note Generation
Create structured clinical documentation following the SOAP (Subjective, Objective, Assessment, Plan) format with automatic citation integration.

### Risk Detection
AI-powered analysis identifies potential risk factors and crisis indicators in session transcripts.

### Client Management
Comprehensive client profiles, case tracking, and communication history.

### Secure Messaging
Protected communication channels between support workers and clients.

### Resource Library
Curated psychoeducation materials and resources for both support workers and clients.

## Database Schema

The application uses Supabase PostgreSQL with the following main tables:
- `users` - User authentication and profiles
- `cases` - Client cases and documentation
- `conversations` - Messaging between workers and clients
- `messages` - Individual messages
- `recordings` - Audio recording metadata
- `notes` - Clinical notes and documentation

See `supabase/migrations/` for detailed schema definitions.

## Deployment

### Build for Production

```bash
npm run build
```

The built files will be in the `dist/` directory.

### Deployment Options

This application can be deployed to:
- Vercel
- Netlify
- AWS Amplify
- Any static hosting service

Ensure environment variables are properly configured in your hosting platform.

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is proprietary and confidential.

## Support

For support and questions, please contact the development team.
