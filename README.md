# Basic-CRUD
This project implements basic CRUD operation and Login, Logout as for admin


## STEPS:

# FIRST NEED TO SETUP YOUR LOCAL DATABASE AND CONFIGURE THE USERNAME PASSWORD TO BACKEND .evn FILE

After database setup create table with the below query and add one admin data for login

# QEURY-1

CREATE TABLE `user_details` (
  `emp_id` int NOT NULL AUTO_INCREMENT,
  `name` VARCHAR(255) DEFAULT NULL,
  `gender` VARCHAR(255) DEFAULT NULL,
  `phone_no` VARCHAR(255) DEFAULT NULL,
  `email` VARCHAR(255) DEFAULT NULL,
  `password` VARCHAR(255) DEFAULT NULL,
  `is_admin` tinyint DEFAULT '0',
  `is_active` tinyint DEFAULT '0',
  PRIMARY KEY (`emp_id`),
  UNIQUE KEY `unique_phone_no` (`phone_no`) 
);
commit;


# QEURY-2

INSERT INTO `user_details` (`name`, `gender`, `phone_no`, `email`, `password`, `is_admin`, `is_active`)
VALUES ('Admin', 'Male', '9999999999', 'admin@gmail.com', '$2b$10$DvvM5IUaftvAp.9dET4XaOZC9uS4hjnoV9MIFKx71I91DtJ/Y4BeK', 1, 1);
commit;


after the database setup and successful running of above query you need to write the command "npm -install --force" to download node_modules and then "npm start" to start the application.

# NOTE - THE ABOVE TWO COMMANDS ARE SAME FOR THE BACKEND AND FRONTEND DIRECTORY


