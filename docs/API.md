# API Design

## Authentication APIs

POST /register

POST /login

POST /logout

---

## User APIs

GET /users/profile

PUT /users/profile

---

## Vendor APIs

POST /vendors/register

GET /vendors

GET /vendors/{id}

PUT /vendors/{id}

---

## Review APIs

POST /reviews

GET /reviews/{vendorId}

---

## Complaint APIs

POST /complaints

GET /complaints

---

## Admin APIs

GET /pending-vendors

PUT /approve-vendor

DELETE /remove-review