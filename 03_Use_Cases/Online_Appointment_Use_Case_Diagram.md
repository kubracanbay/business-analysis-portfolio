# Use Cases – Online Appointment System

This section describes the main use cases for the Online Appointment System. Each use case focuses on how the user interacts with the system to achieve a specific goal.

---

## 1. Register User Account

**Use Case ID:** UC-01  
**Actor:** User  
**Description:** The user creates a new account to access the system.  
**Preconditions:** The user has a valid email address.  
**Postconditions:** The account is created, and a confirmation email is sent.  

**Main Flow:**
1. User clicks on the “Sign Up” button.  
2. System displays the registration form.  
3. User enters name, email, and password.  
4. User submits the form.  
5. System validates inputs and creates the account.  
6. Confirmation email is sent to the user.

**Alternative Flow:**
- If the email is already registered, the system displays an error message.

---

## 2. Login to the System

**Use Case ID:** UC-02  
**Actor:** User  
**Description:** The user logs in using valid credentials.  
**Preconditions:** User account exists.  
**Postconditions:** User is redirected to the dashboard.

**Main Flow:**
1. User opens the login page.  
2. User enters email and password.  
3. System verifies the credentials.  
4. If valid, user is logged in successfully.

**Alternative Flow:**
- If credentials are invalid, the system displays an error message.

---

## 3. Book an Appointment

**Use Case ID:** UC-03  
**Actor:** User  
**Description:** The user books an available appointment slot.  
**Preconditions:** User is logged in. Provider has available time slots.  
**Postconditions:** Appointment is confirmed and visible on the user dashboard.

**Main Flow:**
1. User navigates to “Book Appointment”.  
2. System displays available time slots.  
3. User selects a provider, date, and time.  
4. System checks for conflicts and saves the booking.  
5. Confirmation email/SMS is sent.

**Alternative Flow:**
- If the selected time slot is no longer available, the system asks the user to choose another.

---

## 4. Reschedule or Cancel Appointment

**Use Case ID:** UC-04  
**Actor:** User  
**Description:** The user modifies or cancels a previously booked appointment.  
**Preconditions:** The appointment exists.  
**Postconditions:** The schedule is updated, and provider availability changes accordingly.

**Main Flow:**
1. User opens the appointment list.  
2. User selects the appointment to edit or cancel.  
3. System verifies the request.  
4. If valid, appointment is updated or removed.  
5. Notification is sent to confirm the action.

**Alternative Flow:**
- If the appointment is within 2 hours, cancellation is not allowed.

---

## 5. Manage Provider Availability

**Use Case ID:** UC-05  
**Actor:** Service Provider  
**Description:** The service provider defines or updates available time slots.  
**Preconditions:** Provider account exists.  
**Postconditions:** Updated schedule is reflected in the system.

**Main Flow:**
1. Provider logs into the system.  
2. Provider navigates to “Manage Availability”.  
3. Provider selects working days and time intervals.  
4. System updates the schedule and prevents conflicts.

---

## 6. Receive Notifications

**Use Case ID:** UC-06  
**Actor:** User, Service Provider  
**Description:** Users and providers receive notifications about bookings and changes.  
**Preconditions:** Appointment exists.  
**Postconditions:** Notification is successfully sent.

**Main Flow:**
1. System triggers a notification after each booking, reschedule, or cancellation.  
2. Notification is sent via email or SMS.  
3. Users can confirm receipt or ignore.

---

## 7. View Reports (Admin)

**Use Case ID:** UC-07  
**Actor:** Admin  
**Description:** The admin reviews overall activity and manages users or providers.  
**Preconditions:** Admin is logged in.  
**Postconditions:** Reports are displayed with updated data.

**Main Flow:**
1. Admin opens the “Reports” section.  
2. System shows a list of appointments, providers, and users.  
3. Admin filters results as needed.  
4. Admin can deactivate a user or provider if required.

---

*End of document.*
