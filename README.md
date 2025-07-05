# 🧑‍💻 Fullstack User Management Application

This is a fullstack CRUD application for managing users. It includes a frontend built with **React + Nextjs + Tailwind CSS**, a backend RESTful API built with **Spring Boot (Java)**, and a **PostgreSQL** database.

---

## 📂 Project Structure

```
fullstackproject1/
├── frontend/    # React application with Tailwind CSS
├── api/         # Spring Boot backend (Java 21)
├── db/          # MySQL schema or docker config
```

---

## ✅ Features

- Create new users  
- View a list of all users  
- Delete existing users  
- Update user information (coming soon)  
- Fully functional API integration  
- Modular, production-ready project setup

---

## 🚀 Getting Started

### 1. Backend (API - Spring Boot)

Make sure you have Java 21 and Maven installed.

```bash
cd api
./mvnw spring-boot:run
```

> The backend server runs on `http://localhost:3232/api`.

Update your `application.properties` file with the correct MySQL connection settings.

---

### 2. Frontend (React + Tailwind)

Make sure you have Node.js installed.

```bash
cd frontend
npm install
npm run dev
```

> The frontend runs on `http://localhost:3000` by default and communicates with the backend.



### Refer to :
https://github.com/miladrostami-devjava/fullstack-project-user-management-frontend
---


### 3. Database (MySQL)

You need to have a MySQL database running. Either:

- **Option A: Manual Setup**

  - Manually create a MySQL database (e.g. `fullstack_db`)
  - Run the schema and initial data scripts located in the `/db` folder using a MySQL client (such as MySQL Workbench or CLI)

- **Option B: Docker Setup**

  - Run MySQL using Docker with a mounted volume for schema initialization.
  - Example Docker command:
    ```bash
    docker run --name mysql-db -e MYSQL_ROOT_PASSWORD=root -e MYSQL_DATABASE=fullstack_db -p 3306:3306 -v /path/to/your/fullstackproject1/db:/docker-entrypoint-initdb.d mysql:8
    ```

- ✅ **Update database connection settings** in the file: `api/src/main/resources/application.properties` Example:

  ```properties
  spring.datasource.url=jdbc:mysql://localhost:3306/fullstack_db
  spring.datasource.username=root
  spring.datasource.password=your_password
  spring.jpa.hibernate.ddl-auto=update
  spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
  ```

---


---

## 🧠 Learning Goals

This project is intended for practicing full-stack development:

- React state management
- TailwindCSS styling
- REST API design in Spring Boot
- CRUD operations with database
- Clean folder structure
- Frontend-backend integration

---

## ⚙️ Technologies Used

### Frontend:

- React
-Nextjs
- TypeScript
- Tailwind CSS
- Axios

### Backend:

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- MySQL Driver
- Maven

---

## 🛡️ API Endpoints (Sample)

| Method | Endpoint         | Description         |
|--------|------------------|---------------------|
| GET    | `/api/users`     | Get all users       |
| POST   | `/api/users`     | Create a new user   |
| DELETE | `/api/users/{id}`| Delete a user       |
| PUT    | `/api/users/{id}`| Update a user       |

---

## 👨‍💻 Developer

- **Name**: [milad rostami]
- **Email**: [miladrostami24@gmail.com]
- **GitHub**: [github.com/miladrostami-devjava](https://github.com/miladrostami-devjava)

---

## 📌 License

This project is open-source and available under the [MIT License](LICENSE).