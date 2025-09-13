# Overview

This is a multi-tool file processing web application built with React and Express. The app provides various image and PDF manipulation tools including image resizing, compression, cropping, format conversion, PDF creation/merging, OCR text extraction, and QR code generation. It's designed as a comprehensive file processing suite with a modern, responsive interface.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter for lightweight client-side routing
- **UI Components**: Radix UI primitives with shadcn/ui styling system
- **Styling**: Tailwind CSS with CSS custom properties for theming
- **State Management**: React Query (@tanstack/react-query) for server state management
- **Form Handling**: React Hook Form with Zod validation
- **Build Tool**: Vite for fast development and optimized production builds

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Language**: TypeScript with ES modules
- **Development**: tsx for TypeScript execution in development
- **File Handling**: Multer for multipart form uploads with 10MB size limit
- **Storage**: In-memory storage implementation with interface for future database integration
- **API Design**: RESTful endpoints under `/api` prefix

## Data Storage Solutions
- **Database ORM**: Drizzle ORM configured for PostgreSQL
- **Current Storage**: MemStorage class providing in-memory data persistence
- **Database Schema**: Users and ProcessedFiles tables with metadata support
- **Migration Support**: Drizzle Kit for schema migrations
- **Connection**: Neon Database serverless PostgreSQL integration ready

## File Processing Capabilities
- **Image Processing**: Client-side processing using Canvas API for resize, compress, crop, and format conversion
- **PDF Operations**: jsPDF for PDF creation and manipulation
- **OCR**: Tesseract.js for optical character recognition
- **QR Codes**: qrcode library for QR code generation
- **File Uploads**: Drag-and-drop interface with camera capture support

## Authentication and Authorization
- **Current State**: Basic user schema defined but not implemented
- **Planned**: Session-based authentication with PostgreSQL session store (connect-pg-simple)
- **User Management**: Username/password authentication system ready for implementation

# External Dependencies

## UI and Styling
- **Radix UI**: Complete set of accessible UI primitives (@radix-ui/react-*)
- **Tailwind CSS**: Utility-first CSS framework with custom configuration
- **Lucide React**: Modern icon library for consistent iconography
- **Class Variance Authority**: Utility for managing CSS class variants

## File Processing Libraries
- **Tesseract.js**: Client-side OCR capabilities for text extraction from images
- **jsPDF**: PDF generation and manipulation in the browser
- **qrcode**: QR code generation with customization options
- **react-dropzone**: File upload interface with drag-and-drop support

## Database and Backend
- **Neon Database**: Serverless PostgreSQL database service (@neondatabase/serverless)
- **Drizzle ORM**: Type-safe ORM with PostgreSQL support
- **Express.js**: Web application framework for API endpoints
- **Multer**: File upload middleware for handling multipart/form-data

## Development Tools
- **Vite**: Fast build tool with TypeScript support
- **React Query**: Server state management and caching
- **React Hook Form**: Form handling with validation
- **Zod**: Schema validation and type inference

## Replit Integration
- **Development Plugins**: Error overlay and cartographer for enhanced Replit experience
- **Hot Reload**: Development server with HMR support
- **Asset Management**: Configured asset paths for Replit environment