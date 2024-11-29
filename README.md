# django-react-fullstack Note-Taking App

A simple, full-stack note-taking application built with Django for the backend and React (powered by Vite) for the frontend. This app provides an intuitive interface for creating, editing, and deleting notes.

---

## Features

- Full-stack implementation with Django and React.
- CRUD operations for notes (Create, Read, Update, Delete).
- Modern React frontend using Vite for fast builds and development.
- RESTful API built with Django REST Framework.

---

## Getting Started

### Prerequisites

- Python 3.8+
- Node.js 14+ with npm or yarn
- PostgreSQL (optional for deployment)

---

## Project Setup

### Backend Setup (Django)

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/django-react-fullstack.git
   cd django-react-fullstack/backend
   ```

2. **Create and activate a virtual environment**

   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Run migrations**

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Start the backend server**
   ```bash
   python manage.py runserver
   ```

---

### Frontend Setup (React with Vite)

1. **Navigate to the frontend directory**

   ```bash
   cd ../frontend
   ```

2. **Install dependencies**  
   Using npm:

   ```bash
   npm install
   ```

   Or using yarn:

   ```bash
   yarn install
   ```

3. **Start the development server**  
   Using npm:

   ```bash
   npm run dev
   ```

   Or using yarn:

   ```bash
   yarn dev
   ```

4. **Access the application**
   - React frontend: Visit [http://localhost:5173](http://localhost:5173) (default Vite port).
   - Django backend: Visit [http://localhost:8000](http://localhost:8000).

---

## Project Structure

```
django-react-fullstack/
│
├── backend/
│   ├── notes/          # Django app for notes
│   ├── manage.py       # Django project manager
│   ├── settings.py     # Project configuration
│   └── urls.py         # URL routing
│
└── frontend/
    ├── src/
    │   ├── components/ # React components
    │   ├── pages/      # React pages
    │   ├── App.jsx     # Main App component
    │   └── index.jsx   # React entry point
    ├── vite.config.js  # Vite configuration
    ├── package.json    # Frontend dependencies
    └── public/
```

---

## API Endpoints

| Method | Endpoint         | Description             |
| ------ | ---------------- | ----------------------- |
| GET    | `/api/notes/`    | Retrieve all notes      |
| GET    | `/api/notes/:id` | Retrieve a single note  |
| POST   | `/api/notes/`    | Create a new note       |
| PUT    | `/api/notes/:id` | Update an existing note |
| DELETE | `/api/notes/:id` | Delete a note           |

---

## Deployment

### Backend (Django)

1. Update `DATABASES` in `settings.py` to use PostgreSQL for production.
2. Install `gunicorn` or another WSGI server:
   ```bash
   pip install gunicorn
   ```
3. Collect static files for production:

   ```bash
   python manage.py collectstatic
   ```

4. Use a reverse proxy (e.g., Nginx) to serve the Django application.

### Frontend (React with Vite)

1. Build the React app for production:
   ```bash
   npm run build  # or yarn build
   ```
2. Serve the `dist` folder using a CDN or integrate it with Django’s `STATICFILES_DIRS`.

---

## Technologies Used

- **Backend**: Django, Django REST Framework
- **Frontend**: React, Vite, Axios
- **Database**: SQLite (default)

---

## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request.

---

## Contact

For questions or suggestions, please contact [shasigdel@gmail.com](mailto:shasigdel@gmail.com).

---
