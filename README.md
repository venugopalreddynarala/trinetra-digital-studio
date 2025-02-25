# trinetra-digital-studio
Trinetra Digital Studio
Welcome to Trinetra Digital Studio, a responsive web application built with PHP, MySQL, HTML, CSS, JavaScript, and Bootstrap. This project serves as a digital photography portfolio platform featuring a user-facing gallery, live event streaming, a contact form, and an admin panel for managing content securely.
# Overview
Trinetra Digital Studio allows users to explore categorized photo galleries (Weddings, Events, Portraits), view live events via YouTube, and submit inquiries. The admin panel, accessible only to authenticated admins, enables image uploads, event management, message replies, admin user management, and analytics tracking. For security, only logged-in admins can add new admins.
# Features
# User View:
Image Gallery with category filtering and Lightbox previews.
Live event streaming via YouTube integration.
Contact form for user inquiries.
# Admin Panel:
Secure admin login and registration (only admins can add admins).
Upload, resize, and delete images.
Manage live events (add, update, delete).
Reply to contact inquiries via email.
Manage admin users (create/edit/delete).
View analytics (page views, uploads).
 .Responsive Design: Built with Bootstrap 5.3 for mobile-friendly layouts.
 . Dynamic Content: PHP and MySQL drive galleries, events, and inquiries.
# Requirements
 . Server: Apache or Nginx with PHP 8.2+ and MySQL 5.7+
 . PHP Extensions: GD (for image resizing), mail (for email replies)
 . OS: Windows, Linux, or macOS (tested on Windows with XAMPP)
 . Browser: Modern browsers (Chrome, Firefox, Edge)
 # Setup Instructions
  1. Local Development (Using XAMPP)
 .Install XAMPP:
Download and install XAMPP from apachefriends.org.
Start Apache and MySQL in the XAMPP Control Panel.
# Clone or Copy Files:
Place the project folder in C:\xampp\htdocs\trinetra\:
C:\xampp\htdocs\trinetra\
├── index.php
├── style.css
├── main.js
├── /admin
│   ├── index.php
│   ├── login.php
│   ├── logout.php
│   ├── register.php
│   ├── upload_image.php
│   ├── delete_image.php
│   ├── update_event.php
│   ├── manage_admins.php
│   ├── manage_events.php
│   ├── send_reply.php
│   ├── analytics.php
│   ├── admin.css
├── /media
├── /pages
├── /uploads
├── config.php
├── functions.php
├── submit_contact.php
├── db.sql
# Create Uploads Folder:
Create C:\xampp\htdocs\uploads\ and set permissions:
Right-click > Properties > Security > Grant "Full control" to "Users" or run XAMPP as Administrator.
# Set Up Database:
Open phpMyAdmin (http://localhost/phpmyadmin).
Create a database named trinetra_db.
Import db.sql:
CREATE DATABASE trinetra_db;
USE trinetra_db;
-- (rest of db.sql content follows)
Update config.php with MySQL credentials:
php
$db_host = "localhost";
$db_user = "root"; // Your MySQL username
$db_pass = "";     // Your MySQL password
$db_name = "trinetra_db";
# Enable GD Library:
Open C:\xampp\php\php.ini.
Uncomment extension=gd.
Restart Apache in XAMPP.
# Test Locally:
Access http://localhost/trinetra/index.php (user page).
Admin: http://localhost/trinetra/admin/index.php after logging in.
# Troubleshooting
"Not Found" Errors (404):
Verify file paths (e.g., /uploads/ in config.php, upload_image.php).
Ensure files are in htdocs/ or correct subfolder.
Contact Form Not Saving:
Use debug versions of submit_contact.php and functions.php to check output:
Submit a message and verify contacts table via phpMyAdmin.
Images Not Showing:
Check uploads/ permissions (777), file existence, and file_path in the images table.
Admin Registration Access:
Ensure only logged-in admins can access admin/register.php by verifying session in register.php.
# Contributing
Fork this repository, make changes, and submit pull requests.
Report issues or suggest features by opening an issue on GitHub or contacting via email.
# License
This project is for personal use and learning purposes. Modify and distribute as needed, but consider the open-source nature and credit the original author.

