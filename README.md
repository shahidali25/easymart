EasyMart is a Django-based grocery shopping platform with user authentication, product browsing, cart management, checkout, order tracking, and Razorpay payment support

Features
Email/OTP-based account signup and login
User dashboard, address management, and password reset
Product catalog with categories and product detail pages
Session-based guest cart and authenticated cart support
Checkout with online payment or cash on delivery
Order history, order detail, and order tracking pages
Jazzmin-styled Django admin for easier management
Sample products created for local development
Tech Stack
Django 6.0.4
SQLite for development
Bootstrap, HTML, CSS, and JavaScript on the frontend
Razorpay for payment processing
Jazzmin for the admin interface
python-dotenv for environment variables
Requirements
Python 3.10 or newer
pip
A virtual environment is recommended
Setup
cd easymart
python -m venv env
env\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
Open the app at http://127.0.0.1:8000 and the admin panel at http://127.0.0.1:8000/admin.

Environment Variables
The project loads environment variables from a .env file.

Useful values include:

SECRET_KEY
DEBUG
ALLOWED_HOSTS
EMAIL_HOST_USER
EMAIL_HOST_PASSWORD
RAZORPAY_KEY_ID
RAZORPAY_KEY_SECRET
The default email backend is console-based for local development, so email credentials mainly matter when you switch to SMTP.

Main Routes
/ - landing page
/accounts/signup/ - create account
/accounts/login/ - login page
/accounts/dashboard/ - user dashboard
/accounts/address/ - saved addresses
/products/home/ - product listing
/products/product/<id>/ - product details
/products/category/ - category view
/cart/ - cart page
/cart/add/ - add item to cart
/cart/update/ - update cart quantity
/orders/checkout/ - checkout page
/orders/history/ - order history
/orders/detail/<order_id>/ - order detail page
/orders/track/<order_id>/ - order tracking
/admin/ - Django admin
Useful Commands
python manage.py makemigrations
python manage.py migrate
python manage.py test
python manage.py check
python manage.py collectstatic
Project Structure
accounts/ - authentication, profiles, and addresses
cart/ - cart logic and cart context helpers
products/ - product catalog and landing pages
orders/ - checkout, payment, and tracking
easymart/ - project settings and URL configuration
templates/ - shared HTML templates
static/ - static assets
media/ - uploaded media files
Notes
The project uses SQLite locally by default.
Sample products are created to make the storefront usable immediately after setup.
If you plan to deploy, set DEBUG=False, configure ALLOWED_HOSTS, and switch email and payment settings to production values.
accounts/urls.py - Authentication routes
products/urls.py - Product routes
cart/urls.py - Cart routes
orders/urls.py - Order routes
🐛 Troubleshooting
ModuleNotFoundError: No module named 'dotenv'
pip install python-dotenv
Port 8000 already in use
python manage.py runserver 8001
Database locked
# Delete db.sqlite3 and run migrations again
rm db.sqlite3
python manage.py migrate
Static files not loading
python manage.py collectstatic
📞 Support
For issues or improvements:

Check the logs in logs/django.log
Run python manage.py check for diagnostics
Review .env configuration
Check database migrations
📄 License
This project is provided as-is for educational and commercial use.

🎉 Status
✅ Project Complete & Working

All core features implemented
Database configured and migrated
Authentication system working
Payment integration ready
Admin panel configured
Sample data auto-generated
Production-ready with configuration
Ready for Development or Deployment!
