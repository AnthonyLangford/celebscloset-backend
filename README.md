# CelebsCloset - Social Commerce Platform

A luxury social commerce platform combining the best features of TikTok, Instagram, Facebook, and YouTube with a marketplace for fashion, accessories, entertainment, real estate, and automotive.

## Features

### Core Features
- **User Authentication** - JWT-based auth with CEO master key access
- **Social Feed** - Post photos, videos, and stories
- **Marketplace** - Buy/sell fashion, accessories, real estate, automotive
- **Auction System** - Bid on exclusive celebrity items
- **Entertainment** - Watch reels and stories
- **Celebrity Spotlight** - Real celebrity profiles with Instagram links
- **Real-time Messaging** - Chat with other users via Socket.io
- **AI Assistant "Nana"** - Voice-activated Siri-like assistant
- **Payment System** - Stripe integration for secure transactions

### Celebrity Rotation Bar
15 real American celebrities with:
- Real Instagram, Twitter, and Facebook links
- Follower counts and net worth
- Professional photos and bios
- Direct social media navigation

### AI Assistant Nana
- **Wake Word**: Say "Hey Nana" to activate
- **Voice Responses**: OpenAI TTS integration
- **Smart Search**: Find products, celebrities, and content
- **Navigation**: Navigate the app via voice commands

### Payment System
- **Stripe Integration** - Secure payment processing
- **Send/Receive Money** - User-to-user transfers
- **10% Platform Fee** - Automatically deducted
- **Event Tickets** - Purchase celebrity event tickets

## Tech Stack

### Frontend
- React 19 + TypeScript
- Tailwind CSS + shadcn/ui
- Vite build tool
- Socket.io-client

### Backend
- Node.js + Express
- MongoDB + Mongoose
- Socket.io for real-time features
- JWT authentication
- OpenAI API for Nana voice
- Stripe API for payments
- AWS S3 for video storage

## Getting Started

### Prerequisites
- Node.js 18+
- MongoDB Atlas account
- OpenAI API key
- Stripe account
- AWS S3 bucket (optional, for video uploads)

### Installation

1. Clone the repository:
```bash
git clone <repo-url>
cd celebscloset
```

2. Install dependencies:
```bash
npm install
```

3. Configure environment variables in `.env`:
```env
NODE_ENV=development
PORT=5000
CLIENT_URL=http://localhost:5173
MONGODB_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
OPENAI_API_KEY=your_openai_key
STRIPE_SECRET_KEY=your_stripe_secret
STRIPE_PUBLISHABLE_KEY=your_stripe_publishable
AWS_ACCESS_KEY_ID=your_aws_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
AWS_S3_BUCKET=your_bucket_name
CEO_MASTER_KEY=ANTHONYL123456
```

### Running the App

**Development mode (frontend + backend):**
```bash
npm run dev
```

**Build for production:**
```bash
npm run build
```

**Start production server:**
```bash
npm start
```

## CEO Access

Master Key: `ANTHONYL123456`

Login with:
- Username: `anthony` or `anthony.langford`
- Master Key: `ANTHONYL123456`

CEO privileges:
- Access to Admin Dashboard
- User management
- Platform analytics
- Commission tracking

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/ceo-login` - CEO master key login

### Users
- `GET /api/users/profile` - Get user profile
- `PUT /api/users/profile` - Update profile
- `GET /api/users/:id` - Get user by ID

### Posts
- `GET /api/posts` - Get feed posts
- `POST /api/posts` - Create post
- `POST /api/posts/:id/like` - Like post
- `POST /api/posts/:id/comment` - Comment on post

### Videos
- `GET /api/videos/reels` - Get video reels
- `GET /api/videos/stories` - Get stories
- `POST /api/videos/upload` - Upload video
- `POST /api/videos/:id/like` - Like video
- `POST /api/videos/:id/share` - Share video

### Marketplace
- `GET /api/products` - Get products
- `POST /api/products` - Create listing
- `POST /api/products/:id/bid` - Place bid
- `POST /api/products/:id/buy` - Buy now

### Celebrities
- `GET /api/celebrities` - Get all celebrities
- `GET /api/celebrities/featured` - Get featured celebrities
- `POST /api/celebrities/init` - Initialize celebrity data

### AI (Nana)
- `POST /api/ai/ask` - Ask Nana a question
- `POST /api/ai/speak` - Generate voice response
- `POST /api/ai/wake` - Wake word detection

### Payments
- `POST /api/payments/create-intent` - Create payment intent
- `POST /api/payments/send` - Send money to user
- `GET /api/payments/balance` - Get user balance

### Messages
- `GET /api/messages` - Get conversations
- `GET /api/messages/:userId` - Get messages with user
- `POST /api/messages` - Send message

## Social Sharing

Share content to:
- **Facebook** - Direct share via Facebook Share Dialog
- **Twitter** - Tweet with pre-filled content
- **Instagram** - Copy link to clipboard

## Voice Commands for Nana

Say "Hey Nana" followed by:
- "Find fashion items" - Browse fashion marketplace
- "Show me celebrities" - View celebrity profiles
- "Watch reels" - Go to entertainment
- "Send a message" - Open messages
- "Check my balance" - View payment balance
- "Sell my items" - Create a listing

## Deployment

### Frontend (Static)
The frontend is deployed at:
**https://ewbxe6jhh5b7o.ok.kimi.link**

### Backend (Node.js)
To deploy the backend:
1. Set up a Node.js hosting service (Render, Railway, Heroku)
2. Configure environment variables
3. Run `npm start` to start the server

### Database
Set up MongoDB Atlas:
1. Create a free cluster
2. Add your IP to the whitelist
3. Get the connection string
4. Add to `MONGODB_URI` in .env

## File Structure

```
celebscloset/
├── backend/
│   ├── middleware/     # Auth middleware
│   ├── models/         # MongoDB models
│   ├── routes/         # API routes
│   ├── server.ts       # Main server file
│   └── types.d.ts      # Type definitions
├── src/
│   ├── components/     # React components
│   ├── context/        # React contexts
│   ├── hooks/          # Custom hooks
│   ├── lib/            # Utilities
│   ├── pages/          # Page components
│   └── App.tsx         # Main app component
├── public/             # Static assets
└── dist/               # Build output
```

## License

Private - For Anthony Langford / CelebsCloset
