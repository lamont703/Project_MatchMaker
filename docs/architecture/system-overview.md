# VibeMatch - System Architecture Overview

```mermaid
graph TB
    subgraph "Client Layer"
        ReactApp[React Web App]
        Redux[Redux Store]
        Router[React Router]
        Video[Video Components]
    end

    subgraph "API Gateway"
        API[Express API]
        WS[WebSocket Server]
    end

    subgraph "Core Business Services"
        AuthService[Auth Service]
        ProfileService[Profile Service]
        MatchingEngine[Matching Engine]
        MessagingService[Messaging Service]
        CommunityService[Community Service]
    end

    subgraph "AI/ML Layer"
        PersonalityAI[Personality AI]
        ContentAI[Content AI]
        ConversationAI[Conversation AI]
    end

    subgraph "Data Storage"
        CosmosDB[(Azure Cosmos DB)]
        Redis[(Redis Cache)]
        BlobStorage[(Azure Blob Storage)]
    end

    subgraph "External Services"
        GeminiAPI[Google Gemini API]
        AzureAD[Azure AD B2C]
        GHL[GoHighLevel CRM]
    end

    %% Client Layer Connections
    ReactApp --> API
    ReactApp --> WS
    Redux --> ReactApp
    Router --> ReactApp
    Video --> ReactApp

    %% API Gateway to Services
    API --> AuthService
    API --> ProfileService
    API --> MatchingEngine
    API --> MessagingService
    API --> CommunityService

    %% WebSocket Connections
    WS --> MessagingService
    WS --> MatchingEngine

    %% AI Service Connections
    MatchingEngine --> PersonalityAI
    ProfileService --> ContentAI
    MessagingService --> ConversationAI

    %% Data Storage Connections
    AuthService --> CosmosDB
    ProfileService --> CosmosDB
    MatchingEngine --> CosmosDB
    MessagingService --> CosmosDB
    CommunityService --> CosmosDB

    AuthService --> Redis
    MatchingEngine --> Redis
    MessagingService --> Redis

    ProfileService --> BlobStorage

    %% External Service Connections
    AuthService --> AzureAD
    PersonalityAI --> GeminiAPI
    ConversationAI --> GeminiAPI
    ProfileService --> GHL
```

## Architecture Components

### Client Layer

- **React Web App**: Main user interface
- **Redux Store**: State management
- **React Router**: Navigation
- **Video Components**: Video profile handling

### API Gateway

- **Express API**: REST API endpoints
- **WebSocket Server**: Real-time communication

### Core Business Services

- **Auth Service**: User authentication and authorization
- **Profile Service**: User profile management
- **Matching Engine**: Compatibility algorithm and matching logic
- **Messaging Service**: Chat and communication features
- **Community Service**: Community platform features

### AI/ML Layer

- **Personality AI**: Quiz analysis and personality type classification
- **Content AI**: Video and text content moderation
- **Conversation AI**: Icebreaker generation and chat suggestions

### Data Storage

- **Azure Cosmos DB**: Primary database for all user data
- **Redis Cache**: Session data and real-time caching
- **Azure Blob Storage**: Video and media file storage

### External Services

- **Google Gemini API**: AI processing and analysis
- **Azure AD B2C**: Identity management
- **GoHighLevel CRM**: Lead management and user lifecycle
