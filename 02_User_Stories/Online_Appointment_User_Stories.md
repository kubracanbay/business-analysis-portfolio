# User Stories – Online Appointment System

The following user stories describe the main actions that users and service providers can perform in the system. Each story includes acceptance criteria to define the expected behavior and success conditions.

---

## 1. User Registration

**User Story:**  
As a user, I want to create an account so that I can book and manage appointments online.

**Acceptance Criteria:**  
- The registration form includes name, email, and password fields.  
- A confirmation email is sent after successful registration.  
- Duplicate email addresses are not allowed.  
- Password must contain at least 8 characters.

---

## 2. Login and Authentication

**User Story:**  
As a registered user, I want to log in to my account so that I can access my appointments.

**Acceptance Criteria:**  
- The system verifies email and password.  
- An error message appears for incorrect credentials.  
- The user session remains active until logout.

---

## 3. View Available Time Slots

**User Story:**  
As a user, I want to see available time slots so that I can choose the most suitable time for my appointment.

**Acceptance Criteria:**  
- The system displays all open time slots based on the provider’s schedule.  
- Past or unavailable slots are not shown.  
- The displayed times update automatically if a slot is booked.

---

## 4. Create a New Appointment

**User Story:**  
As a user, I want to book an appointment so that I can meet with a service provider at a specific time.

**Acceptance Criteria:**  
- Users can select a date and time slot from the available list.  
- The system prevents double bookings.  
- The user receives a confirmation email or SMS after the booking is saved.

---

## 5. Reschedule or Cancel Appointment

**User Story:**  
As a user, I want to change or cancel my existing appointment so that I can manage my schedule easily.

**Acceptance Criteria:**  
- The user can select another available slot to reschedule.  
- Cancellations are only allowed at least two hours before the appointment.  
- The system updates the provider’s availability after any change.

---

## 6. Provider Availability Management

**User Story:**  
As a service provider, I want to set my working hours so that users can only book appointments within those times.

**Acceptance Criteria:**  
- Providers can define available days and hours.  
- The system updates the public schedule automatically.  
- Bookings outside of defined hours are not possible.

---

## 7. Notifications

**User Story:**  
As a user, I want to receive reminders and updates so that I don’t miss or forget my appointment.

**Acceptance Criteria:**  
- The system sends confirmation after booking or rescheduling.  
- A reminder is sent 24 hours before the appointment.  
- Notifications are sent by email or SMS depending on the user’s preference.

---

## 8. Admin Monitoring

**User Story:**  
As an admin, I want to monitor appointments and user activity so that I can manage the system effectively.

**Acceptance Criteria:**  
- Admins can view all upcoming appointments and user details.  
- Admins can deactivate users or providers if necessary.  
- The admin dashboard provides simple search and filtering options.

---

*End of document.*
