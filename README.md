📸 Photo Studio Management System

This is a customized Photo Studio Management System built on LAMP stack.
It helps manage clients, bookings, payments, and notifications. The system allows studio clients to book sessions online, get a preview of their photos, receive their photos and have their favorites bookmarked.

🚀 Project Set Up and Installation
1. Clone the Project
git clone https://github.com/mutembeievans/da-perfect-studios.git

2. Move into the project folder
cd da-perfect-studios

3. Configure Apache and PHP

Ensure Apache and PHP are installed and running.

Copy the project folder to your Apache web root directory (e.g., /var/www/html/).

sudo cp -r da-perfect-studios /var/www/html/

4. Set File Permissions
sudo chown -R www-data:www-data /var/www/html/da-perfect-studios
sudo chmod -R 755 /var/www/html/da-perfect-studios

5. Import the Database

Create a new MySQL database:

CREATE DATABASE photo_studio;


Import the provided SQL file:

mysql -u root -p photo_studio < database/photo_studio.sql

6. Configure Database Connection

Open config.php.

Update with your database credentials:

<?php
$host = "localhost";
$user = "root";
$password = "";
$dbname = "photo_studio";
?>

7. Access the Application

Start Apache & MySQL:

sudo service apache2 start
sudo service mysql start


Open in your browser:

http://127.0.0.1//da-perfect-studios
