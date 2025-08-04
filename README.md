# Issue Tracker ORM System

A simple Issue/Bug tracking system developed with **Spring Boot**, **Spring Data JPA**, and **PostgreSQL**. This application tracks bugs under projects, assigns them to users, and allows various queries through REST APIs.

---

## 🔧 Tech Stack

- **Backend Framework**: Spring Boot  
- **ORM Tool**: Spring Data JPA  
- **Database**: PostgreSQL  
- **Build Tool**: Maven  
- **Java Version**: 17+  
- **Port**: 8085

---

## 📂 Folder Structure

```
issue-tracker-orm/
├── src/
│   └── main/
│       └── java/
│           └── com/example/issueTrackerOrm/
│               ├── controller/
│               ├── domain/
│               ├── repository/
│               ├── service/
│               └── IssueTrackerOrmApplication.java
├── resources/
│   └── application.properties
└── pom.xml
```

---

## ⚙️ Configuration (`application.properties`)

- Database connection (PostgreSQL)
- Hibernate dialect and DDL auto-update
- Server port set to 8085
- SQL logging enabled

---

## 🧠 Features

- Add, view, and manage **bugs**, **projects**, and **users**
- Assign bugs to users under specific projects
- Query bugs by:
  - Status
  - Assigned user
  - Project ID
  - Unresolved status for a specific user
  - Count of bugs per project

---

## 🧪 API Endpoints (BugController)

| Endpoint                             | Method | Description                              |
|--------------------------------------|--------|------------------------------------------|
| `/api/bugs`                          | GET    | Fetch all bugs                           |
| `/api/bugs/status/{status}`         | GET    | Fetch bugs by status                     |
| `/api/bugs/project/{project_id}`    | GET    | Fetch bugs by project ID                 |
| `/api/bugs/assigned-to/{userid}`    | GET    | Fetch bugs assigned to a specific user   |
| `/api/bugs/unresolved/user/{userid}`| GET    | Get unresolved bugs for a user           |
| `/api/bugs/count/project/{projectId}`| GET   | Count bugs for a given project ID        |

---

## 👨‍💻 Developer

- **Lokeshwaran M**

---

## 🚀 Getting Started

1. **Clone the project**
   ```bash
   git clone https://github.com/your-username/issue-tracker-orm.git
   cd issue-tracker-orm
   ```

2. **Configure the database**

   Update your PostgreSQL credentials in `application.properties`.

3. **Run the application**
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Test the APIs**

   Use tools like Postman to hit endpoints at `http://localhost:8085/api/bugs`

---

## 📄 License

This project is for educational and demonstration purposes only.
