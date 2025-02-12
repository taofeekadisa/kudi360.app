# Kudi360 - Expense Management Solution

## <b>Overview</b>

<p>
Kudi360 is a FastAPI-powered expense management solution that helps users track, report, and manage expenses efficiently. The platform supports user authentication, expense tracking, budget management, and financial reporting, with AWS S3 integration for storing receipts and reports.
</p>

## <b>Features</b>

✅ User Management – Registration, login (JWT & OAuth), profile updates.

✅ Expense Tracking – Add, edit, delete, and categorize expenses.

✅ Expense Reports – Generate, download, and store reports in AWS S3.

✅ Budget Management – Set spending limits and track expenses.

✅ Notifications – Get email and push notifications for financial updates.

✅ Admin Dashboard – Manage users, expenses, and system configurations.

✅ Secure Authentication – JWT-based authentication with role-based access control.

✅ Scalable API – Built with FastAPI and PostgreSQL.

## <b>Tech Stack</b>
<ul>
<li>Backend: FastAPI (Python) </li>
<li>Database: PostgreSQL </li>

<li>Storage: AWS S3 (For receipts & reports)</li>
<li>Caching & Queue: Redis + Celery </li>
<li>Authentication: JWT & OAuth2 </li>
<li>Deployment: Docker, AWS (EC2, Lambda, S3) </li>
</ul>

## <b>Getting Started</b>

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/kudi360.git
cd kudi360

```

### 2. Set Up Virtual Environment

```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

```

### 3. Install Dependencies

```bash
pip install -r requirements.txt

```

### 4. Set Up Environment Variables

```ini
DATABASE_URL=postgresql://user:password@localhost:5432/kudi360db
AWS_ACCESS_KEY_ID=your_aws_access_key
AWS_SECRET_ACCESS_KEY=your_aws_secret_key
S3_BUCKET_NAME=your_s3_bucket_name
JWT_SECRET=your_jwt_secret
EMAIL_HOST=email.smtp.com
EMAIL_PORT=587

```

### 5. Run Database Migrations

```bash
alembic upgrade head

```

### 6. Start the Application

```bash
uvicorn app.main:app --reload

```

## <b>API Documentation</b>

Once the server is running, access API docs:

<ul>
<li> Swagger UI: http://127.0.0.1:8000/docs </li>
<li> ReDoc: http://127.0.0.1:8000/redoc </li>
</ul>

## <b>Docker Setup</b>
<p> To run the app using Docker, execute: </p>

```bash
docker-compose up --build

```

## <b>Running Tests</b>
<p> To run unit and integration tests: </p>

```bash
pytest

```