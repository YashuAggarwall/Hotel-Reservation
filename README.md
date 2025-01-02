# Hotel-Reservation
The Hotel Reservation System is a Java-based application using JDBC to manage bookings, customer data, and room availability. It streamlines the reservation process with features like check-in/check-out, room upgrades, and payment tracking. Secure database integration ensures data accuracy and enhances the overall user experience.

## Features
- **Reserve a Room**: Allows users to reserve a room by entering guest name, room number, and contact number.
- **View Reservations**: Displays all reservations made, including reservation ID, guest name, room number, contact number, and reservation date.
- **Get Room Number**: Allows users to view the room number associated with a particular reservation ID and guest name.
- **Update Reservations**: Allows users to update details of an existing reservation (guest name, room number, contact number).
- **Delete Reservations**: Allows users to delete an existing reservation by reservation ID.
- **Exit**: Gracefully exits the system with a countdown.

## Prerequisites
- **Java**: Make sure you have Java installed (JDK 8 or higher).
- **MySQL**: You will need a running MySQL database server.
- **JDBC Driver**: You need to have the MySQL JDBC driver in your classpath.

## Database Setup
Before running the system, you need to set up a MySQL database and create a table for storing reservations. Here is an example SQL schema:

```sql
CREATE DATABASE hotel_db;

USE hotel_db;

CREATE TABLE reservations (
    reservation_id INT AUTO_INCREMENT PRIMARY KEY,
    guest_name VARCHAR(100),
    room_number INT,
    contact_number VARCHAR(20),
    reservation_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
