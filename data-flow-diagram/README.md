# Data Flow Diagram (DFD) Documentation

## Level 0 - Context Diagram

### External Entities:
- **Guest**: Provides booking requests, payment info, reviews
- **Host**: Provides property data, availability, booking responses
- **Admin**: Provides moderation actions, system configuration
- **Payment Gateway**: Processes payments, returns transaction status
- **Email Service**: Sends notifications to users

### Data Flows:
- Registration data → System
- Login credentials → System
- Property search criteria → System
- Booking requests → System
- Payment information → System
- Review content → System
- Notification data → Email Service
- Transaction data → Payment Gateway

## Level 1 - Major Processes

### 1. User Management Process
**Inputs**: Registration data, login credentials, profile updates
**Processes**: 
- Validate user input
- Hash passwords
- Generate JWT tokens
- Update user profiles
**Outputs**: User records, authentication tokens, profile data
**Data Stores**: Users table, Profiles table

### 2. Property Management Process  
**Inputs**: Property details, photos, availability data
**Processes**:
- Validate property data
- Store property images
- Update availability calendar
- Handle search queries
**Outputs**: Property listings, search results, availability status
**Data Stores**: Properties table, Amenities table, Photos table

### 3. Booking Management Process
**Inputs**: Booking requests, dates, guest details
**Processes**:
- Check availability
- Validate booking rules
- Create booking records
- Update availability
**Outputs**: Booking confirmations, availability updates
**Data Stores**: Bookings table, Availability table

### 4. Payment Processing
**Inputs**: Payment method, amount, booking details
**Processes**:
- Validate payment data
- Process with payment gateway
- Record transaction
- Update booking status
**Outputs**: Payment confirmations, transaction records
**Data Stores**: Payments table, Transactions table

### 5. Review System
**Inputs**: Review content, ratings, booking reference
**Processes**:
- Validate review eligibility
- Store review data
- Calculate average ratings
- Notify relevant parties
**Outputs**: Review records, updated ratings
**Data Stores**: Reviews table, Ratings table

## Data Stores
- **Users Database**: User accounts, profiles, authentication data
- **Properties Database**: Listings, amenities, photos, availability
- **Bookings Database**: Reservations, dates, status, guest info
- **Payments Database**: Transactions, payment methods, receipts
- **Reviews Database**: Reviews, ratings, responses

## Data Flow Rules
- All sensitive data must be encrypted in transit (HTTPS)
- Payment data never stored directly - use tokenization
- Personal data subject to privacy regulations
- Audit trails for all financial transactions
