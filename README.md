# Life Leveling - Level Up Your Real Life

A professional modern mobile application for gamified personal growth. Built with Next.js, React, and Tailwind CSS, featuring a clean design inspired by Duolingo, Strava, and Notion.

## Project Overview

**Life Leveling** is a production-grade gamified personal growth platform. Users complete daily tasks across Fitness, Focus, and Productivity to earn XP, coins, levels, and climb leaderboards. The app features a professional, clean interface with soft shadows, rounded cards, and intuitive navigation—designed as a serious modern mobile product.

## Key Features

### Core Functionality
- **Dashboard/Home** - User profile, XP progress, coins balance, and 3 daily tasks
- **Tasks Screen** - Browse all available tasks with category filtering and difficulty levels
- **Leaderboard** - Global, City, and Friends rankings with real-time rankings
- **Wallet** - Coins management with withdrawal system (Min ₹200), transaction history
- **Profile** - User stats, achievements, level progression, and account settings

### Advanced Features
- **Coin Economy** - 100 coins = ₹10, max 30 coins per day, mystery rewards at milestones
- **XP System** - 100 levels total, 500 XP per level, difficulty scaling from Easy to Elite
- **Teams/Clans** - Create or join teams, track team XP and rankings
- **Friends System** - Add friends, view friend requests, see friend progress
- **Daily Streak** - Streak calendar tracking with milestone rewards at 7, 14, 30, 60 days
- **Commitment Challenges** - Deposit-based earning system with daily task rewards
- **Premium Subscription** - ₹149/month with ad-free, +25% XP gain, premium badge
- **Settings** - Notifications, privacy policy, terms of service, logout
- **Authentication** - Login and signup screens with email/password

## Design System

### Color Palette (Professional & Clean)
- **Background**: `#0F172A` - Deep Navy, minimal distractions
- **Cards**: `#1E293B` - Dark Slate, subtle elevation
- **Primary**: `#6366F1` - Indigo, main brand accent
- **Secondary**: `#22C55E` - Green, success and positive actions
- **Accent**: `#F59E0B` - Amber/Warning, secondary highlights
- **Text**: `#F8FAFC` - Slate White, primary readable text
- **Muted**: `#334155` & `#CBD5E1` - Inactive states

### Visual Design
- **Shadows**: Soft shadows for depth (box-shadow: 0 1px 3px)
- **Borders**: Subtle borders using semantic color variables
- **Rounded Corners**: 0.75rem (12px) for consistent radius
- **Typography**: Geist font family for all text, clean and modern
- **Layout**: Mobile-first, flexbox-based, responsive grid systems
- **No Decorative Effects**: Minimal, production-focused design aesthetic

## Project Structure

```
app/
  page.tsx                 - Main navigation hub with screen routing
  layout.tsx              - Root layout with metadata and fonts
  globals.css             - Design tokens, theme variables, base styles
  
  screens/
    home.tsx              - Dashboard with profile, XP bar, coins, daily tasks
    tasks.tsx             - Task browser with search, category filter, difficulty
    leaderboard.tsx       - Global/City/Friends rankings with user stats
    wallet.tsx            - Coins display, transaction history, withdrawals
    profile.tsx           - User stats, achievements, edit profile, logout
    friends.tsx           - Friend requests, friends list, messaging
    teams.tsx             - Teams list, create team, join team
    daily-streak.tsx      - Streak calendar, milestones, rewards
    commitment-challenge.tsx - Deposit challenges, progress tracking
    settings.tsx          - Preferences, privacy, terms, logout
    premium.tsx           - Subscription pricing, benefits, features
    login.tsx             - Email/password authentication
    signup.tsx            - Registration with full name, email, password

components/
  nav-bar.tsx             - Bottom tab navigation (Home/Tasks/Leaderboard/Wallet/Profile)
  ui/                     - shadcn/ui components (Button, Input, Progress, etc.)

public/
  [assets]                - Icons and static assets
```

## Core Screens

### Home Dashboard
- User avatar and profile card (name, level, XP bar)
- Coins balance display with conversion rate
- Exactly 3 daily tasks showing:
  - Task title and category
  - XP reward and coin reward
  - Complete/Start button
  - Completion status indicator
- Quick stats grid (streak, total XP, rewards)

### Tasks Screen
- Search bar for task filtering
- Category tabs (All, Fitness, Focus, Productivity)
- Task list with:
  - Task title and category badge
  - Difficulty indicator (Easy/Medium/Hard)
  - XP and coin rewards
  - Start button

### Leaderboard
- Tab navigation (Global, City, Friends)
- User rankings with:
  - Rank position (medal for top 3)
  - Avatar/Username
  - Level and total XP
  - Current user highlighted

### Wallet
- Coins balance display
- Conversion rate (100 coins = ₹10)
- Withdrawal form:
  - Amount input (Min ₹200/2000 coins)
  - UPI ID field
  - Submit button
- Transaction history showing type, amount, and date

### Profile
- User card with avatar, name, level
- XP progress bar
- Achievement grid (locked/unlocked badges)
- Stats cards (Total XP, Day Streak, Tasks Done)
- Edit profile and logout buttons

## Configuration

### Design Token Customization
Edit CSS variables in `app/globals.css`:
```css
:root {
  --background: #0F172A;
  --primary: #6366F1;
  --secondary: #22C55E;
  /* ... more tokens ... */
}
```

### Adding New Screens
1. Create component in `app/screens/[name].tsx`
2. Export default function
3. Update `app/page.tsx` switch statement
4. Add navigation tab in `components/nav-bar.tsx` if needed

### Component Usage
All components use shadcn/ui with Tailwind CSS:
```tsx
import { Button } from '@/components/ui/button'
import { Input } from '@/components/ui/input'
import { Progress } from '@/components/ui/progress'
```

## Gamification System

### XP & Levels
- **Total Levels**: 100
- **XP Per Level**: 500 XP required
- **Level Difficulty Tiers**:
  - Levels 1-10: Easy tasks
  - Levels 11-25: Easy+ tasks
  - Levels 26-40: Medium tasks
  - Levels 41-60: Medium+ tasks
  - Levels 61-80: Hard tasks
  - Levels 81-100: Elite tasks

### Coin Economy
- **Conversion**: 100 coins = ₹10 INR
- **Daily Limit**: 30 coins max per day (sustainability)
- **Milestone Rewards**: Mystery coins only at levels 5, 10, 15, 20, 25, 30, 40, 50, 60, 75, 90, 100
- **Reward Range**: 80-120 coins (example)

### Daily Tasks
- Exactly 3 tasks per day
- Categories: Fitness, Focus, Productivity
- Each task shows XP reward and coin reward
- Mark complete or start task

### Streaks
- Daily task completion extends streak
- Calendar visualization of past 28 days
- Milestone bonuses at 7, 14, 30, 60 days

## Technology Stack

- **Framework**: Next.js 16 (React 19)
- **Styling**: Tailwind CSS v4 with semantic design tokens
- **UI Components**: shadcn/ui
- **Icons**: Lucide React
- **Package Manager**: pnpm
- **Language**: TypeScript (optional)

## Getting Started

```bash
# Install dependencies
pnpm install

# Run development server
pnpm dev

# Open http://localhost:3000 in your browser
```

## Project Features

✅ Production-grade mobile UI  
✅ Professional, clean design aesthetic  
✅ Responsive mobile-first layout  
✅ Bottom tab navigation (5 main screens)  
✅ Comprehensive feature set  
✅ Accessible, semantic HTML  
✅ Optimized for iOS and Android  
✅ No backend required (frontend only)

## Mobile Optimization

- Mobile viewport configuration
- Touch-friendly UI elements (min 48px)
- Safe area padding for notched devices
- Responsive typography
- Bottom navigation for thumb access
- Optimized for iOS 12+ and Android 8+

## Future Backend Integration

This frontend is designed to connect with:
- Authentication system (email/password, social login)
- User database and progress storage
- Real-time leaderboard updates
- Push notifications for streaks
- Payment processing (Premium, withdrawals)
- Transaction and analytics tracking
- Friend and team messaging

## Design Principles

1. **Professional & Serious** - Modern product design, not gamified entertainment
2. **Clean & Minimal** - No cartoon visuals or decorative elements
3. **Mobile-First** - Optimized for small screens with bottom navigation
4. **Semantic Design Tokens** - All colors use CSS variables for theming
5. **Accessibility** - WCAG AA contrast, keyboard navigation, screen readers

## License

Created for demonstration as a production-ready frontend template.
