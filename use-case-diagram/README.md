# Use Case Diagram Documentation

## Actors
1. **Guest** - User looking to book and stay at properties
2. **Host** - User who lists and manages properties
3. **Admin** - System administrator with oversight capabilities
4. **Payment Gateway** - External payment processing system
5. **Email Service** - External notification service

## Use Cases by Actor

### Guest Use Cases
- Register Account
- Login to System
- Search Properties
- View Property Details
- Book Property
- Make Payment
- Cancel Booking
- Write Review
- Manage Profile
- View Booking History

### Host Use Cases
- Register as Host
- Login to System
- Create Property Listing
- Edit Property Listing
- Delete Property Listing
- Manage Availability Calendar
- View Booking Requests
- Confirm/Reject Bookings
- Respond to Reviews
- View Earnings Report

### Admin Use Cases
- Manage User Accounts
- Moderate Property Listings
- View All Bookings
- Manage System Settings
- Generate Reports
- Handle Disputes
- View System Analytics

### External System Use Cases
- Process Payment (Payment Gateway)
- Send Notification (Email Service)
- Verify Payment (Payment Gateway)
- Store Files (Cloud Storage)

## Relationships
- **Include Relationships**: Booking includes Payment processing
- **Extend Relationships**: Property search can extend to filtering
- **Generalization**: Both Guest and Host inherit from User actor

## System Boundaries
The Airbnb Clone system encompasses all use cases related to property rental marketplace operations, excluding external system internal processes.
