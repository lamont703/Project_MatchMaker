# Plenty of Hearts - Technical Design Specifications

## 🎯 Project Overview

**App Name:** Plenty of Hearts  
**Tagline:** "Find your vibe. Not just a match."  
**Target Platform:** Web Application (React with responsive design)  
**MVP Timeline:** 12-16 weeks

## 📐 Technical Architecture

### Frontend Stack

- **Framework:** React
- **State Management:** Redux Toolkit / Zustand
- **Routing:** React Router
- **Video Handling:** HTML5 video with custom controls
- **Animations:** Framer Motion / CSS animations

### Backend Stack

- **API:** Node.js/Express
- **Database:** Microsoft Azure Cosmos DB + Redis (caching)
- **File Storage:** Microsoft Azure Blob Storage
- **Authentication:** Azure Active Directory B2C / Auth0
- **Real-time Notifications:** WebSocket / Server-Sent Events

### AI/ML Components

- **Personality Analysis:** Custom algorithm + Google Gemini API
- **Matching Algorithm:** Collaborative filtering + personality weights
- **Content Moderation:** Azure Content Moderator + custom filters
- **Icebreaker Generation:** Google Gemini API integration

## 🎨 Design System Specifications

### Color Palette (Hex Values)

```css
/* Primary Colors */
--purple-primary: #8b5cf6;
--pink-primary: #ec4899;
--gradient-primary: linear-gradient(135deg, #8b5cf6 0%, #ec4899 100%);

/* Secondary Colors */
--orange-secondary: #f97316;
--green-success: #10b981;
--red-warning: #ef4444;
--blue-info: #6366f1;

/* Neutral Colors */
--white: #ffffff;
--gray-50: #f9fafb;
--gray-100: #f3f4f6;
--gray-400: #9ca3af;
--gray-600: #6b7280;
--gray-900: #1f2937;
```

### Typography Scale

```css
/* Font Families */
--font-primary: "SF Pro Display", "Roboto", sans-serif;
--font-body: "SF Pro Text", "Open Sans", sans-serif;

/* Font Sizes */
--text-xs: 12px;
--text-sm: 14px;
--text-base: 16px;
--text-lg: 18px;
--text-xl: 20px;
--text-2xl: 24px;
--text-3xl: 30px;
--text-4xl: 36px;

/* Font Weights */
--font-light: 300;
--font-normal: 400;
--font-medium: 500;
--font-semibold: 600;
--font-bold: 700;
```

### Spacing System

```css
/* Spacing Scale (px) */
--space-1: 4px;
--space-2: 8px;
--space-3: 12px;
--space-4: 16px;
--space-5: 20px;
--space-6: 24px;
--space-8: 32px;
--space-10: 40px;
--space-12: 48px;
--space-16: 64px;
--space-20: 80px;
```

### Border Radius

```css
--radius-sm: 4px;
--radius-md: 8px;
--radius-lg: 12px;
--radius-xl: 16px;
--radius-2xl: 24px;
--radius-full: 9999px;
```

## 💻 Screen Specifications

### Target Browsers & Breakpoints

- **Desktop:** 1920x1080px (primary), 1366x768px (secondary)
- **Tablet:** 768px - 1024px width
- **Mobile:** 320px - 767px width
- **Large Screens:** 2560px+ (optional enhancement)

### Responsive Design

- **Desktop-first:** Optimize for large screens with graceful mobile degradation
- **Breakpoints:** Use CSS Grid and Flexbox for adaptive layouts
- **Navigation:** Top navigation bar with collapsible mobile menu

## 🎬 Video Specifications

### Upload Requirements

- **Duration:** 15-30 seconds
- **Format:** MP4, MOV
- **Resolution:** 720p minimum, 1080p preferred
- **Aspect Ratio:** 9:16 (vertical) primary, 16:9 secondary
- **File Size:** 50MB maximum
- **Compression:** H.264 codec, AAC audio

### Playback Specifications

- **Auto-play:** Muted by default
- **Controls:** Tap to unmute, double-tap to replay
- **Loading:** Progressive loading with placeholder
- **Bandwidth:** Adaptive quality based on connection

## 🧠 Personality System

### Personality Types (6 Core Types)

1. **The Explorer** 🌍 - Adventurous, curious, spontaneous
2. **The Creative** 🎨 - Artistic, imaginative, expressive
3. **The Connector** 💫 - Social, empathetic, communicative
4. **The Adventurer** 🚀 - Bold, active, thrill-seeking
5. **The Thinker** 🧠 - Analytical, intellectual, introspective
6. **The Nurturer** 🌺 - Caring, supportive, family-oriented

### Quiz Algorithm

- **Questions:** 8 binary choices (A/B format)
- **Scoring:** Weighted responses map to personality dimensions
- **Reliability:** Include validation questions to ensure consistency
- **Retake:** Allow users to retake quiz (cooldown: 30 days)

### Matching Algorithm

```python
# Pseudo-code for matching score calculation
def calculate_match_score(user_a, user_b):
    personality_score = calculate_personality_compatibility(user_a.personality, user_b.personality)
    interest_score = calculate_interest_overlap(user_a.interests, user_b.interests)
    behavior_score = calculate_behavioral_similarity(user_a.actions, user_b.actions)

    # Weighted combination
    final_score = (
        personality_score * 0.5 +
        interest_score * 0.3 +
        behavior_score * 0.2
    )

    return min(max(final_score, 0), 100)  # Clamp to 0-100%
```

## 🔥 Interaction Mechanics

### Desktop Interactions

- **Click & Drag:** Threshold 100px, velocity 200px/s = Pass/Like
- **Button Clicks:** Pass (👎), Like (❤️), Super Like (⭐) buttons
- **Keyboard:** Arrow keys for navigation, Enter for like, Escape for pass
- **Click:** Show profile details/AI insights
- **Double Click:** Replay video

### Mobile Web Interactions

- **Touch Swipe:** Standard swipe gestures on mobile browsers
- **Tap:** Primary interaction method
- **Long Press:** Additional options menu

### Card Stack Implementation

- **Preload:** 3 cards ahead for smooth experience
- **Animation:** CSS transitions with spring easing
- **Feedback:** Visual feedback animations
- **Undo:** Allow undo last action (5 second window)

## 💬 Messaging System

### Real-time Features

- **Protocol:** WebSocket or Socket.io
- **Typing Indicators:** Show when partner is typing
- **Read Receipts:** Optional, user-controlled
- **Message Status:** Sent, delivered, read

### AI Conversation Features

- **Icebreakers:** Generated based on profile analysis
- **Conversation Starters:** Context-aware suggestions
- **Tone Analysis:** Detect conversation health/engagement
- **Safety:** Auto-detect inappropriate content

## 🔒 Privacy & Safety

### Content Moderation

- **Video Screening:** AI-powered inappropriate content detection
- **Profile Text:** Automated filtering + human review
- **Reporting System:** Easy reporting with categorized reasons
- **Blocking:** Instant block with no notification to blocked user

### Data Protection

- **Encryption:** End-to-end for messages, AES-256 for stored data
- **GDPR Compliance:** Full data export/deletion capabilities
- **Location Privacy:** Show distance ranges, not exact locations
- **Photo Protection:** Watermarking, screenshot detection

## 📊 Analytics & Metrics

### Key Performance Indicators

- **User Engagement:** Daily/weekly active users
- **Matching Success:** Matches per user, message response rates
- **Retention:** D1, D7, D30 retention rates
- **Conversion:** Free to premium upgrade rates

### A/B Testing Framework

- **Personality Quiz:** Question variations, UI changes
- **Swipe Interface:** Card designs, button placements
- **Matching Algorithm:** Different scoring weights
- **Onboarding Flow:** Step sequences, copy variations

## 💎 Premium Features

### Subscription Tiers

- **Basic (Free):** 5 likes/day, basic matching
- **Premium ($9.99/month):** Unlimited likes, super likes, see who liked you
- **Premium+ ($19.99/month):** Advanced filters, priority matching, read receipts

### Implementation

- **Subscription Management:** Stripe/PayPal integration for web payments
- **Feature Gates:** Graceful degradation for free users
- **Upgrade Prompts:** Strategic placement, not intrusive

## 🚀 Development Phases

### Phase 1: Core MVP (8 weeks)

- [ ] User authentication & onboarding
- [ ] Personality quiz implementation
- [ ] Basic profile creation (photos only)
- [ ] Simple swipe interface
- [ ] Basic matching algorithm
- [ ] Simple messaging system

### Phase 2: Video & Enhancement (4 weeks)

- [ ] Video upload & playback
- [ ] AI personality insights
- [ ] Enhanced matching algorithm
- [ ] Icebreaker suggestions
- [ ] Push notifications

### Phase 3: Polish & Premium (4 weeks)

- [ ] Premium features implementation
- [ ] Advanced animations & micro-interactions
- [ ] Comprehensive analytics
- [ ] Performance optimization
- [ ] Production deployment & launch

## 🛠 Technical Requirements

### Performance Targets

- **Initial Load:** < 3 seconds to main screen
- **Interaction Response:** < 100ms click to animation
- **Video Load:** < 2 seconds on broadband connection
- **Message Delivery:** < 500ms end-to-end

### Browser Requirements

- **Chrome:** 90+ (supports 95% of users)
- **Firefox:** 88+ (supports 90% of users)
- **Safari:** 14+ (supports 95% of Mac users)
- **Edge:** 90+ (supports modern Windows users)
- **Storage:** 50MB cached data, 200MB including video cache
- **RAM:** 4GB minimum for smooth operation

### Third-Party Integrations

- **Authentication:** Azure Active Directory B2C / Auth0
- **Analytics:** Google Analytics + Mixpanel
- **Error Monitoring:** Sentry / Azure Application Insights
- **Real-time Notifications:** WebSocket / Server-Sent Events
- **Video Processing:** Azure Media Services / Cloudinary
- **AI Services:** Google Gemini API for conversation features

This specification provides a comprehensive foundation for developing the Plenty of Hearts MVP while maintaining scalability for future enhancements.
