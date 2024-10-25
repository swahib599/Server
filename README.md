# Cocktail Application Backend

## Overview
A Flask-based RESTful API that serves as the backend for the Cocktail Application. It provides endpoints for user authentication, cocktail management, and review systems.

## Features
•⁠  ⁠RESTful API architecture
•⁠  ⁠JWT-based authentication
•⁠  ⁠CRUD operations for cocktails and reviews
•⁠  ⁠User management system
•⁠  ⁠Search functionality
•⁠  ⁠Database management with SQLAlchemy

## Technology Stack
•⁠  ⁠Python 3.x
•⁠  ⁠Flask
•⁠  ⁠SQLAlchemy ORM
•⁠  ⁠JWT Extended
•⁠  ⁠SQLite database (configurable for other databases)
•⁠  ⁠Flask-CORS for cross-origin support

## Project Structure

├── app.py
├── config.py
├── models.py
├── seed.py
└── requirements.txt


## Database Schema
•⁠  ⁠Users
•⁠  ⁠Cocktails
•⁠  ⁠Ingredients
•⁠  ⁠CocktailIngredients (junction table)
•⁠  ⁠Reviews

## API Endpoints

### Authentication
•⁠  ⁠POST ⁠ /api/register ⁠: User registration
•⁠  ⁠POST ⁠ /api/login ⁠: User login
•⁠  ⁠POST ⁠ /api/verify-token ⁠: Token verification

### Cocktails
•⁠  ⁠GET ⁠ /api/cocktails ⁠: List all cocktails
•⁠  ⁠POST ⁠ /api/cocktails ⁠: Create new cocktail
•⁠  ⁠GET ⁠ /api/cocktails/<id> ⁠: Get specific cocktail
•⁠  ⁠PUT ⁠ /api/cocktails/<id> ⁠: Update cocktail
•⁠  ⁠DELETE ⁠ /api/cocktails/<id> ⁠: Delete cocktail

### Reviews
•⁠  ⁠POST ⁠ /api/cocktails/<id>/reviews ⁠: Add review
•⁠  ⁠PUT ⁠ /api/reviews/<id> ⁠: Update review
•⁠  ⁠DELETE ⁠ /api/reviews/<id> ⁠: Delete review

### Search
•⁠  ⁠GET ⁠ /api/cocktails/search ⁠: Search cocktails
•⁠  ⁠GET ⁠ /api/ingredients ⁠: List all ingredients

## Setup and Installation
1.⁠ ⁠Clone the repository

2.⁠ ⁠Create and activate virtual environment:
   ⁠ bash
   python -m venv venv
   source venv/bin/activate  # Unix
   venv\Scripts\activate     # Windows
    ⁠

3.⁠ ⁠Install dependencies:
   ⁠ bash
   pip install -r requirements.txt
    ⁠

4.⁠ ⁠Configure environment variables:
   - Create ⁠ .env ⁠ file based on config.py
   - Set necessary environment variables

5.⁠ ⁠Initialize database:
   ⁠ bash
   python seed.py
    ⁠

6.⁠ ⁠Run the application:
   ⁠ bash
   python app.py
    ⁠

## Environment Variables

FLASK_APP=app.py
FLASK_ENV=development
SECRET_KEY=your-secret-key
JWT_SECRET_KEY=your-jwt-secret
DATABASE_URL=sqlite:///cocktails.db


## Database Management
•⁠  ⁠SQLAlchemy ORM for database operations
•⁠  ⁠Migration support
•⁠  ⁠Seeding script for initial data
•⁠  ⁠SQLite by default, configurable for PostgreSQL/MySQL

## Error Handling
•⁠  ⁠Comprehensive error handling system
•⁠  ⁠Structured error responses
•⁠  ⁠Logging system for debugging

## Security Features
•⁠  ⁠Password hashing
•⁠  ⁠JWT token authentication
•⁠  ⁠CORS protection
•⁠  ⁠Rate limiting

## Logging
•⁠  ⁠Configured logging for debugging
•⁠  ⁠Error tracking
•⁠  ⁠Activity monitoring

## Testing
⁠ bash
python -m pytest tests/
 ⁠

## Deployment
1.⁠ ⁠Configure production environment variables
2.⁠ ⁠Set up production database
3.⁠ ⁠Configure CORS for production domain
4.⁠ ⁠Set up logging
5.⁠ ⁠Configure web server (Gunicorn recommended)

## Contributing
1.⁠ ⁠Fork the repository
2.⁠ ⁠Create your feature branch
3.⁠ ⁠Commit your changes
4.⁠ ⁠Push to the branch
5.⁠ ⁠Create a new Pull Request

