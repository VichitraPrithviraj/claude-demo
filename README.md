# Claude Demo - Instagram Recipe Meal Planner

An intelligent application that analyzes Instagram recipe bookmarks to automatically generate personalized meal plans using AI-powered content analysis.

## Overview

This app connects to your Instagram bookmarks, extracts recipe information from saved videos, and uses Claude AI to create structured meal plans based on your preferences, dietary requirements, and available ingredients.

## Key Features

### Core Functionality
- **Instagram Integration**: Seamless access to saved recipe videos from bookmarks
- **AI-Powered Recipe Extraction**: Advanced parsing of video content to extract ingredients, cooking methods, and metadata
- **Smart Meal Planning**: Generate weekly/monthly meal plans optimized for variety, nutrition, and preferences
- **Dietary Intelligence**: Automatic filtering and recommendations based on dietary restrictions and allergies
- **Dynamic Shopping Lists**: Auto-generated ingredient lists with quantity optimization and store categorization
- **Nutritional Insights**: Comprehensive nutritional analysis and macro tracking for planned meals

### Advanced Features
- **Cuisine Diversity**: Ensure meal plan variety across different cuisines and cooking styles
- **Seasonal Adaptation**: Recommend recipes based on seasonal ingredient availability
- **Prep Time Optimization**: Balance quick weekday meals with elaborate weekend cooking
- **Leftover Management**: Suggest recipes that utilize leftovers from previous meals
- **Batch Cooking Integration**: Identify meals suitable for meal prep and bulk cooking

## Technical Architecture

### Backend Stack
- **Runtime**: Node.js with TypeScript
- **Framework**: Express.js or Fastify
- **Database**: PostgreSQL with Prisma ORM
- **AI Integration**: Anthropic Claude API for content analysis
- **Video Processing**: FFmpeg for video analysis and frame extraction
- **Authentication**: OAuth 2.0 for Instagram integration

### Frontend Stack
- **Framework**: Next.js 14 with App Router
- **UI Library**: Tailwind CSS with shadcn/ui components
- **State Management**: Zustand or TanStack Query
- **Charts/Analytics**: Recharts or Chart.js

### Infrastructure
- **Hosting**: Vercel (frontend) + Railway/Render (backend)
- **Storage**: AWS S3 for video cache and processed data
- **API**: Meta Graph API for Instagram integration
- **Monitoring**: Sentry for error tracking

## Project Phases

### Phase 1: Foundation (Current)
- [x] Repository setup and documentation
- [ ] Project architecture and tech stack finalization
- [ ] Development environment configuration
- [ ] Database schema design

### Phase 2: Instagram Integration
- [ ] Meta Developer App setup and approval
- [ ] Instagram Basic Display API integration
- [ ] Bookmark retrieval and video URL extraction
- [ ] Rate limiting and error handling implementation

### Phase 3: Content Analysis
- [ ] Video download and caching system
- [ ] Frame extraction and OCR for text overlay detection
- [ ] Claude API integration for recipe parsing
- [ ] Structured data extraction (ingredients, instructions, metadata)

### Phase 4: Meal Planning Engine
- [ ] Recipe categorization and tagging system
- [ ] Meal planning algorithm development
- [ ] Dietary preference and restriction handling
- [ ] Nutritional calculation and balancing

### Phase 5: User Interface
- [ ] Dashboard for meal plan visualization
- [ ] Recipe browsing and filtering interface
- [ ] Shopping list generation and management
- [ ] User preference configuration

### Phase 6: Enhancement & Optimization
- [ ] Performance optimization and caching
- [ ] Advanced filtering and search capabilities
- [ ] Export functionality (PDF, calendar integration)
- [ ] User feedback and rating system

## Installation & Setup

```bash
# Clone the repository
git clone https://github.com/VichitraPrithviraj/claude-demo.git
cd claude-demo

# Install dependencies (when available)
npm install

# Environment setup
cp .env.example .env.local
# Configure Instagram API credentials and Claude API key

# Database setup
npm run db:migrate
npm run db:seed

# Start development server
npm run dev
```

## Configuration

### Required API Keys
- **Instagram Basic Display API**: For accessing user bookmarks
- **Anthropic Claude API**: For recipe content analysis
- **Optional**: Nutritional data API (Spoonacular/Edamam)

### Environment Variables
```bash
INSTAGRAM_APP_ID=your_app_id
INSTAGRAM_APP_SECRET=your_app_secret
CLAUDE_API_KEY=your_claude_api_key
DATABASE_URL=your_database_url
NEXTAUTH_SECRET=your_auth_secret
```

## Usage Example

1. **Connect Instagram**: Authenticate and grant access to bookmarks
2. **Analysis**: App processes saved recipe videos automatically
3. **Preferences**: Set dietary restrictions, cuisine preferences, cooking time limits
4. **Generation**: AI creates personalized weekly meal plan
5. **Shopping**: Export optimized grocery list organized by store sections

## Contributing

This is primarily a personal project for demonstrating AI integration capabilities. However, suggestions and feedback are welcome via issues.

## Roadmap Considerations

- **Mobile App**: React Native version for on-the-go meal planning
- **Social Features**: Share meal plans and recipes with friends
- **Integration**: Calendar sync for meal scheduling
- **Analytics**: Cooking habit insights and improvement suggestions

## License

MIT License (to be confirmed)

---

**Note**: This project requires Instagram API approval and is subject to Meta's platform policies and rate limits.
