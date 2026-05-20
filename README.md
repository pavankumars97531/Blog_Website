# 📝 Blog Website

A full-featured blog web application built with **Flask** and **Python**, where an admin can create, edit, and delete blog posts, and registered users can read and comment on them.

---

## Features

- **User Authentication** — Register, log in, and log out securely with hashed passwords
- **Role-Based Access** — Admin-only controls for creating, editing, and deleting posts
- **Rich Text Editor** — CKEditor integration for writing beautifully formatted blog posts
- **Comment System** — Logged-in users can leave comments on posts
- **Gravatar Support** — Profile avatars auto-generated from user email via Gravatar
- **Responsive UI** — Bootstrap 5-powered design that works on all screen sizes
- **About & Contact Pages** — Static informational pages included

---

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python, Flask |
| Database | SQLite (default) / PostgreSQL (via env var) |
| ORM | Flask-SQLAlchemy |
| Authentication | Flask-Login, Werkzeug |
| Forms | Flask-WTF |
| Rich Text | Flask-CKEditor |
| UI | Bootstrap 5, Flask-Bootstrap |
| Avatars | Flask-Gravatar |
| Deployment | Procfile (Heroku-ready) |

---

## Project Structure

```
Blog_Website/
├── main.py             # Main Flask application, routes, and DB models
├── forms.py            # WTForms form classes
├── requirements.txt    # Python dependencies
├── Procfile            # Heroku deployment config
├── .gitignore
├── static/             # CSS, JS, and image assets
└── templates/          # HTML templates (Jinja2)
```

---

## Getting Started

### Prerequisites

- Python 3.8+
- pip

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/pavankumars97531/Blog_Website.git
cd Blog_Website
```

2. **Install dependencies**

```bash
# Windows
python -m pip install -r requirements.txt

# macOS / Linux
pip3 install -r requirements.txt
```

3. **Set up environment variables**

Create a `.env` file in the root directory:

```env
MY_SECRET_KEY=your_secret_key_here
DB_URI=sqlite:///posts.db
```

> For production, replace `DB_URI` with your PostgreSQL connection string.

4. **Run the application**

```bash
python main.py
```

The app will be available at `http://localhost:5001`

---

## Usage

- The **first registered user** (user ID = 1) is automatically granted **admin privileges**.
- As admin, you can **create**, **edit**, and **delete** blog posts.
- Any registered user can **leave comments** on posts.
- Unregistered visitors can **read** posts but cannot comment.

---

## Deployment

This project includes a `Procfile` for easy deployment to **Heroku** or similar platforms.

Set the following environment variables on your hosting platform:

| Variable | Description |
|---|---|
| `MY_SECRET_KEY` | Flask secret key for session security |
| `DB_URI` | Database connection URI (PostgreSQL recommended for production) |

---

## License

This project is open source and available under the [MIT License](LICENSE).
