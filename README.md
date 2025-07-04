text
# User Management Application

A full-stack User Management application built with **Spring Boot** (backend REST API) and **React** (frontend).  
This project demonstrates basic CRUD operations on user data with a clean and responsive UI.

---

## Features

- Create, read, update, and delete users via REST API
- React frontend for user-friendly interaction
- Uses Spring Data JPA with an H2/MySQL database (configurable)
- CORS enabled for frontend-backend communication
- Bootstrap styling for a modern UI

---

## Technologies Used

| Backend                     | Frontend            | Database         |
|-----------------------------|---------------------|------------------|
| Java 17+ with Spring Boot   | React.js            | H2 / MySQL       |
| Spring Data JPA             | Bootstrap 5         |                  |
| Jakarta Persistence (JPA)   | Fetch API for AJAX  |                  |

---

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven or Gradle
- Node.js and npm
- (Optional) MySQL database or use embedded H2

### Backend Setup

1. Clone the repository:
git clone https://github.com/yourusername/user-management-app.git
cd user-management-app/backend

text

2. Configure your database in `src/main/resources/application.properties` (default uses H2).

3. Enable CORS in your controller to allow frontend requests:
import org.springframework.web.bind.annotation.CrossOrigin;

@CrossOrigin(origins = "http://localhost:3000")
@RestController
@RequestMapping("/user")
public class UserController {
// your endpoints
}

text

4. Run the Spring Boot application:
./mvnw spring-boot:run

text
or
./gradlew bootRun

text

5. Backend will start on `http://localhost:8080`.

### Frontend Setup

1. Navigate to the frontend folder:
cd ../frontend

text

2. Install dependencies:
npm install

text

3. Start the React development server:
npm start

text

4. Frontend will start on `http://localhost:3000`.  
If port 3000 is busy, you will be prompted to run on another port.

---

## Usage

- Use the React UI to add new users and fetch the list of existing users.
- The frontend communicates with the backend REST API to perform CRUD operations.
- API endpoints are available under `/user`.

---

## Troubleshooting

- **CORS errors:** Ensure `@CrossOrigin(origins = "http://localhost:3000")` is enabled in the backend controller.
- **Port conflicts:** Make sure ports 8080 (backend) and 3000 (frontend) are free or configure different ports.
- **Database issues:** Check your database configuration in `application.properties`.
- **Failed to fetch errors:** Confirm backend is running and accessible at the expected URL.

---

## License

This project is licensed under the MIT License.

---

## Contact

For questions or suggestions, please contact [soniharshit1833@gmail.com].
