# Boonix — Event Booking Platform

Full-stack event booking project using React/TypeScript, Material UI, Node.js, Express and MySQL.

## Features
- Browse and manage events and reservations
- JWT-based login and role-protected API endpoints
- REST APIs for users, events and bookings
- Optional image uploads to AWS S3

## Setup
1. Set up MySQL using the checked-in schema files, and create a dedicated least-privilege database user.
2. Copy `backend/.env.example` to `backend/.env`; replace the placeholders with **new** local values. Never commit your .env.
3. From `backend/`, run `npm ci` and `npm run dev`.
4. From `frontend/frontend/`, run `npm ci` and `npm start`.

See `backend/routes/` for the implemented endpoints. The old prototype tests under `backend/tests/` were written for a different Sequelize model structure and must be rewritten against the current mysql2 implementation before they can be treated as passing coverage.

## Security note
Past versions tracked credentials and generated dependencies. The tracked .env files and hard-coded backend database password have been removed from the current branch. Rotate any real DB password and other exposed credentials; historical commits remain accessible until cleaned separately. Do not use any historical values.
