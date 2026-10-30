# ELEVATE-SDE-Task-3 — CredVault Backend

## Technology
- Node.js
- Express.js
- SQLite
- JWT authentication
- bcryptjs
- CORS

## Run
```bash
npm install
npm start
```
API: `http://localhost:5000`

## Default Admin
Username: `admin`
Password: `admin`

## Required APIs
- POST `/api/applications`
- GET `/api/applications/track/:applicationId`
- GET `/api/certificates/verify/:certificateId`
- POST `/api/admin/login`
- GET `/api/admin/applications`
- PATCH `/api/admin/applications/:applicationId/approve`
- PATCH `/api/admin/applications/:applicationId/reject`
- GET `/api/admin/certificates`
- GET `/api/admin/certificates/:certificateId/revoke`

Protected admin endpoints require:
`Authorization: Bearer YOUR_TOKEN`

## Database
Applications, Certificates, and Admins tables are created automatically in SQLite.

Approving an application creates a certificate. Revoking a certificate changes only the certificate status to `Revoked`; the application remains unchanged.

This project implements ELEVATE SDE Internship Task 3 — Backend Development: API & Database.
