# Learning Log

A web app for organizing what you're learning — create topics, then keep dated entries under each one.

---

## What it does

- **Topics** — create subjects you're studying
- **Entries** — dated, editable notes under each topic
- **User accounts** — registration and login, with each user seeing only their own topics
- **Access control** — entries are scoped to their owner

## Stack

`Python` · `Django` · `SQLite`

---

## What I learned

Django's ORM and its auth system do an enormous amount for you, and the tradeoff is that you have to learn *its* way of doing things rather than assembling your own. Coming from Flask — where you wire up sessions and queries yourself — the contrast was the useful part: Flask taught me what the pieces are, Django taught me what a mature framework decides on your behalf.

The recurring lesson across both is the same one: **ownership checks belong in the query, not the view.** Filtering topics by the logged-in user at the database level is the difference between a real access-control boundary and a cosmetic one.

---

## Running locally

```bash
git clone https://github.com/josephshinkle/Learning-Log
cd Learning-Log
python -m venv venv
source venv/bin/activate      # Windows: venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver
```

Visit `http://localhost:8000`.

---

Built by **Joseph Shinkle** — [LinkedIn](https://www.linkedin.com/in/josephshinkle) · [GitHub](https://github.com/josephshinkle)
