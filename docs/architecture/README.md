# VibeMatch Architecture Documentation

This directory contains the technical architecture diagrams for the VibeMatch dating application. All diagrams are created using PlantUML and use basic syntax that works without Graphviz dependencies.

## 📋 Working Diagram Overview

### 1. **system-overview-basic.puml** ✅
- **Purpose**: High-level system architecture showing all major components
- **Audience**: Technical leads, stakeholders, development team
- **Key Elements**: Frontend, backend services, AI components, databases, external APIs
- **Status**: Working - shows clean participant layout

### 2. **registration-flow.puml** ✅
- **Purpose**: User registration and personality quiz sequence flow
- **Audience**: Backend developers, QA engineers
- **Key Elements**: User registration, Azure AD integration, personality analysis, GoHighLevel sync
- **Status**: Working - complete sequence diagram

### 3. **matching-algorithm.puml** ✅
- **Purpose**: Detailed matching algorithm implementation flow
- **Audience**: Backend developers, AI engineers
- **Key Elements**: Swipe processing, compatibility scoring, AI insights, caching strategy
- **Status**: Working - simplified from complex alt statements

### 4. **messaging-system.puml** ✅
- **Purpose**: Real-time messaging architecture and flow
- **Audience**: Backend developers, frontend developers
- **Key Elements**: WebSocket connections, message delivery, typing indicators, read receipts
- **Status**: Working - clean sequence flow

### 5. **database-schema.puml** ✅
- **Purpose**: Database entity relationships and structure
- **Audience**: Database developers, backend engineers
- **Key Elements**: User profiles, matches, messages, communities, personality data
- **Status**: Working - participant format with detailed notes

### 6. **community-components.puml** ✅
- **Purpose**: Community platform component structure
- **Audience**: Full-stack developers, product managers
- **Key Elements**: Community management, posts, events, social discovery
- **Status**: Working - participant format showing component relationships

### 7. **system-overview.md** (Backup)
- **Purpose**: Mermaid version of system architecture
- **Format**: Markdown with Mermaid diagram
- **Status**: Working - renders natively in Cursor

## 🛠 How to Use These Diagrams

### Prerequisites
1. ✅ PlantUML extension installed in VS Code/Cursor
2. ✅ Java available (no Graphviz required!)
3. ✅ All diagrams use basic syntax

### Viewing Diagrams
1. Open any `.puml` file in VS Code/Cursor
2. Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac)
3. Type "PlantUML: Preview Current Diagram"
4. The diagram will render in a preview pane

### Exporting Diagrams
1. Right-click on the diagram preview
2. Select "Export Current Diagram"
3. Choose format (PNG, SVG, PDF)
4. Save for presentations or documentation

## 🖼️ Exporting Diagrams to Images

### Method 1: VS Code/Cursor PlantUML Extension (Recommended)

1. **Open any `.puml` file** in Cursor
2. **Preview the diagram**: Press `Cmd+Shift+P` → "PlantUML: Preview Current Diagram"
3. **Export options:**
   - **Right-click** on the diagram preview
   - **Select "Export Current Diagram"**
   - **Choose format**: PNG, SVG, PDF, or PostScript
   - **Save** to your desired location

### Method 2: Command Line Export

If you have PlantUML installed locally, you can batch export all diagrams:

```bash
# Export all diagrams to PNG
java -jar plantuml.jar -tpng docs/architecture/*.puml

# Export specific diagram to SVG
java -jar plantuml.jar -tsvg docs/architecture/system-overview-basic.puml

# Export to specific directory
java -jar plantuml.jar -o exports/ docs/architecture/*.puml
```

### Method 3: Online PlantUML Server

1. **Copy diagram code** from any `.puml` file
2. **Go to**: http://www.plantuml.com/plantuml/
3. **Paste your code** in the text area
4. **Download** in PNG, SVG, or other formats

### Method 4: VSCode Extension Batch Export

1. **Open Command Palette**: `Cmd+Shift+P`
2. **Type**: "PlantUML: Export Workspace Diagrams"
3. **Choose format and location**
4. **All diagrams** will be exported automatically

## 📁 Recommended Export Structure

For presentations and documentation, we recommend creating an `exports/` directory:

```
docs/
├── architecture/
│   ├── *.puml (source files)
│   └── exports/
│       ├── png/
│       │   ├── system-overview-basic.png
│       │   ├── registration-flow.png
│       │   └── ...
│       ├── svg/
│       │   ├── system-overview-basic.svg
│       │   └── ...
│       └── pdf/
           ├── system-overview-basic.pdf
           └── ...
```

## 🎯 Export Format Recommendations

- **PNG**: Best for presentations, documentation, and web use
- **SVG**: Best for scalable graphics and print materials
- **PDF**: Best for formal documentation and client deliverables
- **PostScript**: Best for high-quality printing

## 🚀 Quick Export Setup

Want to quickly export all diagrams? Run this command:

```bash
# Create export directory structure
mkdir -p docs/architecture/exports/{png,svg,pdf}

# Export all diagrams (if you have PlantUML installed)
java -jar plantuml.jar -tpng -o exports/png/ docs/architecture/*.puml
java -jar plantuml.jar -tsvg -o exports/svg/ docs/architecture/*.puml
java -jar plantuml.jar -tpdf -o exports/pdf/ docs/architecture/*.puml
```

### Editing Guidelines
- **Consistency**: All diagrams use participant syntax for compatibility
- **Clarity**: Notes provide detailed component information
- **Simplicity**: Avoid complex syntax that requires Graphviz
- **Documentation**: Update this README when adding new diagrams

## 🎯 Technical Analysis Workflow

### For Senior Developers
1. **Review** existing diagrams before architectural decisions
2. **Update** diagrams when implementing new features
3. **Validate** designs with the team using these visual references
4. **Document** architectural decisions with diagram updates

### For Junior Developers
1. **Study** diagrams to understand system interactions
2. **Reference** during implementation to stay aligned with architecture
3. **Ask questions** about unclear relationships shown in diagrams
4. **Suggest updates** when discovering implementation details

## 📊 Diagram Maintenance

### Regular Updates
- **After major feature implementations**
- **When external integrations change**
- **During architectural refactoring**
- **Before major releases**

### Review Process
1. Create feature branch for architecture changes
2. Update relevant diagrams
3. Export updated images
4. Submit pull request with diagram changes
5. Architecture review before merging

## 🔗 Integration Points

### Key External Services
- **Azure AD B2C**: User authentication and management
- **Google Gemini API**: AI personality analysis and insights
- **GoHighLevel CRM**: Lead management and user lifecycle
- **Azure Cosmos DB**: Primary database storage
- **Azure Blob Storage**: Video and media file storage

### Development Phases
1. **Phase 1**: Authentication, profiles, basic matching (Weeks 1-4)
2. **Phase 2**: Video processing, AI integration, messaging (Weeks 5-8)
3. **Phase 3**: Community platform, advanced features (Weeks 9-12)
4. **Phase 4**: Premium features, analytics, optimization (Weeks 13-16)

## 📈 Performance Considerations

### Caching Strategy
- **Redis**: Session data, match cache, real-time data
- **CDN**: Static assets, video content delivery
- **Database**: Indexed queries, optimized schema

### Scalability Points
- **WebSocket Server**: Horizontal scaling for messaging
- **Matching Engine**: Distributed processing for large user base
- **AI Services**: Rate limiting and request queuing
- **Database**: Sharding strategy for user growth

## 🚀 Getting Started

1. **Clone** the repository
2. **Install** PlantUML extension in Cursor
3. **Open** any `.puml` file
4. **Preview** the diagram using `Cmd+Shift+P`
5. **Start** implementing based on the architecture

## ✅ All Diagrams Tested and Working

Every diagram in this directory has been tested and confirmed working with the current PlantUML setup. No external dependencies (like Graphviz) are required.

For questions about the architecture or diagrams, please reach out to the senior development team or create an issue in the project repository.
