# Life Leveling - Screen Reference Guide

## App Navigation Structure

```
┌─────────────────────────────────────┐
│         Life Leveling App           │
├─────────────────────────────────────┤
│                                     │
│        [SCREEN CONTENT]             │
│                                     │
│                                     │
│                                     │
├─────────────────────────────────────┤
│ [Home] [Tasks] [Lead] [Wallet] [Me] │  ← Bottom Tab Navigation
└─────────────────────────────────────┘
```

## Screen Details

### 1. HOME DASHBOARD
**File**: `app/screens/home.tsx`

```
┌────────────────────────────┐
│ 👤 Alex Kumar    [Level 12]│ ← Profile Card
│                       750💰 │
├────────────────────────────┤
│ XP Progress                │
│ ████████░░ 1450/2000 XP    │ ← Progress Bar
├────────────────────────────┤
│ 💰 Coins Balance           │
│ 750 coins = ₹75            │
│ [Withdraw] [View Rewards]  │ ← Action Buttons
├────────────────────────────┤
│ Daily Tasks (3 available)  │
│ ┌──────────────────────┐   │
│ │ 💪 Pushups ×20       │   │ ← Task Card
│ │ Fitness              │   │
│ │ ⚡50 XP  +10💰       │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 📚 Read 10 minutes   │   │
│ │ Focus  [✓ Done]      │   │
│ │ ⚡40 XP  +8💰        │   │
│ │              [Done]  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🧘 Meditate 5 min    │   │
│ │ Productivity         │   │
│ │ ⚡30 XP  +6💰        │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
├────────────────────────────┤
│ ⭐7  ↗️1450  🎁3            │ ← Quick Stats
│ Day  Total   Rewards       │
│ Streak XP                  │
└────────────────────────────┘
```

**Components**:
- Profile header with avatar, name, level, coins
- XP progress bar
- Coins balance card with actions
- 3 daily tasks (Fitness, Focus, Productivity)
- Quick stats grid

**Interactions**:
- Tap "Start" to begin task
- Tap "Done" to complete task
- Tap "Withdraw" to withdraw coins
- Tap "View Rewards" to see rewards

---

### 2. TASKS SCREEN
**File**: `app/screens/tasks.tsx`

```
┌────────────────────────────┐
│ Available Tasks            │
│ ┌────────────────────────┐ │
│ │ 🔍 Search tasks...     │ │ ← Search Bar
│ └────────────────────────┘ │
├────────────────────────────┤
│ [All] [💪Fitness] [📚Focus]│ ← Category Tabs
│ [🎯Productivity]           │
├────────────────────────────┤
│ Task List:                 │
│ ┌──────────────────────┐   │
│ │ 💪 Pushups ×20       │   │ ← Task Card
│ │ Fitness  [Easy]      │   │
│ │ ⚡50 XP  +10💰       │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🏃 Run 5km           │   │
│ │ Fitness [Medium]     │   │
│ │ ⚡75 XP  +15💰       │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 📚 Read 10 minutes   │   │
│ │ Focus    [Easy]      │   │
│ │ ⚡40 XP  +8💰        │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 📋 Project task      │   │
│ │ Productivity [Hard]  │   │
│ │ ⚡100 XP +20💰       │   │
│ │              [Start] │   │
│ └──────────────────────┘   │
└────────────────────────────┘
```

**Components**:
- Search bar for filtering
- Category filter tabs (All, Fitness, Focus, Productivity)
- Task cards with difficulty badges
- Task cards showing title, category, XP, coins
- Start button

**Interactions**:
- Type in search to filter tasks
- Tap category tabs to filter
- Tap "Start" to begin task

---

### 3. LEADERBOARD SCREEN
**File**: `app/screens/leaderboard.tsx`

```
┌────────────────────────────┐
│ Leaderboard                │
│ [🏆Global] [📍City] [👥Fr] │ ← Tab Navigation
├────────────────────────────┤
│ Global Rankings:           │
│ ┌──────────────────────┐   │
│ │ 🥇 Pro Gamer         │   │ ← Top 3 Medals
│ │    Lvl87  43,500 XP  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🥈 Fitness King      │   │
│ │    Lvl76  38,000 XP  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🥉 Study Master      │   │
│ │    Lvl65  32,500 XP  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 4  Alex Kumar   [You]│   │ ← Current User
│ │    Lvl12   1,450 XP │   │    (Highlighted)
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 5  Daily Hustler     │   │
│ │    Lvl45  22,500 XP  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 6  Rise & Grind      │   │
│ │    Lvl38  19,000 XP  │   │
│ └──────────────────────┘   │
├────────────────────────────┤
│ Your ranking updates daily │
│ based on XP earned         │
└────────────────────────────┘
```

**Components**:
- 3 tabs: Global, City, Friends
- Ranking list with:
  - Medal/Rank number
  - Username
  - Level
  - Total XP
  - "You" badge for current user

**Interactions**:
- Tap tabs to switch ranking types
- View your current rank (highlighted)

---

### 4. WALLET SCREEN
**File**: `app/screens/wallet.tsx`

```
┌────────────────────────────┐
│ Wallet                     │
├────────────────────────────┤
│ Total Balance              │
│        750                 │
│       coins                │
│       ₹75.00               │
│ 100 coins = ₹10            │ ← Balance Card
├────────────────────────────┤
│ [Withdraw] [View Rewards]  │ ← Action Buttons
├────────────────────────────┤
│ Withdrawal Form (Expanded):│
│                            │
│ Withdrawal Amount:         │
│ ┌────────────────────────┐ │
│ │ Min. 2000 coins  = ₹200│ │
│ └────────────────────────┘ │
│                            │
│ UPI ID:                    │
│ ┌────────────────────────┐ │
│ │ yourname@upi           │ │
│ └────────────────────────┘ │
│                            │
│ [Submit Request] [Cancel] │
├────────────────────────────┤
│ Transaction History:       │
│ ┌──────────────────────┐   │
│ │ 🎁 Task reward      │   │ ← Transaction
│ │    Today        +10  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ ↗️ Level reward      │   │
│ │    Yesterday    +25  │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🔊 Ad reward        │   │
│ │    2 days ago   +5   │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ ↑ Withdrawal        │   │
│ │    5 days ago  -100  │   │
│ └──────────────────────┘   │
└────────────────────────────┘
```

**Components**:
- Coins balance display with rupee conversion
- Action buttons (Withdraw, View Rewards)
- Expandable withdrawal form with amount and UPI
- Transaction history with type icons

**Interactions**:
- Tap "Withdraw" to show form
- Enter amount and UPI ID
- Tap "Submit Request" to process
- View transaction history

---

### 5. PROFILE SCREEN
**File**: `app/screens/profile.tsx`

```
┌────────────────────────────┐
│ Profile                    │
│ ┌──────────────────────┐   │
│ │ AK  Alex Kumar  [✎]  │   │ ← Profile Header
│ │     Level 12         │   │
│ │ XP Progress          │   │
│ │ ████████░░ 1450/2000 │   │
│ └──────────────────────┘   │
├────────────────────────────┤
│ ⚡1,450    ⭐7      🏆42    │ ← Quick Stats
│ Total XP   Streak   Tasks  │
├────────────────────────────┤
│ Achievements:              │
│ ┌──────────┐ ┌──────────┐ │
│ │ 🎖️       │ │ 🎖️       │ │ ← Achievement
│ │ First    │ │ Week     │ │    Grid
│ │ Step     │ │ Warrior  │ │
│ │ Complete │ │ 7-day    │ │
│ │ 1st task │ │ streak   │ │
│ └──────────┘ └──────────┘ │
│ ┌──────────┐ ┌──────────┐ │
│ │ 🎖️       │ │ 🔒       │ │
│ │ Century  │ │ Level 50 │ │
│ │ 100 XP   │ │ Locked   │ │
│ └──────────┘ └──────────┘ │
│ ┌──────────┐ ┌──────────┐ │
│ │ 🔒       │ │ 🔒       │ │
│ │ Million  │ │ Legend   │ │
│ │ Locked   │ │ Locked   │ │
│ └──────────┘ └──────────┘ │
├────────────────────────────┤
│ [Edit Profile]             │ ← Action Buttons
│ [🚪 Logout]                │
└────────────────────────────┘
```

**Components**:
- User avatar with initials
- Profile header with name and level
- XP progress bar
- Quick stats cards
- Achievement grid (unlocked/locked)
- Edit and Logout buttons

**Interactions**:
- Tap "Edit Profile" to modify profile
- Tap "Logout" to sign out

---

### 6. FRIENDS SCREEN
**File**: `app/screens/friends.tsx`

```
┌────────────────────────────┐
│ Friends                    │
│ ┌────────────────────────┐ │
│ │ 🔍 Search users...     │ │ ← Search
│ │ [➕ Add] [🔍 Search]   │ │
│ └────────────────────────┘ │
├────────────────────────────┤
│ Friend Requests (2):       │
│ ┌──────────────────────┐   │
│ │ John Doe             │   │
│ │ Level 15 • 3,500 XP  │   │
│ │ [✓ Accept] [✕ Decline]  │ ← Request
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Jane Smith           │   │
│ │ Level 18 • 5,200 XP  │   │
│ │ [✓ Accept] [✕ Decline]  │
│ └──────────────────────┘   │
├────────────────────────────┤
│ Friends List (4):          │
│ ┌──────────────────────┐   │
│ │ Mike Johnson         │   │ ← Friend
│ │ Level 22 • 7,800 XP  │   │
│ │              [💬]    │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Sarah Lee            │   │
│ │ Level 19 • 6,500 XP  │   │
│ │              [💬]    │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Tom Wilson           │   │
│ │ Level 14 • 3,200 XP  │   │
│ │              [💬]    │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Emma Brown           │   │
│ │ Level 16 • 4,500 XP  │   │
│ │              [💬]    │   │
│ └──────────────────────┘   │
└────────────────────────────┘
```

**Components**:
- Search bar for finding friends
- Friend requests section with Accept/Decline
- Friends list with levels and XP
- Message button for each friend

**Interactions**:
- Search for friends
- Accept or decline requests
- Message friends

---

### 7. TEAMS SCREEN
**File**: `app/screens/teams.tsx`

```
┌────────────────────────────┐
│ Teams & Clans              │
│ [Create Team] ➕           │ ← Create Button
├────────────────────────────┤
│ Your Teams:                │
│ ┌──────────────────────┐   │
│ │ Fitness Warriors     │   │ ← Team Card
│ │ 👥 12 members        │   │
│ │ 45,000 XP   Rank: #2 │   │
│ │ [Joined]             │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Study Buddies        │   │
│ │ 👥 8 members         │   │
│ │ 28,000 XP   Rank: #5 │   │
│ │ [Joined]             │   │
│ └──────────────────────┘   │
├────────────────────────────┤
│ Discover Teams:            │
│ ┌──────────────────────┐   │
│ │ Tech Titans          │   │ ← Team Card
│ │ 👥 24 members        │   │    (Not Joined)
│ │ 87,000 XP   Rank: #1 │   │
│ │ [Join Team]          │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ Morning Runners      │   │
│ │ 👥 15 members        │   │
│ │ 52,000 XP   Rank: #3 │   │
│ │ [Join Team]          │   │
│ └──────────────────────┘   │
└────────────────────────────┘
```

**Components**:
- Create Team button
- Team list with members, XP, rank
- Joined/Join status
- Team cards with actions

**Interactions**:
- Create new team
- Join existing teams
- View team details

---

### 8. DAILY STREAK SCREEN
**File**: `app/screens/daily-streak.tsx`

```
┌────────────────────────────┐
│ Daily Streak               │
│ ┌──────────────────────┐   │
│ │ 🔥 Current Streak    │   │ ← Streak Card
│ │       7 days         │   │
│ │                      │   │
│ │ Personal Best: 14    │   │
│ └──────────────────────┘   │
├────────────────────────────┤
│ Last 28 Days:              │
│ ┌─┬─┬─┬─┬─┬─┬─┐          │
│ │✓│✓│✓│✓│✓│✓│✓│          │ ← Calendar
│ ├─┼─┼─┼─┼─┼─┼─┤          │
│ │✓│✓│✓│✓│ │ │ │          │
│ ├─┼─┼─┼─┼─┼─┼─┤          │
│ │ │ │ │ │ │ │ │          │
│ ├─┼─┼─┼─┼─┼─┼─┤          │
│ │ │ │ │ │ │ │ │          │
│ └─┴─┴─┴─┴─┴─┴─┘          │
├────────────────────────────┤
│ Milestones:                │
│ ┌──────────────────────┐   │
│ │ 🎉 7-Day Streak      │   │ ← Unlocked
│ │ 100 coins            │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🎉 14-Day Streak     │   │
│ │ Mystery Reward       │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🔒 30-Day Streak     │   │ ← Locked
│ │ Premium Badge        │   │
│ └──────────────────────┘   │
│ ┌──────────────────────┐   │
│ │ 🔒 60-Day Streak     │   │
│ │ 500 coins            │   │
│ └──────────────────────┘   │
└────────────────────────────┘
```

**Components**:
- Current and best streak display
- 28-day calendar grid
- Milestone rewards list
- Locked/unlocked badges

**Interactions**:
- View streak history
- See upcoming milestones

---

### 9. PREMIUM SCREEN
**File**: `app/screens/premium.tsx`

```
┌────────────────────────────┐
│ Life Leveling Premium      │
│ Unlock premium features    │
├────────────────────────────┤
│ ⭐ Monthly Subscription    │
│         ₹149/month         │
│ Billed monthly. Cancel.    │ ← Pricing
│                            │
│ [Subscribe Now]            │
├────────────────────────────┤
│ What You Get:              │
│ ⚡ Ad-Free Experience      │ ← Benefits
│ 🔥 Premium Badge           │
│ ⬆️ +25% Faster XP Gain     │
│ 👥 Priority Support        │
│ 🎁 Exclusive Rewards       │
│ 🎲 Monthly Mystery Reward  │
├────────────────────────────┤
│ Free vs Premium:           │
│ ┌──────────┬───────────┐   │
│ │ Feature  │ Free  Pro │   │
│ ├──────────┼───────────┤   │ ← Comparison
│ │ Ad-Free  │  ✗    ✓  │   │
│ │ XP Mult. │ 1x   1.25x│   │
│ │ Badge    │  ✗    ✓  │   │
│ │ Support  │  ✗    ✓  │   │
│ └──────────┴───────────┘   │
├────────────────────────────┤
│ [Subscribe to Premium]     │
│ [Restore Purchase]         │
│                            │
│ Subscription renews monthly│
│ Manage in account settings │
└────────────────────────────┘
```

**Components**:
- Pricing display (₹149/month)
- Benefits list with icons
- Free vs Premium comparison table
- Subscribe and Restore buttons

**Interactions**:
- View premium features
- Subscribe to premium
- Restore previous purchase

---

## Bottom Navigation

All screens accessible via bottom tab bar:

```
┌─────────────────────────────────────┐
│ 🏠 Home | 📋 Tasks | 🏆 Leaderboard │
│         💳 Wallet | 👤 Profile      │
└─────────────────────────────────────┘
```

- **Home** - Dashboard with profile and daily tasks
- **Tasks** - Browse and search available tasks
- **Leaderboard** - Rankings (Global, City, Friends)
- **Wallet** - Coins management and history
- **Profile** - User stats and achievements

---

## Color Coding

- 🟪 **Indigo (#6366F1)** - Primary actions, active states
- 🟩 **Green (#22C55E)** - Success, completed tasks
- 🟨 **Amber (#F59E0B)** - Warnings, highlights
- ⚫ **Dark Navy (#0F172A)** - Background
- ⚪ **Slate White (#F8FAFC)** - Text

---

## Responsive Design

All screens are optimized for:
- ✅ Mobile phones (320px+)
- ✅ Tablets (landscape)
- ✅ Small screens
- ✅ Notched devices (iPhone X+)

---

For detailed technical information, see `IMPLEMENTATION.md`
For quick start, see `QUICKSTART.md`
