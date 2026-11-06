# Food Waste Donation Platform — Architecture

## Technology stack
- Frontend: React.js with Vite
- Backend: Node.js with Express
- Database: MySQL (Aiven-compatible)

## Core roles
- Donor: publish surplus food and manage donations.
- NGO: discover listings and reserve eligible donations.
- Volunteer: coordinate and update pickups.
- Administrator: moderate users/listings and monitor platform activity.

## Core workflow
1. A donor creates a food listing with quantity, preparation time, expiry time, storage conditions, allergens, and pickup window.
2. An NGO reserves an eligible listing.
3. The donor confirms the reservation and pickup details.
4. A volunteer or NGO updates pickup and delivery status.
5. The platform stores status history for traceability.

## Safety and integrity
- Expired listings cannot be reserved.
- Quantities cannot be reserved beyond the available amount.
- Food safety is the donor's responsibility; the platform does not certify food.
- Secrets and database credentials belong in backend environment variables, never in committed files.

## Planned modules
Authentication, food listings, reservations, pickup coordination, notifications, admin dashboard, and reporting.
