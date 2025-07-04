# User Management Application

---

This full-stack User Management application provides a robust solution for managing user data, featuring a **Spring Boot** (backend REST API) and **React** (frontend) architecture. It's designed to showcase fundamental CRUD (Create, Read, Update, Delete) operations with a focus on a clean, responsive, and user-friendly interface.

---

## ✨ Features

* **Complete CRUD Operations:** Seamlessly create, read, update, and delete user records via a powerful REST API.
* **Intuitive React Frontend:** Interact with the application through a modern and responsive user interface built with React.js.
* **Flexible Database Support:** Utilizes Spring Data JPA with configurable support for H2 (default embedded) or MySQL databases.
* **Seamless Communication:** CORS (Cross-Origin Resource Sharing) is pre-configured to ensure smooth communication between the frontend and backend.
* **Modern UI:** Enhanced with Bootstrap 5 for a consistent and appealing design.

---

## 🛠️ Technologies Used

| Category   | Backend                         | Frontend              | Database   |
| :--------- | :------------------------------ | :-------------------- | :--------- |
| **Stack** | Java 17+ with Spring Boot       | React.js              | H2 / MySQL |
| **Tools** | Spring Data JPA                 | Bootstrap 5           |            |
|            | Jakarta Persistence (JPA)       | Fetch API for AJAX    |            |

---

## 🚀 Getting Started

To get this application up and running, follow these simple steps:

### Prerequisites

Ensure you have the following installed on your system:

* **Java Development Kit (JDK):** Version 17 or higher
* **Build Tool:** Maven or Gradle
* **Node.js & npm:** For managing frontend dependencies
* **(Optional) MySQL Database:** If you prefer using MySQL over the embedded H2 database.

### Backend Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/yourusername/user-management-app.git](https://github.com/yourusername/user-management-app.git)
    cd user-management-app/backend
    ```

2.  **Configure Database:**
    Open `src/main/resources/application.properties` to configure your database settings. By default, it's set up to use H2.

3.  **Enable CORS:**
    Ensure CORS is enabled in your `UserController` to allow frontend requests. This is typically done by adding the `@CrossOrigin` annotation:

    ```java
    import org.springframework.web.bind.annotation.CrossOrigin;
    import org.springframework.web.bind.annotation.RestController;
    import org.springframework.web.bind.annotation.RequestMapping;

    @CrossOrigin(origins = "http://localhost:3000")
    @RestController
    @RequestMapping("/user")
    public class UserController {
        // your endpoints
    }
    ```

4.  **Run the Backend Application:**

    * **Using Maven:**
        ```bash
        ./mvnw spring-boot:run
        ```
    * **Using Gradle:**
        ```bash
        ./gradlew bootRun
        ```
    The backend API will be accessible at `http://localhost:8080`.

### Frontend Setup

1.  **Navigate to Frontend Directory:**
    ```bash
    cd ../frontend
    ```

2.  **Install Dependencies:**
    ```bash
    npm install
    ```

3.  **Start React Development Server:**
    ```bash
    npm start
    ```
    The frontend application will typically start on `http://localhost:3000`. If this port is in use, you'll be prompted to use an alternative port.

---

## 💻 Usage

Once both the backend and frontend servers are running, you can:

* Access the React UI in your web browser (usually at `http://localhost:3000`).
* Utilize the intuitive interface to **add new users** and **view the list of existing users**.
* The frontend seamlessly communicates with the backend REST API, whose endpoints are available under `/user`, to perform all CRUD operations.

---

## 🛑 Troubleshooting

Encountering issues? Here are some common solutions:

* **CORS Errors:** Verify that `@CrossOrigin(origins = "http://localhost:3000")` is correctly applied to your backend controller.
* **Port Conflicts:** Confirm that ports `8080` (backend) and `3000` (frontend) are available. If not, configure different ports in your respective application settings.
* **Database Connection Issues:** Double-check your database configuration in `application.properties`.
* **"Failed to fetch" Errors:** Ensure your backend Spring Boot application is running and accessible at the expected URL (`http://localhost:8080`).

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 📧 Contact

For any questions, feedback, or suggestions, feel free to reach out:

soniharshit1833@gmail.com
