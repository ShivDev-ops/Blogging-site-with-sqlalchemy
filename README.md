# Blogging Site With SQLAlchemy

This is a Flask-based blogging project that uses SQLAlchemy for database access and Flask-Mail for contact form email delivery.

## What the app does

- Shows blog posts on the home page.
- Opens individual post pages from a slug-based route.
- Includes About and Contact pages.
- Provides an admin dashboard for logging in and managing posts.
- Supports creating and editing posts.
- Supports file uploads for post images.
- Sends contact form submissions by email.

## Tech Stack

- Python
- Flask
- Flask-SQLAlchemy
- Flask-Mail
- Jinja2 templates
- MySQL
- Bootstrap and jQuery for the front end

## Project Structure

- `main.py` - Flask application, routes, database models, and mail setup.
- `config.json` - Local configuration and secrets used by the app.
- `templates/` - Jinja templates for pages like home, about, contact, login, dashboard, edit, and post views.
- `static/` - CSS, JavaScript, images, Bootstrap assets, and Font Awesome assets.

## Main Routes

- `/` - Home page with the latest blog posts.
- `/about` - About page.
- `/post/<slug>` - Individual post page.
- `/contact` - Contact form.
- `/dashboard` - Admin login and dashboard.
- `/edit/<sno>` - Create or edit a post.
- `/uploader` - Upload a file for a post.

## Setup

1. Create and activate a Python virtual environment.
2. Install the required packages used by the project.
3. Make sure MySQL is running and the database in `config.json` exists.
4. Update `config.json` with your local database URI, Gmail credentials, upload path, and admin credentials.
5. Run the app:

```bash
python main.py
```

## Configuration Notes

- `config.json` is hidden and ignored by git because it contains local credentials and environment-specific values.
- The app reads `config.json` at startup, so keep the file in the project root.
- `app.run(debug=True)` is enabled for development.

## Notes

- This project appears to be built from a Clean Blog style template.
- Some paths in `config.json` are machine-specific and may need to be updated before running the app elsewhere.

hello