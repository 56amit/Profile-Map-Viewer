# 📚 Book Review API

This is a full-fledged backend API built using **FastAPI**, **PostgreSQL**, and **Redis**.  
It allows users to add books, fetch book listings, and post reviews per book.  
Includes Redis caching, Alembic migrations, and Swagger-based API testing.

---

## 🚀 Features

- 📘 Add and List Books
- 📝 Add and View Reviews per Book
- ⚡ Redis Cache for Fast Book Retrieval
- 🗃️ PostgreSQL with SQLAlchemy ORM
- 🧬 Alembic for DB Migrations
- 🔐 Environment-based DB config via `.env`
- 📄 Auto-generated Swagger Docs
- 🧪 Unit Testing with Pytest

---

## 🛠️ Tech Stack

| Layer      | Technology     |
|------------|----------------|
| Backend    | FastAPI        |
| DB         | PostgreSQL     |
| ORM        | SQLAlchemy     |
| Caching    | Redis          |
| Migration  | Alembic        |
| Testing    | Pytest         |
| Docs       | Swagger (FastAPI) |
| Server     | Uvicorn        |
| Env Mgmt   | python-dotenv  |

---

## 📁 Folder Structure

book-review-api/
│
├── app/
│ ├── routes/ # API endpoints (books, reviews)
│ ├── models/ # SQLAlchemy models
│ ├── schemas/ # Pydantic schemas
│ ├── database.py # DB connection & setup
│ └── main.py # Entry point with routers
│
├── migrations/ # Alembic migration scripts
├── requirements.txt # Python dependencies
├── alembic.ini # Alembic config
├── .env # Environment variables
└── README.md # This file

yaml
Copy
Edit

---

## ⚙️ Local Setup (Windows + VS Code)

### ✅ Step 1: Clone the Repo
```bash
git clone https://github.com/your-username/book-review-api.git
cd book-review-api
✅ Step 2: Create & Activate Virtual Environment
bash
Copy
Edit
python -m venv venv
.\venv\Scripts\activate
✅ Step 3: Install Dependencies
bash
Copy
Edit
pip install -r requirements.txt
✅ Step 4: Setup PostgreSQL Database
Open pgAdmin

Create new DB: bookdb

Use your PostgreSQL username & password

✅ Step 5: Set Environment Variable
Create a .env file in root folder:

ini
Copy
Edit
DATABASE_URL=postgresql://<your-username>:<your-password>@localhost:5432/bookdb
Example (Do not share publicly):
DATABASE_URL=postgresql://postgres:mySecurePass@localhost:5432/bookdb

✅ Step 6: Run Alembic Migration
bash
Copy
Edit
alembic upgrade head
✅ Step 7: Start the Server
bash
Copy
Edit
uvicorn app.main:app --reload
🔗 Swagger API Docs
📘 http://127.0.0.1:8000/docs

🔥 API Endpoints
Method	Endpoint	Description
GET	/books	List all books
POST	/books	Add a new book
GET	/books/{book_id}/reviews	List reviews
POST	/books/{book_id}/reviews	Add a review

✅ Run Tests (Optional)
bash
Copy
Edit
pytest tests/
🌱 Future Enhancements
JWT-based Authentication

User Login & Register APIs

Admin Book Approval Panel

Docker Deployment

🙌 Author
Amit Kumar Pandey
Frontend & Backend Developer
📧 amit760729@gmail.com
📞 7607297771

