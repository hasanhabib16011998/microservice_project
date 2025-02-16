docker exec -it mysql-container mysql -u root -p

-- Create the database
CREATE DATABASE auth;

-- Use the database
USE auth;

-- Create the users table
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL
);


INSERT INTO users (email, password) VALUES
('user1@example.com', 'password123'),
('user2@example.com', 'securepass'),
('user3@example.com', 'mysecretpass'),
('user4@example.com', 'pass1234'),
('user5@example.com', 'adminpass');