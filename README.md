# Django Book App

## Overview

This Django-based book app allows users to:

- Get book recommendations.
- Search for books and receive direct URLs to Amazon and Flipkart.
- View Goodreads reviews of books.
- Add books to their favorites.
- Track their search history.

## Features

1. **Book Recommendations**: Provides book recommendations by using Google api.
2. **Search Functionality**:
   - Users can search for a book.
   - The app scrapes Amazon and Flipkart for book URLs.
   - Goodreads reviews are fetched and displayed.
3. **Favorites Page**: Users can add and manage their favorite books.
4. **Search History**: The app keeps a record of the user's search history.

## Technologies Used

- **Django**: Web framework for the backend.
- **Beautiful Soup**: Used for web scraping to fetch book data from Amazon, Flipkart, and Goodreads.
- **SQLite**: Default database used by Django.

## Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/yourusername/django-book-app.git
   cd django-book-app
   ```

2. **Set up a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Apply Migrations:**

   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

5. **Run the development server:**

   ```bash
   python manage.py runserver
   ```

6. **Access the app at <http://127.0.0.1:8000/>**

## Usage

- Search for Books: Use the search bar to find books by title or author.
- View Details: The app will show Amazon and Flipkart URLs, along with Goodreads reviews.
- Add to Favorites: Click on a book to add it to your favorites list.
- View Search History: Access your search history to revisit previous searches.

## Troubleshooting

### SQL Migrations

If you encounter issues with migrations, try the following:

- Fake migrations:

   ```bash
   python manage.py migrate --fake <app_name> <migration_number>
   ```

- Reset migrations: Delete migration files and the database, then reapply migrations:

   ```bash
   find . -path "*/migrations/*.py" -not -name "__init__.py" -delete
   rm db.sqlite3
   python manage.py makemigrations
   python manage.py migrate
   ```

## Contributing

- If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.
