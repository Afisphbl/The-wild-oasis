# The Wild Oasis

The Wild Oasis is a hotel operations dashboard for internal staff.
It helps teams manage cabins, bookings, check-ins/check-outs, guests, and business settings from one interface.

## What This App Does

- Authenticated staff login and protected routes
- Dashboard with operational stats and charts
- Cabin management (create, update, duplicate, delete)
- Booking management with filtering and sorting
- Booking details with check-in/check-out flows
- Hotel settings management (pricing and booking constraints)
- User account management (update profile and password)
- Dark mode support with persisted preference

## Tech Stack

- React 19
- Vite 8
- React Router DOM 6
- TanStack React Query 4
- Supabase (database + auth)
- Styled Components
- React Hook Form
- Recharts
- React Hot Toast
- Date-fns
- ESLint 9

## Project Structure

```text
.
|-- public/
|   |-- netlify.toml
|   `-- screenshots/
|-- src/
|   |-- context/            # app-wide providers (dark mode)
|   |-- data/               # seed/mock data and upload helpers
|   |-- features/           # domain modules
|   |   |-- authentication/
|   |   |-- bookings/
|   |   |-- cabins/
|   |   |-- check-in-out/
|   |   |-- dashboard/
|   |   `-- settings/
|   |-- hooks/              # reusable custom hooks
|   |-- pages/              # route-level pages
|   |-- services/           # Supabase and API access layer
|   |-- styles/             # global style tokens and themes
|   |-- ui/                 # shared presentational components
|   `-- utils/              # helpers and constants
|-- index.html
|-- package.json
`-- vite.config.js
```

## Routing Overview

- `/login`
- `/dashboard`
- `/bookings`
- `/bookings/:bookingId`
- `/checkin/:bookingId`
- `/cabins`
- `/users`
- `/settings`
- `/account`

All app routes except `/login` are protected behind authentication.

## Screenshots

### Login

![Login](public/screenshots/The%20Wild%20Oasis%20-%20Login.png)

### Dashboard/Home

![Home](public/screenshots/The%20Wild%20Oasis%20-%20Home.png)

### Cabins

![Cabins](public/screenshots/The%20Wild%20Oasis%20-%20Cabin.png)

### Create New Cabin

![Create New Cabin](public/screenshots/The%20Wild%20Oasis%20-%20Create-new-cabin.png)

### Cabin Settings / Actions

![Cabin Actions](public/screenshots/The%20Wild%20Oasis%20-%20Cabin-setting.png)

### Bookings

![Bookings](public/screenshots/The%20Wild%20Oasis%20-%20Booking.png)

### Settings

![Settings](public/screenshots/The%20Wild%20Oasis%20-%20Setting.png)

### Users

![Users](public/screenshots/The%20Wild%20Oasis%20-%20User.png)

### Delete Confirmation

![Delete Popup](public/screenshots/The%20Wild%20Oasis%20-%20Delete-popup.png)

## Getting Started

### Prerequisites

- Node.js 18+
- npm 9+

### Install and Run

```bash
npm install
npm run dev
```

### Build for Production

```bash
npm run build
npm run preview
```

### Lint

```bash
npm run lint
```

## Environment and Backend Notes

- The app uses Supabase for authentication and data storage.
- Supabase client setup lives in `src/services/supabase.js`.
- For production hardening, move Supabase URL/key values to environment variables (`.env`) and avoid committing secrets.

## Future Improvements

- Role-based access control (admin vs staff permissions)
- Better audit logs for booking and cabin mutations
- Pagination and virtualization for larger datasets
- CSV/PDF exports for reporting
- Offline-friendly caching strategy
- E2E test coverage (Playwright/Cypress)
- CI/CD checks for lint, tests, and build
- Internationalization (i18n) and multi-currency support

## Author

- Afisphbl

## License

This project is for educational and portfolio purposes. Add a formal license if you plan to distribute or open-source it.
