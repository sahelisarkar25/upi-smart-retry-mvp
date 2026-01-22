# upi-smart-retry-mvp
UPI Failure Tracker + Smart Retry (MVP)

A fintech-style UPI product MVP inspired by Paytm/GPay that improves payment trust by handling FAILED/PENDING scenarios with clear status tracking and smart retry flows.

Problem

UPI users often face:

Pending/timeout confusion

Failed payments without clarity

Too many customer support tickets

Drop-offs due to low trust

Solution (MVP Features)

Authentication: Login/Signup

Payment flow simulation: Processing → Payment Status

Failure Tracker: clear reason + next action

Smart Retry: retry without re-entering details, parent transaction linking

History: transaction list for the user

Transaction Details: timeline of status events (INITIATED → PENDING → SUCCESS/FAILED)

Tech Stack

FlutterFlow (no-code frontend)

Firebase Authentication

Firestore Database

Firestore Collections
users

name

email

created_at

transactions

txn_id

user_id

amount

payee_vpa

status (INITIATED/PENDING/SUCCESS/FAILED/CANCELLED)

failure_reason_text

retry_count

parent_txn_id

created_at

updated_at

resolved_at

status_events

txn_id

status

note

event_time

Metrics (planned)

Payment completion rate

Failure rate

Pending resolution time

Retry conversion rate

Duplicate retry risk signals


Roadmap

Add risk guardrails for retry during pending

Add “refund ETA” messaging

Support dashboard for failure reasons

Analytics event dictionary
