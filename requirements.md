# Airbnb Clone - Technical Requirement Specifications

## 1. User Authentication System

### Functional Requirements
- Users can register with email, password, and user type (guest/host)
- Users can login with email/password or OAuth providers (Google, Facebook)
- Password reset functionality via secure email links
- Email verification for new accounts
- JWT token-based session management with refresh tokens
- Role-based access control (Guest, Host, Admin)

### Technical Specifications

#### API Endpoints:
```http
POST /api/auth/register
POST /api/auth/login
POST /api/auth/logout
POST /api/auth/forgot-password
POST /api/auth/reset-password
POST /api/auth/verify-email
POST /api/auth/refresh-token
GET /api/auth/me
