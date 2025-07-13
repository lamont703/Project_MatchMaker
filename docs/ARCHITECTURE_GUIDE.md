# VibeMatch Architecture Guide

## 🎯 Quick Start for Developers

This guide helps you understand and use the VibeMatch architecture diagrams for development planning and implementation.

## 📋 Available Diagrams

### 1. **System Overview** (`docs/architecture/system-overview-basic.puml`)
- **Purpose**: High-level system architecture
- **Use When**: Planning overall system design, understanding component relationships
- **Shows**: All services, data stores, external APIs, and their connections

### 2. **Registration Flow** (`docs/architecture/registration-flow.puml`)
- **Purpose**: User onboarding process
- **Use When**: Implementing authentication, personality quiz, GoHighLevel integration
- **Shows**: Step-by-step user registration and personality analysis

### 3. **Matching Algorithm** (`docs/architecture/matching-algorithm.puml`)
- **Purpose**: Core matching logic
- **Use When**: Building the swipe interface, compatibility scoring, AI integration
- **Shows**: Swipe processing, cache strategy, AI analysis, match detection

### 4. **Messaging System** (`docs/architecture/messaging-system.puml`)
- **Purpose**: Real-time chat features
- **Use When**: Implementing WebSocket connections, chat UI, typing indicators
- **Shows**: Message flow, AI enhancements, read receipts, real-time delivery

### 5. **Database Schema** (`docs/architecture/database-schema.puml`)
- **Purpose**: Data model and relationships
- **Use When**: Setting up database, planning data migrations, API design
- **Shows**: Tables, relationships, foreign keys, data structure

### 6. **Community Platform** (`docs/architecture/community-components.puml`)
- **Purpose**: Community features architecture
- **Use When**: Building community features, posts, events, social discovery
- **Shows**: Frontend components, backend services, data flow

## 🛠 How to Use These Diagrams

### Opening Diagrams
1. **Open any `.puml` file** in Cursor
2. **Press `Cmd+Shift+P`** (or `Ctrl+Shift+P` on Windows)
3. **Type**: `PlantUML: Preview Current Diagram`
4. **Press Enter** to view the diagram

### During Development
- **Reference before coding** - understand the data flow first
- **Check component interactions** - see how services connect
- **Validate API design** - ensure consistency with diagrams
- **Plan testing scenarios** - based on sequence flows

### During Code Reviews
- **Compare implementation** with diagram expectations
- **Identify missing error handling** in complex flows
- **Verify security considerations** in authentication flows
- **Check performance implications** in matching/caching flows

## 📊 Development Phases

### Phase 1: Foundation (Weeks 1-4)
**Focus Diagrams**: `system-overview-basic.puml`, `registration-flow.puml`, `database-schema.puml`
- Set up basic architecture
- Implement user registration
- Design database schema
- Integrate Azure AD B2C

### Phase 2: Core Features (Weeks 5-8)
**Focus Diagrams**: `matching-algorithm.puml`, `database-schema.puml`
- Build personality quiz
- Implement matching engine
- Add swipe interface
- Integrate Gemini AI

### Phase 3: Communication (Weeks 9-12)
**Focus Diagrams**: `messaging-system.puml`, `system-overview-basic.puml`
- Build real-time messaging
- Add WebSocket infrastructure
- Implement chat features
- Add AI conversation enhancements

### Phase 4: Community & Polish (Weeks 13-16)
**Focus Diagrams**: `community-components.puml`, `system-overview-basic.puml`
- Build community platform
- Add social discovery features
- Performance optimization
- Production deployment

## 🎯 Key Technical Decisions

### Architecture Patterns
- **Microservices**: Each service handles specific domain logic
- **Event-Driven**: WebSocket for real-time features
- **Caching Strategy**: Redis for performance-critical data
- **AI Integration**: External API calls to Gemini

### Data Flow
1. **User Input** → React Components
2. **API Calls** → Express.js Routes  
3. **Business Logic** → Service Layer
4. **Data Persistence** → Cosmos DB
5. **Real-time Updates** → WebSocket Server

### Integration Points
- **Azure AD B2C**: User authentication
- **Google Gemini API**: AI personality analysis
- **GoHighLevel CRM**: Lead management
- **Azure Blob Storage**: Video file storage

## 🚨 Common Implementation Patterns

### Error Handling
```javascript
// Follow this pattern in all services
try {
  const result = await serviceMethod();
  return { success: true, data: result };
} catch (error) {
  logger.error('Service error:', error);
  return { success: false, error: error.message };
}
```

### API Response Format
```javascript
// Consistent API responses
{
  success: boolean,
  data?: any,
  error?: string,
  metadata?: {
    timestamp: string,
    requestId: string
  }
}
```

### WebSocket Message Format
```javascript
// Consistent WebSocket messages
{
  type: 'message' | 'typing' | 'match' | 'notification',
  payload: any,
  userId: string,
  timestamp: string
}
```

## 📝 Questions to Ask During Implementation

### Before Starting a Feature
1. Which diagram shows this feature's architecture?
2. What services does this feature interact with?
3. What data does this feature need to store/retrieve?
4. Are there any external API dependencies?

### During Implementation
1. Does my code match the sequence shown in the diagram?
2. Am I handling all the error cases shown?
3. Are the data transformations consistent with the schema?
4. Do I need to update any diagrams based on implementation details?

### Before Code Review
1. Have I tested all the flows shown in the relevant diagram?
2. Are there any performance implications I haven't considered?
3. Does my implementation handle the caching strategy correctly?
4. Are security considerations properly implemented?

## 🔄 Updating Diagrams

When you discover implementation details that differ from the diagrams:

1. **Discuss with senior developer** - understand if it's a valid change
2. **Update the diagram** - keep documentation current
3. **Document the reasoning** - add comments explaining changes
4. **Commit with descriptive message** - track architectural evolution

## 🎉 Success Metrics

By using these diagrams effectively, you should achieve:

- **Faster onboarding** - understand system quickly
- **Fewer integration bugs** - clear component boundaries
- **Better code reviews** - shared understanding of architecture
- **Easier debugging** - trace issues through data flows
- **Consistent implementation** - follow established patterns

---

**Remember**: These diagrams are living documents. Update them as the system evolves! 