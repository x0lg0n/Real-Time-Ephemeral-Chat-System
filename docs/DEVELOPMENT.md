# Development Setup Guide

## Prerequisites

Before you begin, ensure you have the following installed:

- Node.js 18+ or Bun
- Git
- Code editor (VS Code recommended)

## Initial Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/your-username/real-time-ephemeral-chat-system.git
   cd real-time-ephemeral-chat-system
   ```

2. **Install dependencies**

   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   # or
   bun install
   ```

3. **Set up environment variables**

   ```bash
   cp .env.example .env.local
   ```

   Edit `.env.local` with your Upstash credentials:
   - Redis REST URL and token
   - Realtime URL and token

4. **Start the development server**

   ```bash
   npm run dev
   ```

5. **Open your browser**
   Visit [http://localhost:3000](http://localhost:3000)

## Project Structure Overview

```folder
src/
├── app/                    # Next.js App Router
│   ├── api/               # API routes
│   ├── room/[roomId]/     # Dynamic room pages
│   ├── layout.tsx         # Root layout
│   └── page.tsx           # Homepage
├── components/            # React components
├── hooks/                 # Custom React hooks
└── lib/                   # Utility libraries
```

## Development Workflow

### Creating New Features

1. Create a feature branch:

   ```bash
   git checkout -b feature/your-feature-name
   ```

2. Make your changes following the coding standards

3. Run tests:

   ```bash
   npm run test
   ```

4. Check linting:

   ```bash
   npm run lint
   ```

5. Commit your changes:

   ```bash
   git add .
   git commit -m "feat: add your feature description"
   ```

### Code Quality Checks

- **TypeScript**: All code should be properly typed
- **ESLint**: Run `npm run lint` to check for issues
- **Formatting**: Use Prettier for consistent formatting
- **Testing**: Write tests for new functionality

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run test` - Run tests (when implemented)

## API Development

The API is built with Elysia.js and can be found in the `elysia/` directory.

To work on the API:

```bash
cd elysia/app
npm install
npm run dev
```

## Database Setup

This project uses Upstash Redis for data storage. You'll need to:

1. Create an Upstash account
2. Create a Redis database
3. Get your REST URL and token
4. Add them to your `.env.local` file

## Common Development Tasks

### Adding a New Component

1. Create the component file in `src/components/`
2. Export it properly
3. Add TypeScript interfaces for props
4. Write tests if applicable

### Creating API Routes

1. Add new routes in `src/app/api/`
2. Follow the existing pattern
3. Use proper error handling
4. Add validation with Zod

### Styling

- Use Tailwind CSS utility classes
- Follow the existing color palette
- Maintain responsive design principles

## Troubleshooting

### Common Issues

1. **Environment variables not loading**
   - Ensure `.env.local` exists
   - Restart the development server
   - Check variable names match exactly

2. **TypeScript errors**
   - Run `npm run build` to see all type errors
   - Check that all imports are correct
   - Ensure proper typing of props and state

3. **API connection issues**
   - Verify Upstash credentials
   - Check network connectivity
   - Ensure CORS is properly configured

### Getting Help

- Check the [README.md](../README.md) for general information
- Review [CONTRIBUTING.md](../CONTRIBUTING.md) for contribution guidelines
- Create an issue on GitHub for bugs or feature requests
