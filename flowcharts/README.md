# Flowcharts Documentation

## Booking Process Flowchart

### Start → Property Search
1. **User Action**: Guest searches for properties
2. **System Action**: Validate search parameters
3. **Decision**: Valid parameters?
   - No: Return error message
   - Yes: Query database

### Availability Check
4. **System Action**: Check property availability for dates
5. **Decision**: Property available?
   - No: Show alternative properties or dates
   - Yes: Display property details

### Booking Creation
6. **User Action**: Select dates and proceed to booking
7. **System Action**: Calculate total cost including fees
8. **User Action**: Confirm booking details
9. **System Action**: Create pending booking record

### Payment Processing
10. **User Action**: Enter payment information
11. **System Action**: Validate payment data
12. **Decision**: Payment valid?
    - No: Return to payment step with error
    - Yes: Process payment via gateway

### Payment Result
13. **System Action**: Receive payment gateway response
14. **Decision**: Payment successful?
    - No: Notify user, free up dates
    - Yes: Confirm booking, update availability

### Confirmation & Notification
15. **System Action**:
    - Update booking status to "confirmed"
    - Send confirmation email to guest
    - Send notification to host
    - Update property availability calendar

### End Process
16. **System Action**: Return booking confirmation to user
17. **End**: Booking process complete

## User Registration Flowchart

### Start → Registration Form
1. **User Action**: Access registration page
2. **User Action**: Fill email, password, user type (guest/host)
3. **System Action**: Validate input format

### Validation Check
4. **Decision**: All fields valid?
   - No: Show specific error messages
   - Yes: Check email uniqueness

### Email Check
5. **System Action**: Query database for existing email
6. **Decision**: Email already exists?
   - Yes: Show "email taken" error
   - No: Create user account

### Account Creation
7. **System Action**:
   - Hash password with bcrypt
   - Create user record with "unverified" status
   - Generate email verification token
   - Send verification email

### Email Verification
8. **User Action**: Click verification link in email
9. **System Action**: Validate verification token
10. **Decision**: Token valid?
    - No: Show error, offer to resend verification
    - Yes: Activate user account

### Completion
11. **System Action**:
    - Update user status to "active"
    - Generate JWT token
    - Log user in automatically
12. **End**: Registration complete, redirect to dashboard
