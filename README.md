# Hospital Management System

A full-stack hospital management system built with Django and React. The project is intended to help hospitals, clinics, and medical teams manage day-to-day operations such as patients, doctors, appointments, departments, medical records, billing, and administrative workflows.

## Technology Stack

- **Backend:** Django, Django REST Framework
- **Frontend:** React
- **Database:** PostgreSQL or SQLite for local development
- **Authentication:** Django authentication or JWT-based API authentication
- **API Format:** RESTful JSON APIs

## Core Features

- Patient registration and profile management
- Doctor and staff management
- Appointment scheduling and tracking
- Department and ward management
- Medical records and visit history
- Billing and payment records
- Role-based access for administrators, doctors, nurses, receptionists, and patients
- Dashboard views for operational summaries

## Project Structure

This repository is currently ready for a Django backend and React frontend. A recommended structure is:

```text
hospital-management-system/
├── backend/
│   ├── manage.py
│   ├── requirements.txt
│   └── ...
├── frontend/
│   ├── package.json
│   ├── src/
│   └── ...
├── README.md
└── .gitignore
```

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.10+
- Node.js 18+
- npm or yarn
- PostgreSQL, if using PostgreSQL instead of SQLite

## Backend Setup

From the project root:

```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

The Django API should be available at:

```text
http://localhost:8000/
```

## Frontend Setup

From the project root:

```bash
cd frontend
npm install
npm run dev
```

The React app should be available at:

```text
http://localhost:5173/
```

If the frontend is created with Create React App instead of Vite, use:

```bash
npm start
```

## Environment Variables

Create a `.env` file in the backend directory for local configuration:

```env
SECRET_KEY=your-django-secret-key
DEBUG=True
DATABASE_URL=sqlite:///db.sqlite3
ALLOWED_HOSTS=localhost,127.0.0.1
CORS_ALLOWED_ORIGINS=http://localhost:5173
```

For production, set secure values and disable debug mode:

```env
DEBUG=False
```

## API Development

The backend should expose REST endpoints for the frontend to consume. Example API groups may include:

```text
/api/auth/
/api/patients/
/api/doctors/
/api/appointments/
/api/departments/
/api/records/
/api/billing/
```

## Testing

Run backend tests:

```bash
cd backend
python manage.py test
```

Run frontend tests:

```bash
cd frontend
npm test
```

## Development Workflow

1. Create or update backend models, serializers, views, and URLs.
2. Run migrations after model changes.
3. Build React pages and components that consume the API.
4. Keep API responses consistent and documented.
5. Add tests for critical workflows such as authentication, appointments, billing, and medical records.

## Deployment Notes

Before deploying:

- Set `DEBUG=False`
- Configure production database credentials
- Set secure `SECRET_KEY`
- Configure allowed hosts and CORS origins
- Collect static files with Django
- Build the React frontend for production
- Serve the backend and frontend behind HTTPS

Example production commands:

```bash
cd backend
python manage.py collectstatic

cd ../frontend
npm run build
```

## Contributing

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes with clear messages.
4. Open a pull request describing the update.

## License

This project is currently not licensed. Add a license before distributing or using it in production.


