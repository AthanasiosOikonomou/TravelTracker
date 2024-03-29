# TravelTracker

## Overview
This project allows users to interact with a world map using a web application. The application is built with Express, EJS, and interacts with a PostgreSQL database using the pg library. Users can input a country in a text box, and if the country exists and is spelled correctly, the color of the corresponding area on the world map changes. The application also provides error messages for incorrect spellings, non-existent countries, and attempts to add a country already visited.

## Sample Video

https://github.com/AthanasiosOikonomou/TravelTracker/assets/87909481/0e6c9286-1476-4947-8fcd-8648f1fe45ec

## Prerequisites

1) Node.js: Download and Install Node.js (https://nodejs.org/)
2) pgAdmin: Download and Install pgAdmin (https://sbp.enterprisedb.com/getfile.jsp?fileid=1258649)

## Installation

1) Clone the repository: git clone https://github.com/your-username/TravelTracker.git
2) Navigate to the project directory: cd TravelTracker.
3) Install dependencies: npm i
4) Create a PostgreSQL database using pgAdmin with the following details:
  i) Database Name: world
  ii) Tables: Use the provided SQL script to create the necessary tables (countries and visited_countries).

## Usage

nodemon index.js

## Database Setup

Ensure that you have a PostgreSQL database named world with the required tables (countries and visited_countries). You can use pgAdmin to manage your database.

1) The table countries should have this data: [countries.csv](https://github.com/AthanasiosOikonomou/TravelTracker/files/13854991/countries.csv)
2) The table visited_countries should be empty with columns id, country_code.

## Functionalility

1) checkVisisted(): Retrieves the list of visited countries from the database.
2) GET /: Renders the main page with the world map, allowing users to visualize visited countries.
3) POST /add: Handles user input, checks if the country exists, and updates the database with the visited country. Provides error messages for invalid inputs or previously visited countries.

## Database Connection

The application connects to a PostgreSQL database using the following credentials:

1) Host: localhost
2) Port: 5432
3) User: postgres
4) Password: (Your Password)
5) Database: world

## Update to version 1.01

1) Run these queries: [queries.txt](https://github.com/AthanasiosOikonomou/TravelTracker/files/13894090/queries.txt)
2) index.js and index.ejs got updated.
3) Added 1 more file: new.ejs

## Thanks

I would like to thank Dr. Angela Yu and her course 'The Complete 2023 Web Development Bootcamp' for this project.
