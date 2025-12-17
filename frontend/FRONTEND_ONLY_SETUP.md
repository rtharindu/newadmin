# Frontend-Only Setup Guide

## Overview
This frontend has been converted to frontend-only mode, connecting to an external backend API.

## Environment Setup
1. Copy `env.example` to `.env.local`
2. Update `NEXT_PUBLIC_API_URL` to point to your backend server

## Installation
```bash
npm install
```

## Development
```bash
npm run dev
```

## Backend API Endpoints Expected
- `POST /api/auth/login` - Authentication
- `POST /api/auth/forgot-password` - Password reset request
- `POST /api/auth/verify-otp` - OTP verification
- `POST /api/auth/reset-password` - Password reset

## Removed Components
- Prisma database setup
- API routes (now handled by backend)
- Database dependencies
- Authentication middleware (backend handles)

## Architecture
- Frontend: Next.js 14 with App Router
- Backend: Separate service (Node.js/Express recommended)
- Communication: HTTP API calls
- Authentication: JWT tokens from backend
