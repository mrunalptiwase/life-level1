# Life Leveling - Quick Start Guide

## Installation & Setup

### Prerequisites
- Node.js 18+ or 20+
- pnpm (recommended) or npm

### 1. Install Dependencies
```bash
pnpm install
```

### 2. Run Development Server
```bash
pnpm dev
```

### 3. Open in Browser
Navigate to `http://localhost:3000`

The app will load with the **Home** screen by default.

## Navigating the App

### Bottom Tab Navigation
The app has 5 main screens accessible via the bottom tab bar:

| Tab | Screen | Description |
|-----|--------|-------------|
| 🏠 Home | Dashboard | Profile, XP bar, coins, daily tasks |
| 📋 Tasks | Task Browser | Browse all tasks, filter by category |
| 🏆 Leaderboard | Rankings | Global/City/Friends rankings |
| 💳 Wallet | Coins | Manage coins, withdrawal, history |
| 👤 Profile | User Profile | Stats, achievements, account |

Simply tap any tab at the bottom to navigate to that screen.

## Screen Overview

### Home Dashboard
- **View your profile** - Avatar, name, level
- **Track XP progress** - Progress bar showing current/max XP
- **Check coins balance** - Current coins and conversion rate (100 coins = ₹10)
- **Complete daily tasks** - 3 daily tasks available (Fitness, Focus, Productivity)
- **Quick stats** - Day streak, total XP, rewards count

### Tasks Browser
- **Search tasks** - Find specific tasks by name
- **Filter by category** - All, Fitness, Focus, Productivity
- **View task details** - Title, difficulty, rewards
- **Start tasks** - Begin a task with one tap

### Leaderboard
- **Global rankings** - Worldwide user rankings
- **City rankings** - Local rankings by city
- **Friends rankings** - See how you rank vs friends
- **View medals** - 🥇🥈🥉 for top 3 users
- **Your position** - Highlighted with "You" badge

### Wallet
- **Coins balance** - Your current coin count
- **Conversion rate** - See rupee equivalent
- **Withdraw coins** - Request withdrawal (min ₹200)
- **Transaction history** - All coin transactions with dates

### Profile
- **User info** - Name, avatar, level
- **XP progress** - Progress bar to next level
- **Statistics** - Total XP, day streak, tasks completed
- **Achievements** - Unlocked and locked badges
- **Account actions** - Edit profile, logout

## Features to Explore

### Gamification System
- **Levels** - Progress from Level 1 to 100
- **XP** - Earn XP from tasks (500 XP = 1 level)
- **Coins** - Earn coins from task rewards
- **Streaks** - Maintain daily login streaks
- **Achievements** - Unlock badges for milestones

### Task Categories
1. **Fitness** - Health and exercise challenges
2. **Focus** - Learning and concentration tasks
3. **Productivity** - Work and personal development

### Social Features
- **Friends** - Add and manage friends
- **Teams** - Create or join teams
- **Rankings** - Compete on leaderboards
- **Achievements** - Unlock exclusive badges

## Sample Data

All screens include sample data:
- **User Profile** - Alex Kumar, Level 12, 1,450 XP
- **Daily Tasks** - 3 tasks: Pushups, Reading, Meditation
- **Leaderboard** - 6 users with rankings
- **Friends** - 4 friends to connect with
- **Achievements** - 6 achievement badges

## Customization

### Change Colors
Edit `app/globals.css`:
```css
:root {
  --background: #0F172A;
  --primary: #6366F1;
  --secondary: #22C55E;
  /* ... more colors ... */
}
```

### Add New Screen
1. Create `app/screens/new-screen.tsx`
2. Export default component
3. Add to `app/page.tsx` switch statement
4. Add tab in `components/nav-bar.tsx`

### Modify Navigation
Edit `components/nav-bar.tsx` to change:
- Tab labels
- Icons (from lucide-react)
- Tab order
- Colors

## Common Tasks

### View a Different Screen
Tap the desired tab at the bottom of the screen.

### Search for a Task
Go to **Tasks** → Use search bar → Type task name

### Filter Tasks by Category
Go to **Tasks** → Tap category tab (All, Fitness, Focus, Productivity)

### Check Your Rank
Go to **Leaderboard** → Select ranking type (Global, City, Friends)

### Start a Task
Go to **Home** or **Tasks** → Tap "Start" button on any task

### Withdraw Coins
Go to **Wallet** → Tap "Withdraw" → Enter amount and UPI → Submit

### View Achievements
Go to **Profile** → Scroll to "Achievements" section

## Performance Tips

- All screens load instantly
- No backend required (frontend only)
- Responsive on all devices
- Optimized for mobile

## Troubleshooting

### Screen not loading?
- Clear browser cache
- Refresh the page (Cmd+R or Ctrl+R)
- Check console for errors (F12)

### Navigation not working?
- Make sure JavaScript is enabled
- Check that you're using a modern browser
- Try a different browser

### Styling looks odd?
- Clear CSS cache
- Refresh hard (Cmd+Shift+R or Ctrl+Shift+R)
- Check that Tailwind CSS is loading

## Browser Support

✅ Works on:
- Chrome (latest)
- Safari (latest)  
- Firefox (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Next Steps

1. **Explore all screens** - Navigate through tabs to see all features
2. **Try interactions** - Click buttons, fill forms, toggle tabs
3. **Customize design** - Change colors and fonts
4. **Add backend** - Connect to your API for real data
5. **Deploy** - Use Vercel, Netlify, or any hosting service

## Resources

- **Documentation**: See `README.md` for detailed docs
- **Implementation**: See `IMPLEMENTATION.md` for technical details
- **Source Code**: All code in `app/` and `components/` folders

## Support

For issues or questions:
1. Check the source code in `app/screens/`
2. Review `README.md` for architecture details
3. Check component usage in other screens
4. Verify all dependencies are installed (`pnpm install`)

---

Enjoy exploring Life Leveling! 🚀
