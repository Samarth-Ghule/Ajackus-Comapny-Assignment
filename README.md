# Digital Library Book Management System

## Overview
The **Digital Library Book Management System** is a Spring Boot-based REST API designed to efficiently manage books in a digital library. 
It provides functionalities such as adding, updating, retrieving, deleting books, and maintaining their availability status.

## Features
- Add new books to the system.
- Update book details.
- Retrieve book information using various filters.
- Delete books from the library.
- Check book availability status.
- **Exit API** to safely terminate the application.

## Technologies Used
- **Backend**: Spring Boot, Hibernate, MySQL
- **API Testing**: Postman

## Setup Instructions
1. **Clone the Repository**:
   ```sh
   git clone https://github.com/your-username/DigitalLibraryBookManagementSystem.git
   ```
2. **Navigate to the Project Directory**:
   ```sh
   cd DigitalLibraryBookManagementSystem
   ```
3. **Configure Database**:
   - Update `application.properties` with your MySQL database credentials.
4. **Build and Run the Application**:
   ```sh
   mvn spring-boot:run
   ```
5. **Access APIs via Postman or Browser**:
   - Example endpoint: `http://localhost:8080/book/viewAll`

## API Endpoints
### 1. Add a Book
   - **URL**: `/book/addBook`
   - **Method**: `POST`
   - **Request Body**:
     ```json
     {
       "title": "Spring Boot Guide",
       "author": "John Doe",
       "genre": "Technology",
       "availabilityStatus": "Available"
     }
     ```

### 2. Get All Books
   - **URL**: `/book/viewAll`
   - **Method**: `GET`

### 3. Get a Book by ID
   - **URL**: `/book/getById/{id}`
   - **Method**: `GET`

### 4. Update a Book
   - **URL**: `/book/updateBook/{id}`
   - **Method**: `PUT`
   - **Request Body** (Example):
     ```json
     {
       "title": "Updated Title",
       "author": "Jane Doe",
       "genre": "Science",
       "availabilityStatus": "Checked Out"
     }
     ```

### 5. Delete a Book
   - **URL**: `/book/deleteBook/{id}`
   - **Method**: `DELETE`

### 6. Exit API
   - **URL**: `/book/exit`
   - **Method**: `POST`
   - **Description**: Safely terminates the application.


