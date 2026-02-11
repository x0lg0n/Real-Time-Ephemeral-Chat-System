# 🔥 Real-Time Ephemeral Chat System

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Next.js](https://img.shields.io/badge/Next.js-16.0.7-black)](https://nextjs.org)
[![React](https://img.shields.io/badge/React-19.2.1-blue)](https://react.dev)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9.3-blue)](https://www.typescriptlang.org)

A secure, real-time chat application with self-destructing rooms built using Next.js, TypeScript, and Upstash services.

## 🌟 Features

- **🔒 Ephemeral Messaging**: Chat rooms automatically destroy themselves after use
- **⚡ Real-time Communication**: Powered by Upstash Realtime
- **🛡️ Anonymous Chat**: No user registration required - temporary identities
- **📱 Responsive Design**: Works seamlessly across all devices
- **🎨 Modern UI**: Clean, dark-themed interface with Tailwind CSS
- **📦 Type Safety**: Full TypeScript support throughout
- **⚡ Fast Performance**: Optimized with Next.js 16 and React Server Components

## 🚀 Tech Stack

- **Frontend**: [Next.js 16](https://nextjs.org) with App Router
- **Language**: [TypeScript](https://www.typescriptlang.org)
- **Styling**: [Tailwind CSS](https://tailwindcss.com)
- **State Management**: [React Query](https://tanstack.com/query)
- **Real-time**: [Upstash Realtime](https://upstash.com/docs/realtime)
- **Data Storage**: [Upstash Redis](https://upstash.com/docs/redis)
- **API Framework**: [Elysia.js](https://elysiajs.com)
- **Validation**: [Zod](https://zod.dev)

## 📋 Prerequisites

- Node.js 18+ or Bun
- npm, yarn, pnpm, or bun package manager
- Upstash account (for Redis and Realtime services)

## 🗝️ Environment Variables

This project requires several environment variables to function properly. These variables configure connections to external services and control various aspects of the application.

### Required Services

1. **Upstash Redis** - For storing chat room data and session information
2. **Upstash Realtime** - For real-time messaging functionality

### Setting up Environment Variables

1. Create a `.env.local` file in the project root directory
2. Add the following variables:

```env
# Upstash Redis Configuration
UPSTASH_REDIS_REST_URL=your_redis_rest_url
UPSTASH_REDIS_REST_TOKEN=your_redis_rest_token

# Upstash Realtime Configuration  
UPSTASH_REALTIME_URL=your_realtime_url
UPSTASH_REALTIME_TOKEN=your_realtime_token

# Application Settings
NEXT_PUBLIC_APP_URL=http://localhost:3000
ROOM_EXPIRY_TIME=3600  # Room expiry time in seconds
```

### How to Obtain Service Credentials

#### Upstash Redis

1. Sign up at [Upstash Console](https://console.upstash.com)
2. Create a new Redis database
3. Copy the REST URL and token from the database dashboard
4. Add them to your environment variables as `UPSTASH_REDIS_REST_URL` and `UPSTASH_REDIS_REST_TOKEN`

#### Upstash Realtime

1. In your Upstash console, navigate to the Realtime section
2. Create a new Realtime database
3. Copy the URL and token from the database dashboard
4. Add them to your environment variables as `UPSTASH_REALTIME_URL` and `UPSTASH_REALTIME_TOKEN`

### Environment Variable Details

| Variable | Description | Example |

|----------|-------------|---------|
| `UPSTASH_REDIS_REST_URL` | REST endpoint for your Redis database | `https://us1-your-database-12345.upstash.io` |
| `UPSTASH_REDIS_REST_TOKEN` | Authentication token for Redis | `AXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX` |
| `UPSTASH_REALTIME_URL` | WebSocket endpoint for Realtime service | `wss://your-realtime.upstash.io` |
| `UPSTASH_REALTIME_TOKEN` | Authentication token for Realtime | `eyXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX` |
| `NEXT_PUBLIC_APP_URL` | Public URL of your application | `http://localhost:3000` |
| `ROOM_EXPIRY_TIME` | Time in seconds before rooms expire | `3600` (1 hour) |

> **Note**: Never commit your `.env.local` file to version control. It's already included in the `.gitignore` file.

## 🛠️ Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/x0lg0n/Real-Time-Ephemeral-Chat-System
   cd real-time-ephemeral-chat-system
   ```

2. **Install dependencies**

   ```bash
   # Using npm
   npm install
   
   # Using yarn
   yarn install
   
   # Using pnpm
   pnpm install
   
   # Using bun
   bun install
   ```

3. **Environment Setup**

   Create a `.env.local` file in the root directory:

   ```env
   # Upstash Redis Configuration
   UPSTASH_REDIS_REST_URL=your_redis_rest_url
   UPSTASH_REDIS_REST_TOKEN=your_redis_rest_token
   
   # Upstash Realtime Configuration
   UPSTASH_REALTIME_URL=your_realtime_url
   UPSTASH_REALTIME_TOKEN=your_realtime_token
   
   # Application Settings
   NEXT_PUBLIC_APP_URL=http://localhost:3000
   ROOM_EXPIRY_TIME=3600  # Room expiry time in seconds
   ```

4. **Run the development server**

   ```bash
   npm run dev
   # or
   yarn dev
   # or
   pnpm dev
   # or
   bun dev
   ```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 📖 Usage

1. **Create a Chat Room**
   - Visit the homepage
   - Your temporary identity will be generated automatically
   - Click "CREATE SECURE ROOM" to start a new chat session

2. **Share the Room**
   - Copy the room URL and share it with participants
   - Anyone with the link can join the chat

3. **Chat Features**
   - Real-time messaging between participants
   - Messages are encrypted in transit
   - Room automatically expires after the set time period
   - All messages are permanently deleted when the room expires

4. **Room Expiry**
   - Rooms automatically self-destruct after the configured time
   - All data is permanently removed from the system
   - No data retention beyond room lifetime

## 🏗️ Project Structure

```folder
real-time-ephemeral-chat-system/
├── src/
│   ├── app/                    # Next.js app router
│   │   ├── api/                # API routes
│   │   ├── room/[roomId]/      # Room page
│   │   ├── layout.tsx          # Root layout
│   │   └── page.tsx            # Home page
│   ├── components/             # React components
│   ├── hooks/                  # Custom hooks
│   └── lib/                    # Utility libraries
├── public/                     # Static assets
├── elysia/                     # API server (separate)
├── README.md
└── package.json
```

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 🎯 Contributing

We welcome contributions from the community! Here's how you can help make this project better:

### 🚀 Getting Started

1. **Fork the Repository**
   - Click the "Fork" button at the top right of this repository
   - Clone your forked repository to your local machine
   git clone https://github.com/your-username/real-time-ephemeral-chat-system.git
   cd real-time-ephemeral-chat-system

2. **Set Up Development Environment**
   - Install dependencies: `npm install`
   - Create your `.env.local` file (see Environment Variables section)
   - Start the development server: `npm run dev`

3. **Create a Feature Branch**
   git checkout -b feature/your-feature-name
   Use descriptive branch names like:
   - `feature/add-user-authentication`
   - `bugfix/fix-room-expiry-issue`
   - `enhancement/improve-ui-components`

### 📝 Development Guidelines

**Code Quality Standards:**
- ✅ Use TypeScript for all new code
- ✅ Follow the existing ESLint configuration
- ✅ Write clear, descriptive commit messages
- ✅ Include tests for new functionality
- ✅ Ensure all existing tests pass before submitting

**Commit Message Format:**
type(scope): brief description

Detailed explanation of changes (optional)

- Specific changes made
- Reason for changes
- Impact on functionality

Resolves: #issue-number (if applicable)

**Commit Types:**
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or modifying tests
- `chore`: Maintenance tasks

### 🔄 Submission Process

1. **Before Pushing:**

   # Run code quality checks

   npm run lint
   npm run build

   # Ensure all tests pass

   npm test

2. **Push Your Changes:**
   git push origin feature/your-feature-name

3. **Create Pull Request:**
   - Go to your fork on GitHub
   - Click "New Pull Request"
   - Select your feature branch
   - Provide a clear title and detailed description
   - Link any related issues

### 🎯 What We're Looking For

**Areas for Contribution:**

- 🐛 Bug fixes and performance improvements
- ✨ New features and enhancements
- 📚 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test coverage expansion
- 📱 Mobile responsiveness improvements

**Good First Issues:**
Check our [GitHub Issues](https://github.com/your-username/real-time-ephemeral-chat-system/issues) for issues labeled `good first issue` or `help wanted`.

### 🤝 Community Guidelines

- Be respectful and inclusive
- Provide constructive feedback
- Help others learn and grow
- Follow our [Code of Conduct](CODE_OF_CONDUCT.md)
- Ask questions in our [Discussions](https://github.com/your-username/real-time-ephemeral-chat-system/discussions)

### 📋 Pull Request Review Process

1. **Initial Review**: Maintainers will review your PR within 48 hours
2. **Feedback**: Address any requested changes
3. **Approval**: Once approved, your PR will be merged
4. **Celebration**: 🎉 Your contribution is now part of the project!

### 🆘 Need Help?

- Check our [Documentation](docs/)
- Join our [Discord Community](link-to-discord)
- Create a [GitHub Discussion](https://github.com/your-username/real-time-ephemeral-chat-system/discussions)
- Contact maintainers via email

Thank you for contributing to make this project amazing! 🚀

### Code Quality Standards

- Use TypeScript for all new code
- Follow ESLint configuration
- Write meaningful commit messages
- Include tests for new functionality
- Ensure all existing tests pass

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, questions, or feature requests:

- Create an issue in the [GitHub Issues](https://github.com/your-username/real-time-ephemeral-chat-system/issues)
- Contact the maintainer via email

## 💙 Acknowledgements

- [Next.js](https://nextjs.org) - React framework
- [Upstash](https://upstash.com) - Redis and Realtime services
- [Tailwind CSS](https://tailwindcss.com) - Styling framework
- [React Query](https://tanstack.com/query) - Server state management
- [Elysia.js](https://elysiajs.com) - API framework

---

<p align="center">Made with ❤️ and ☕</p>
