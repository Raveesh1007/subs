# Resubs - Subscription Tracking Platform

Resubs is a modern, fast, and efficient subscription tracking platform that helps you manage and monitor your various digital subscriptions like Netflix, ChatGPT, YouTube, Spotify, and Apple services. Built with performance in mind, Resubs is hosted on Cloudflare's edge network and utilizes Cloudflare D1 for lightning-fast database operations.

## ✨ Features

- 📊 Track multiple subscriptions from popular platforms
- 📅 Visual calendar interface for easy subscription management
- 📈 Analytics dashboard to monitor spending patterns
- ⚡ Fast and responsive design powered by Next.js and Cloudflare
- 🔐 Secure authentication using NextAuth.js
- 💸 Monitor your subscription spending
- 🔔 Get insights into your subscription patterns

## 🛠️ Tech Stack

- **Frontend**: Next.js, React, TypeScript
- **Hosting**: Cloudflare Pages
- **Database**: Cloudflare D1
- **Authentication**: NextAuth.js
- **Styling**: Tailwind CSS
- **ORM**: Drizzle ORM
- **Package Manager**: pnpm

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ 
- pnpm
- Cloudflare account

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Raveesh1007/resubs.git
   cd resubs
   ```

2. **Install dependencies:**
   ```bash
   pnpm install
   ```

3. **Set up environment variables:**
   Create a `.dev.vars` file in the root directory:
   ```bash
   AUTH_SECRET=your_auth_secret_here
   AUTH_GOOGLE_ID=your_google_oauth_id
   AUTH_GOOGLE_SECRET=your_google_oauth_secret
   ```

## ☁️ Cloudflare Setup

1. **Login to Wrangler:**
   ```bash
   pnpm wrangler login
   ```

2. **Create a D1 database:**
   ```bash
   pnpm wrangler d1 create subs-db
   ```

3. **Update `wrangler.toml`** with your database ID

4. **Run migrations:**
   ```bash
   # Local development
   pnpm run db:migrate:local
   
   # Production
   pnpm run db:migrate:prod
   ```

## 🔑 Authentication Setup

1. **Create Google OAuth credentials:**
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select existing
   - Enable Google+ API
   - Create OAuth 2.0 credentials
   - Add your domain to authorized origins

2. **Generate AUTH_SECRET:**
   ```bash
   openssl rand -base64 32
   ```

3. **Add secrets to Cloudflare Pages:**
   - `AUTH_SECRET`
   - `AUTH_GOOGLE_ID`
   - `AUTH_GOOGLE_SECRET`

## 🏃‍♂️ Development

### Local Development

```bash
# Start development server
pnpm run dev

# Open database studio
pnpm run db:studio

# Generate database migrations
pnpm run db:generate
```

### Available Scripts

- `pnpm dev` - Start development server
- `pnpm build` - Build for production
- `pnpm deploy` - Deploy to Cloudflare Pages
- `pnpm db:generate` - Generate database migrations
- `pnpm db:studio` - Open Drizzle Studio
- `pnpm lint` - Run linter
- `pnpm format` - Format code

## 🚀 Deployment

Deploy to Cloudflare Pages:

```bash
pnpm run deploy
```


## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Next.js](https://nextjs.org/)
- Powered by [Cloudflare](https://cloudflare.com/)
- Styled with [Tailwind CSS](https://tailwindcss.com/)
- Icons from [Lucide](https://lucide.dev/)

---

<p align="center">Made with ❤️ by <a href="https://github.com/Raveesh1007">Raveesh</a></p>

