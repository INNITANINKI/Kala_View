
# 🎨 Kala View – Online Art Gallery

A visually dynamic and artist-centric web platform that allows for the upload, management, and display of artworks and organise workshops , exhibitions. Built with Java Full Stack technologies, this project provides a simple and effective way to create an online art gallery.

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [How to Run](#how-to-run)
- [Testing](#testing)

---

## 📖 About the Project

Kala View is an online platform for showcasing and browsing various forms of artwork. Admins can upload images and metadata, and users can explore them in a clean, categorized layout. This project helps build digital presence for artists and creates a responsive visual experience for users.

---

## 🌟 Features

- Admin image upload with title, description, and category
- Organized gallery with Thymeleaf rendering
- Static file image storage
- MySQL backend for metadata
- Simple admin UI
- Mobile responsive layout

---

## 💻 Tech Stack

| Layer        | Technology                   |
|-------------|------------------------------|
| Frontend     | Thymeleaf, HTML, CSS, Bootstrap |
| Backend      | Java, Spring Boot             |
| Database     | MySQL                         |
| Build Tool   | Maven                         |
| IDE          | VS Code / Spring Tool Suite   |
| Testing Tool | Postman                       |

---

## 📂 Project Structure

```
Kala_View/
├── src/
│   └── main/
│       ├── java/com/kala/view/     # Controllers, Services, Models
│       ├── resources/
│       │   ├── static/img/         # Uploaded artwork images
│       │   └── templates/          # Thymeleaf templates
├── pom.xml
└── application.properties
```

---

## 🗃️ Database Schema

```sql
CREATE TABLE artwork (
    id INT NOT NULL AUTO_INCREMENT,
    title VARCHAR(225) NOT NULL,
    description VARCHAR(2000) NOT NULL,
    category VARCHAR(225) NOT NULL,
    label VARCHAR(225) NOT NULL,
    price INT NOT NULL,
    likes INT NOT NULL,
    imgUrl VARCHAR(2000) NOT NULL,
    owner_id INT NOT NULL,
    PRIMARY KEY (id),
    FOREIGN KEY (owner_id) REFERENCES user(id)
);
```

---

## 🚀 How to Run

### Prerequisites
- Java 17+
- Maven
- MySQL

### Steps

1. Clone the repository:
```bash
git clone https://github.com/<your-username>/Kala_View.git
cd Kala_View
```

2. Configure `application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/kala_view_db
spring.datasource.username=root
spring.datasource.password=yourpassword
```

3. Run the application:
```bash
mvn spring-boot:run
```
