# Vegetable Shop Website + Mobile App

Simple full-stack billing website for a vegetable shop with:
- Vegetable menu CRUD with images
- Click-to-add cart billing
- Quantity support from 0.5kg to 20kg
- Pay Now with QR code
- Print bill
- Clear cart
- Monthly sales report

## Tech Stack
- Web frontend: React + TypeScript + Vite
- Mobile app: React Native + Expo
- Backend: Node.js + Express
- Database: SQLite

## Project Structure
- `frontend/` customer billing UI, menu management UI, reports UI
- `mobile/` mobile customer app (billing, QR payment flow, report view)
- `backend/` APIs, SQLite schema, billing logic

## Setup
1. Install Node.js (includes `npm`).
2. Install dependencies:
   - `npm install`
   - `npm --prefix backend install`
   - `npm --prefix frontend install`
   - `npm --prefix mobile install`
3. Run both frontend and backend:
   - `npm run dev`
4. Open frontend at `http://localhost:5173`
5. Run mobile app:
   - `npm run dev:mobile`

If testing from a real phone, set `mobile/src/api.ts` `API_BASE` to your computer IP (for example `http://192.168.1.8:4000/api`) instead of `localhost`.

Backend runs on `http://localhost:4000`.

## Main APIs
- `GET /api/vegetables`
- `POST /api/vegetables`
- `PUT /api/vegetables/:id`
- `DELETE /api/vegetables/:id`
- `POST /api/orders`
- `PATCH /api/orders/:id/pay`
- `GET /api/orders/:id`
- `GET /api/reports/monthly?month=4&year=2026`

## Usage Flow
1. Open **Billing** page.
2. Click a vegetable card to add directly to bill.
3. Adjust kg quantity in cart (0.5 steps).
4. Click **Pay Now** to generate QR.
5. Click **Mark Paid** after payment.
6. Click **Print Bill** for invoice print.
7. Open **Monthly Report** page to view sales.

## Testing
- Backend billing tests:
  - `npm --prefix backend test`
