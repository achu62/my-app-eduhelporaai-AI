# EduraAI - Educational Assistant

## Overview

EduraAI is a mobile-first educational chatbot web application built with vanilla HTML, CSS, and JavaScript. The application provides AI-powered educational assistance with modern dark UI, image/file upload support, and strict educational content filtering. It features conversation persistence, stop functionality during generation, and a clean mobile-optimized interface.

## System Architecture

### Frontend Architecture
- **Framework**: Vanilla HTML, CSS, and JavaScript (no React)
- **Build Tool**: Vite for development server and static file serving
- **Styling**: Custom CSS with dark theme and mobile-first responsive design
- **State Management**: Native JavaScript state management
- **UI Components**: Custom CSS components with Font Awesome icons

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **API Design**: RESTful endpoints with file upload support
- **Middleware**: Multer for multipart file handling
- **Session Management**: Express sessions with PostgreSQL store

### Database Architecture
- **Primary Database**: PostgreSQL
- **ORM**: Drizzle ORM with type-safe schema definitions
- **Migration System**: Drizzle Kit for schema management
- **Connection**: Neon serverless PostgreSQL for production

## Key Components

### Chat System
- Real-time conversation interface with typing indicators
- Message history persistence with session-based storage
- File attachment support for educational materials
- AI response streaming with abort capability
- Text-to-speech functionality for AI responses
- Custom educational keyboard with mathematical and scientific symbols

### File Processing
- **Supported Formats**: Images (JPEG, PNG, GIF, WebP), PDFs, Word documents, plain text
- **Size Limits**: 10MB maximum file size
- **Image Analysis**: OpenAI Vision API for image content analysis
- **Storage**: Local file system with automatic cleanup

### AI Integration
- **Provider**: Google Gemma-2-9B model via OpenRouter.ai for text generation and image analysis
- **Content Filtering**: Educational content validation to ensure appropriate responses
- **Context Management**: Conversation history tracking for coherent interactions
- **Safety**: Built-in content moderation and educational focus enforcement

### User Interface
- **Design System**: Custom Tailwind configuration with CSS variables
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **Accessibility**: ARIA labels and keyboard navigation support
- **Dark/Light Mode**: CSS variable-based theming system
- **Educational Keyboard**: Custom on-screen keyboard with Greek letters, mathematical operators, superscripts, subscripts, and scientific symbols
- **Voice Output**: Text-to-speech functionality for AI responses with speaker controls

## Data Flow

1. **User Input**: Messages and files submitted through the chat interface
2. **Content Validation**: Educational content filtering before AI processing
3. **File Processing**: Images converted to base64 for AI vision analysis
4. **AI Processing**: OpenAI API generates contextual educational responses
5. **Response Delivery**: Streamed responses with real-time updates
6. **Persistence**: Conversation history stored in PostgreSQL
7. **Cleanup**: Temporary files automatically removed after processing

## External Dependencies

### Core Services
- **OpenAI API**: GPT-4o model for text generation and image analysis
- **Neon Database**: Serverless PostgreSQL hosting
- **Replit Infrastructure**: Development and deployment platform

### Development Tools
- **TypeScript**: Type safety across frontend and backend
- **ESBuild**: Fast JavaScript bundling for production
- **PostCSS**: CSS processing with Tailwind and Autoprefixer
- **Drizzle Kit**: Database schema management and migrations

### UI Libraries
- **Radix UI**: Accessible component primitives
- **Lucide React**: Icon library
- **TanStack React Query**: Server state management
- **React Hook Form**: Form handling with validation

## Deployment Strategy

### Development Environment
- **Runtime**: Node.js 20 with hot reload via tsx
- **Database**: PostgreSQL 16 in development mode
- **Build Process**: Vite dev server with HMR
- **Port Configuration**: Frontend on 5000, backend integrated

### Production Deployment
- **Platform**: Replit Autoscale deployment
- **Build Process**: 
  1. Vite builds optimized frontend bundle
  2. ESBuild creates server bundle with external packages
  3. Static assets served from dist/public directory
- **Environment**: Production Node.js with PostgreSQL connection
- **Scaling**: Automatic scaling based on traffic

### Configuration Management
- **Environment Variables**: DATABASE_URL, OPENAI_API_KEY
- **Path Aliases**: TypeScript path mapping for clean imports
- **Asset Handling**: Static file serving with proper caching headers

## Changelog

- June 27, 2025: Initial setup with vanilla HTML/CSS/JavaScript architecture
- June 27, 2025: Configured Deepseek R1 model integration with educational content filtering
- June 27, 2025: Implemented file upload support for images, PDFs, and documents
- June 27, 2025: Added mobile-first responsive design with dark theme
- June 27, 2025: Created conversation persistence and stop functionality
- June 28, 2025: Updated AI model to Google Gemma-2-9B via OpenRouter.ai per user preference
- June 28, 2025: Added text-to-speech functionality for AI responses with speaker controls
- June 28, 2025: Implemented custom educational keyboard with mathematical/scientific symbols

## User Preferences

Preferred communication style: Simple, everyday language.