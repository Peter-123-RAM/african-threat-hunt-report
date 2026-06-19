Hunt Queries

Query 1

Identify OTP submissions from multiple IP addresses.

Logic:

Group OTP submissions by user session.

Alert when:

- OTP submitted from a different IP than login.
- OTP submitted within 5 minutes of login.

---

Query 2

Identify wallet transfers immediately following OTP validation.

Logic:

Search for:

POST /otp

followed by:

POST /wallet-transfer

within 10 minutes.

---

Query 3

Identify repeated transfer attempts from a newly observed IP.

Logic:

Count wallet-transfer requests.

Alert when:

More than 2 transfer requests occur within 5 minutes after OTP validation.
