# Movie Watchlist Application

A simple web application to manage a watchlist of movies. Built using Java, Spring Boot, Spring MVC, PostgreSQL, HTML & CSS, and Thymeleaf.

## Features

- Add movies to the watchlist
- Update movie details
- Delete movies from the watchlist
- View all movies in the watchlist

## Technologies Used

- **Backend:** Java, Spring Boot, Spring MVC
- **Database:** PostgreSQL
- **Frontend:** HTML, CSS, Thymeleaf
- **Build Tool:** Maven

## Getting Started

### Prerequisites

- Java 11 or higher
- Maven 3.6.3 or higher
- PostgreSQL 12 or higher
- IDE Intellij IDEA or any other as well
- Note: Spring initializr is used for creation of project becasue Intellij is not providing Spring in Community version

### Installation

1. **Clone the repository:**

sh
git clone https://github.com/HyperVarun/Project.git
cd master/watchlistApplication

2. **Set up the PostgreSQL database:**

Create a database named `watchlist_Application` and a user with access to it.
sql
CREATE DATABASE watchlist_Application;
CREATE USER watchlist_user WITH ENCRYPTED PASSWORD 'yourpassword'; (Optional)
GRANT ALL PRIVILEGES ON DATABASE movie_watchlist TO watchlist_user;

4. **Configure the application properties:**

Update the `src/main/resources/application.properties` file with your PostgreSQL configuration: appkication properties
spring.datasource.url=jdbc:postgresql://localhost:5432/DatatBase_Name
spring.datasource.username={Check your user_name}
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update

4. **Build and run the application:**
    sh
    mvn clean install
    mvn spring-boot:run
    
5. **Access the application:**

Open your browser and navigate to `http://localhost:8080`.

## Project Structure

In this project I have created serveral package like Controller, Model, Entity, Service and Configuration in these packages are files you can check in the project.

## Endpoints

- **GET /watchlist:** View all movies in the watchlist
- **GET /watchlistItemForm:** Form to add a new movie
- **GET /watchlistItemForm?id={id}:** Form to update an existing movie
- **POST /watchlistItemForm:** Submit the form to add/update a movie
- **DELETE /delete?id={id}:** Delete a movie by its ID
