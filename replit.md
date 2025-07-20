# Bunker Game - Online Multiplayer Survival Game

## Overview

This is a web application for an online version of the "Bunker" board game - a social survival game with role-playing and debate elements. The project is built as a full-stack application using modern web technologies with a focus on real-time multiplayer functionality.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a monorepo structure with separate client and server directories, sharing common types and schemas. It uses a modern full-stack TypeScript architecture with React frontend and Express.js backend.

### Directory Structure
- `/client` - React frontend with Vite build system
- `/server` - Express.js backend with TypeScript
- `/shared` - Common schemas, types, and utilities
- `/migrations` - Database migration files

## Key Components

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build System**: Vite with hot module replacement
- **UI Framework**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design system
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Forms**: React Hook Form with Zod validation
- **Sound**: Custom Web Audio API implementation for game sounds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ESM modules
- **Database**: PostgreSQL via Neon serverless with Drizzle ORM
- **Authentication**: Replit Auth with OpenID Connect integration
- **Session Management**: Express sessions with PostgreSQL storage
- **Real-time**: Socket.io ready (prepared for future multiplayer features)

### Database Design
- **ORM**: Drizzle with PostgreSQL dialect
- **Schema Management**: Type-safe schema definitions in shared directory
- **Key Tables**: 
  - `users` - Player profiles with game statistics
  - `sessions` - Authentication session storage
- **Features**: User profiles with nicknames, descriptions, game statistics, and premium status

## Data Flow

1. **Authentication**: Users authenticate via Replit Auth (OpenID Connect)
2. **Session Management**: Sessions stored in PostgreSQL with automatic cleanup
3. **API Communication**: RESTful API with JSON payloads
4. **Client State**: TanStack Query manages server state with optimistic updates
5. **Form Handling**: React Hook Form with Zod validation for type safety

## External Dependencies

### Core Dependencies
- **Database**: Neon PostgreSQL serverless platform
- **Authentication**: Replit Auth system
- **UI Components**: Radix UI primitives for accessibility
- **Styling**: Tailwind CSS for utility-first styling
- **Validation**: Zod for runtime type checking

### Development Tools
- **TypeScript**: Full type safety across the stack
- **Vite**: Fast development server and build tool
- **Drizzle Kit**: Database migrations and introspection
- **ESBuild**: Production backend bundling

## Deployment Strategy

### Development Environment
- **Frontend**: Vite dev server with HMR
- **Backend**: tsx for TypeScript execution in development
- **Database**: Neon serverless PostgreSQL

### Production Build
- **Frontend**: Vite builds to `dist/public` for static serving
- **Backend**: ESBuild bundles server code to `dist/index.js`
- **Database**: Migrations applied via Drizzle Kit

### Key Features
- **Mobile-first**: Responsive design optimized for mobile devices
- **Dark Theme**: Custom dark theme with game-specific color palette
- **Sound System**: Web Audio API integration for immersive experience
- **Type Safety**: End-to-end TypeScript with shared schemas
- **Authentication**: Secure session-based auth with Replit integration
- **Performance**: Optimized queries and caching strategies

## Recent Changes (Phase 1.4 - January 20, 2025)

### ✅ Room Creation & Management System
- **Enhanced Database Schema**: Added comprehensive room settings (password, time controls, survivor count, spectators)
- **Advanced Room Creation**: Full form with 9 catastrophe types including premium scenarios
- **Time Configuration**: Speech (30-120s), Discussion (30-180s), Voting (30-60s) settings
- **Room Discovery**: Public room listing with real-time refresh and filtering
- **Player Management**: Auto-start, webcam requirements, spectator controls
- **Premium Features**: Harry Potter, LOTR, and Cyberpunk themed scenarios

### 🚀 Current Capabilities
- Complete user authentication and profile management
- Advanced room creation with custom apocalypse scenarios
- Public room browsing and joining system
- Real-time room status updates
- Mobile-optimized interface with survival game theming

The architecture is designed to support the MVP phase with user authentication and profiles, while being extensible for future game features like real-time multiplayer rooms, character cards, and game logic.