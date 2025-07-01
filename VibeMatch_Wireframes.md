# VibeMatch - Dating Web App MVP Wireframes

## Project Overview

**App Name:** VibeMatch  
**Tagline:** "Find your vibe. Not just a match."  
**Platform:** Web application (Desktop with mobile responsiveness)  
**Design Philosophy:** Fun, clean, emotionally intelligent interface that blends dating with self-discovery

---

## 🎯 Design System

### Color Palette

- **Primary:** Gradient purple-to-pink (#8B5CF6 → #EC4899)
- **Secondary:** Warm orange (#F97316)
- **Background:** Clean white (#FFFFFF) with soft gray sections (#F9FAFB)
- **Text:** Dark gray (#1F2937) for primary, medium gray (#6B7280) for secondary
- **Success:** Green (#10B981)
- **Warning:** Red (#EF4444)

### Typography

- **Headers:** Bold, modern sans-serif (SF Pro Display / Roboto)
- **Body:** Clean, readable sans-serif (SF Pro Text / Open Sans)
- **Size Scale:** 32px (H1), 24px (H2), 18px (H3), 16px (body), 14px (small)

### Iconography

- **Style:** Rounded, friendly icons
- **Size:** 24px standard, 32px for primary actions
- **Colors:** Match brand palette

---

## 💻 Screen Wireframes

### 1. Welcome / Onboarding Screen

```
┌─────────────────────────────────────┐
│               STATUS BAR            │
├─────────────────────────────────────┤
│                                     │
│              [LOGO]                 │
│            VibeMatch                │
│                                     │
│         Find your vibe.             │
│       Not just a match.             │
│                                     │
│                                     │
│         🎭 Personality-Based        │
│         📹 Video Profiles           │
│         🔥 Smart Matching           │
│                                     │
│                                     │
│     ┌─────────────────────────┐     │
│     │      Get Started        │     │
│     └─────────────────────────┘     │
│                                     │
│        Already have an account?     │
│              Sign In                │
│                                     │
└─────────────────────────────────────┘
```

**Key Elements:**

- Hero logo with app name
- Value proposition tagline
- 3 key feature highlights with icons
- Primary CTA button (gradient background)
- Secondary sign-in link
- Clean, welcoming design

---

### 2. Personality Quiz Flow (VibeMatch)

#### Quiz Introduction Screen

```
┌─────────────────────────────────────┐
│  ◄    VibeMatch Quiz           ✕    │
├─────────────────────────────────────┤
│                                     │
│              🧠                     │
│                                     │
│         Discover Your               │
│         Personality Vibe            │
│                                     │
│     Answer 8 quick questions to     │
│     unlock your unique personality  │
│     type and find better matches    │
│                                     │
│         ⏱️ Takes 2 minutes          │
│                                     │
│     ┌─────────────────────────┐     │
│     │     Start Quiz          │     │
│     └─────────────────────────┘     │
│                                     │
└─────────────────────────────────────┘
```

#### Quiz Question Screen

```
┌─────────────────────────────────────┐
│  ◄         Question 3/8        ✕    │
├─────────────────────────────────────┤
│ ████████████░░░░░░░░░░░░░░░░░░░░░░░ │ (Progress bar)
│                                     │
│              🎨                     │
│                                     │
│     What energizes you most         │
│        on a weekend?                │
│                                     │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │  🏠  Cozy movie night at home   │ │
│  │                                 │ │
│  └─────────────────────────────────┘ │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │  🎉  Big party with friends     │ │
│  │                                 │ │
│  └─────────────────────────────────┘ │
│                                     │
└─────────────────────────────────────┘
```

**Quiz Features:**

- Progress indicator
- Card-based questions with icons
- Large, clickable answer buttons
- Smooth transitions between questions
- Visual metaphors for personality traits

---

### 3. Profile Setup Screen

```
┌─────────────────────────────────────┐
│  ◄      Create Profile         ✕    │
├─────────────────────────────────────┤
│                                     │
│           📹 Your Video             │
│     ┌─────────────────────────┐     │
│     │                         │     │
│     │       [UPLOAD]          │     │
│     │     Tap to record       │     │
│     │      15-30 seconds      │     │
│     │                         │     │
│     └─────────────────────────┘     │
│                                     │
│  Name: [________________]           │
│                                     │
│  Age:  [__]  📍 Location: [_____]   │
│                                     │
│  ✏️ Tell us about yourself:         │
│  ┌─────────────────────────────────┐ │
│  │                                 │ │
│  │                                 │ │
│  └─────────────────────────────────┘ │
│                                     │
│  🏷️ Interests (tap to add):         │
│  [Music] [Travel] [Fitness] [+]     │
│                                     │
│     ┌─────────────────────────┐     │
│     │     Continue            │     │
│     └─────────────────────────┘     │
└─────────────────────────────────────┘
```

**Key Elements:**

- Prominent video upload area
- Essential profile fields
- Interest tags with easy selection
- Bio text area
- Clear progress indication

---

### 4. MatchCard Swipe Deck

```
┌─────────────────────────────────────┐
│     🔥        VibeMatch        ⚙️    │
├─────────────────────────────────────┤
│                                     │
│  ┌─────────────────────────────────┐ │
│  │                                 │ │
│  │        [VIDEO PREVIEW]          │ │
│  │         Auto-playing            │ │
│  │                                 │ │
│  │  🔊                          📱 │ │
│  │                                 │ │
│  │  Taylor, 24  📍 2 miles away   │ │
│  │                                 │ │
│  │     🌟 The Explorer 🌍          │ │
│  │     87% Match • 3 mutual        │ │
│  │                                 │ │
│  │  "Love hiking and discovering   │ │
│  │   hidden coffee shops! 🏔️☕"    │ │
│  │                                 │ │
│  │  📸 Music 🎵 Adventure ✈️       │ │
│  └─────────────────────────────────┘ │
│                                     │
│     💡 See Why We Think You Match   │
│                                     │
│    👎            ❤️            ⭐   │
│   PASS         LIKE         SUPER   │
│                                     │
└─────────────────────────────────────┘
```

**Interactive Elements:**

- Swipeable cards (left = pass, right = like)
- Video controls (mute/unmute, replay)
- "Why We Match" AI insight popup
- Super like option for premium engagement
- Personality badge with emoji

#### AI Insight Popup

```
┌─────────────────────────────────────┐
│              ✕ Close                │
├─────────────────────────────────────┤
│         Why You Match! 🎯           │
│                                     │
│  You're both Explorers who love:    │
│                                     │
│  ✓ Outdoor adventures               │
│  ✓ Trying new experiences           │
│  ✓ Spontaneous weekend trips        │
│                                     │
│  🧠 Personality Compatibility:      │
│  • Both value authenticity         │
│  • Similar energy levels           │
│  • Complementary communication     │
│                                     │
│     Confidence Score: 87%           │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │         Like Taylor!            │ │
│  └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

---

### 5. Match Result Screen

```
┌─────────────────────────────────────┐
│                 ✕                   │
├─────────────────────────────────────┤
│                                     │
│              🎉                     │
│                                     │
│           It's a Match!             │
│                                     │
│      You and Taylor are             │
│        87% compatible               │
│                                     │
│    ┌───────┐        ┌───────┐       │
│    │ [YOU] │   💕   │[TAYLOR]│      │
│    │       │        │       │       │
│    └───────┘        └───────┘       │
│                                     │
│    🌟 Explorer + 🎨 Creative        │
│                                     │
│   💡 Icebreaker suggestion:         │
│   "I saw you love hiking! What's    │
│    your favorite trail discovery?"  │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │      Send Message               │ │
│  └─────────────────────────────────┘ │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │      Keep Swiping               │ │
│  └─────────────────────────────────┘ │
│                                     │
└─────────────────────────────────────┘
```

**Key Elements:**

- Celebratory animation/confetti
- Profile photos of both users
- Compatibility percentage
- Personality type pairing
- AI-generated icebreaker
- Clear next actions

---

### 6. Inbox / Messaging Preview

```
┌─────────────────────────────────────┐
│  ◄       Messages              👤   │
├─────────────────────────────────────┤
│                                     │
│  ┌─────────────────────────────────┐ │
│  │ 📸 Taylor    🟢    87% match    │ │
│  │ "Thanks for the trail rec! 🏔️"  │ │
│  │                         2m ago  │ │
│  └─────────────────────────────────┘ │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │ 📸 Alex      🟡    92% match    │ │
│  │ "Coffee shop hunt this weekend?" │ │
│  │                         1h ago  │ │
│  └─────────────────────────────────┘ │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │ 📸 Jordan    ⚪    79% match    │ │
│  │ AI: "Ask about their art proj..." │ │
│  │                         1d ago  │ │
│  └─────────────────────────────────┘ │
│                                     │
│            💡 AI Tip:               │
│    "Taylor mentioned rock climbing  │
│     - perfect conversation starter!" │
│                                     │
└─────────────────────────────────────┘
```

#### Individual Chat Screen

```
┌─────────────────────────────────────┐
│  ◄  📸 Taylor (87% match)      📹   │
├─────────────────────────────────────┤
│                                     │
│         Today, 2:15 PM              │
│                                     │
│  ┌─────────────────────────┐        │
│  │ Hey! Love your hiking   │        │
│  │ video. Which trail? 🏔️  │        │
│  └─────────────────────────┘        │
│                                     │
│         ┌─────────────────────────┐  │
│         │ Thanks! It's Bear Creek │  │
│         │ Trail. Hidden gem! 💎   │  │
│         └─────────────────────────┘  │
│                                     │
│  ┌─────────────────────────┐        │
│  │ No way! I was just      │        │
│  │ there last weekend! 🤯   │        │
│  └─────────────────────────┘        │
│                                     │
│   💡 AI suggests: "Ask about their  │
│      favorite post-hike snack spot" │
│                                     │
│  ┌─────────────────────────────────┐ │
│  │ Type a message...         🎁 📷  │ │
│  └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

---

### 7. Settings / Profile Management

```
┌─────────────────────────────────────┐
│  ◄         Settings                 │
├─────────────────────────────────────┤
│                                     │
│         👤 Your Profile             │
│  ┌─────────────────────────────────┐ │
│  │  📹 Edit Video                  │ │
│  │  ✏️  Edit Bio & Photos          │ │
│  │  🏷️  Update Interests           │ │
│  │  📍 Change Location             │ │
│  └─────────────────────────────────┘ │
│                                     │
│      🧠 Personality & Matching      │
│  ┌─────────────────────────────────┐ │
│  │  🔄 Retake Personality Quiz     │ │
│  │  ⚙️  Matching Preferences       │ │
│  │  📊 View Your Vibe Report       │ │
│  └─────────────────────────────────┘ │
│                                     │
│         💎 Premium Features         │
│  ┌─────────────────────────────────┐ │
│  │  ⭐ Unlimited Super Likes       │ │
│  │  👁️  See Who Likes You          │ │
│  │  🔍 Advanced Filters            │ │
│  │  📈 Detailed Match Insights     │ │
│  │                                 │ │
│  │     Upgrade for $9.99/month     │ │
│  └─────────────────────────────────┘ │
│                                     │
│         ⚙️ App Settings             │
│  • Notifications                    │
│  • Privacy & Safety                │
│  • Help & Support                  │
│                                     │
└─────────────────────────────────────┘
```

---

## 🔄 User Flow Overview

1. **Onboarding:** Welcome → Quiz → Profile Setup
2. **Core Loop:** Swipe Deck → Match → Messaging
3. **Profile Management:** Settings → Edit Profile → Quiz Retake
4. **Premium Upgrade:** Throughout app with gentle prompts

## 📐 Technical Specifications

### Screen Dimensions

- **Primary Target:** Desktop 1920x1080px
- **Tablet Target:** 768px - 1024px width
- **Mobile Target:** 320px - 767px width
- **Responsive:** Adapts to various screen sizes with CSS Grid/Flexbox

### Interaction Patterns

- **Drag & Click Interactions:** Primary navigation for card deck (with button alternatives)
- **Click Interactions:** Buttons, options, navigation (with hover states)
- **Video Playback:** Auto-play with manual controls
- **Smooth Animations:** Page transitions, match celebrations

### Performance Considerations

- **Video Optimization:** Compressed, web-optimized formats
- **Lazy Loading:** Cards and images load as needed
- **Offline Support:** Basic functionality with service worker caching
- **Fast Loading:** Critical screens load under 2 seconds
- **Responsive Design:** Seamless experience across all device sizes

---

## 🎨 Visual Design Notes

### Personality Type Badges

- **The Explorer** 🌍 (Purple gradient)
- **The Creative** 🎨 (Orange gradient)
- **The Connector** 💫 (Pink gradient)
- **The Adventurer** 🚀 (Blue gradient)
- **The Thinker** 🧠 (Green gradient)
- **The Nurturer** 🌺 (Coral gradient)

### Animation Guidelines

- **Subtle and purposeful:** Enhance UX without distraction
- **Spring animations:** For natural, organic feel
- **Celebration moments:** Confetti, hearts for matches
- **Loading states:** Smooth skeleton screens

### Accessibility

- **Color contrast:** WCAG AA compliant
- **Text size:** Scalable fonts
- **Voice over:** Screen reader friendly
- **Motor accessibility:** Large touch targets (44px minimum)

---

## 💡 AI Enhancement Opportunities

1. **Smart Matching:** Continuous learning from user behavior
2. **Icebreaker Generation:** Contextual conversation starters
3. **Profile Optimization:** Suggestions for better matches
4. **Timing Intelligence:** Optimal notification timing
5. **Safety Features:** AI-powered content moderation

This wireframe foundation supports a scalable, engaging dating web application that prioritizes meaningful connections through personality-based matching while maintaining a fun, game-like experience. The design is optimized for desktop users with full responsive support for tablets and mobile browsers.
