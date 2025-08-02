# Overview

This is a personalized Linux cloud server with QR code file access - a full-stack file management web application built with React and Express. The application provides a modern file manager interface that allows users to upload files to their personal cloud server and generate QR codes for easy mobile access. Staff can use this to manage files remotely and share them securely through QR codes that can be scanned from mobile devices.

# User Preferences

Preferred communication style: Simple, everyday language.
Project Purpose: Built for staff use - needs clear documentation and explanations for team members.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Framework**: Radix UI primitives with shadcn/ui components for accessible, customizable interface
- **Styling**: Tailwind CSS with CSS variables for theming support (light/dark modes)
- **Build Tool**: Vite for fast development and optimized builds

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database ORM**: Drizzle ORM for type-safe database operations
- **File Handling**: Multer middleware for multipart file uploads
- **Development**: Full-stack development setup with Vite middleware integration

## Data Storage
- **Database**: PostgreSQL with Drizzle ORM for schema management
- **File Storage**: Local filesystem storage in uploads directory
- **Schema Design**: 
  - Files table with hierarchical folder structure using parentId relationships
  - Support for both files and folders with isFolder boolean flag
  - Metadata tracking including file size, MIME type, and upload timestamps

## Key Features
- **File Management**: Upload, organize, and browse files in a hierarchical folder structure
- **QR Code Generation**: Generate QR codes for files to enable easy sharing
- **Responsive Design**: Mobile-first design with adaptive layouts
- **Drag & Drop**: Modern file upload with drag-and-drop support
- **File Preview**: Icon-based file type recognition and preview

## Development Architecture
- **Monorepo Structure**: Shared schema and types between client and server
- **Type Safety**: End-to-end TypeScript with shared interfaces
- **Hot Reload**: Vite development server with Express API integration
- **Path Aliases**: Organized imports with @ aliases for clean code structure

# External Dependencies

## Core Frontend Dependencies
- React 18 ecosystem (react, react-dom)
- TanStack Query for data fetching and caching
- Wouter for routing
- Radix UI component primitives for accessibility
- Tailwind CSS for styling
- date-fns for date formatting

## Backend Dependencies
- Express.js web framework
- Drizzle ORM with PostgreSQL adapter
- Neon Database serverless for PostgreSQL hosting
- Multer for file upload handling
- QRCode library for QR code generation
- Zod for runtime validation

## Development Tools
- Vite build tool and dev server
- TypeScript for type checking
- PostCSS with Autoprefixer
- ESBuild for server bundling
- Replit development environment integration

## Database
- PostgreSQL database (configured for Neon serverless)
- Drizzle Kit for schema migrations
- Connection via DATABASE_URL environment variable