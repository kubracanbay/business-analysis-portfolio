# SQL Data Validation – PostgreSQL Version

These SQL queries are used to verify data integrity and business rules for the Online Appointment System.  
They are written specifically for PostgreSQL syntax and align with the rules defined in the BRD and Test Cases.

---

## 1. Detect Double Bookings
Checks if a provider has more than one booking in the same time slot.

```sql
SELECT provider_id, start_time, COUNT(*) AS cnt
FROM appointments
WHERE status = 'active'
GROUP BY provider_id, start_time
HAVING COUNT(*) > 1;

Expected Result:
No records should be returned. Each time slot can only be booked once per provider.

sql

SELECT a.id, a.user_id, a.start_time, a.cancelled_at
FROM appointments a
WHERE a.cancelled_at IS NOT NULL
  AND a.start_time - a.cancelled_at < INTERVAL '2 hour';

Expected Result:
No results. All cancellations must occur at least two hours before the appointment


sql


SELECT n.appointment_id, n.channel, n.sent_at
FROM notifications n
JOIN appointments a ON a.id = n.appointment_id
WHERE a.created_at >= NOW() - INTERVAL '1 day';

Expected Result:
At least one record per booking in the last 24 hours.
Each booking or reschedule event should trigger a corresponding notification.

sql


SELECT a.id, a.provider_id, a.start_time
FROM appointments a
LEFT JOIN provider_hours h
  ON a.provider_id = h.provider_id
 AND EXTRACT(DOW FROM a.start_time) = h.weekday
WHERE (a.start_time::time < h.start_time)
   OR (a.start_time::time > h.end_time);

Expected Result:
No records should appear. All booked times must fall within the provider’s working hours.

sql

SELECT l.user_id, l.ip_address, l.attempt_time, s.alert_level
FROM login_attempts l
LEFT JOIN security_alerts s ON l.id = s.login_attempt_id
WHERE l.ip_address IN (SELECT ip FROM blocked_ips)
   OR s.alert_level IS NOT NULL;

Expected Result:
All suspicious IP logins should have corresponding entries in the security_alerts table.
If alerts are missing, the logging or detection mechanism needs review.

Execution Notes
Run these queries on the staging or test database, not in production.
For daily automation, integrate queries into a scheduled report or alert system.
Use a read-only connection when validating live data

--end---

