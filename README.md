# University ERP Desktop Application (AP Final Project)

## 📺 Project Demonstration
<video src="https://github.com/anikura/IIITD-ADVANCED-PROGRAMING-ERP/raw/main/AP_VEDIO.mp4" width="100%" controls>
  Your browser does not support the video tag. You can view the video directly at: 
  https://github.com/anikura/IIITD-ADVANCED-PROGRAMING-ERP/blob/main/AP_VEDIO.mp4
</video>

---

This project is a secure, role-based desktop application developed using Java Swing and MySQL, designed to manage academic sections, enrollments, and grading for a university department.

### 1. Prerequisites

| Software | Version | Purpose |
| :--- | :--- | :--- |
| **Java Development Kit (JDK)** | **21 or later** | Required to run the compiled application. |
| **MySQL Server** | **8.0 or later** | Required to host the databases. |

### 2. Database Setup (Crucial First Step)

1.  **Execute the entire provided SQL script (`schema_setup.sql`)** in MySQL Workbench. This creates the necessary tables (`users_auth`, `students`, `sections`, etc.) and inserts seed data.
2.  **Connection Details:** Ensure your `DBConnection.java` file is configured to match your local MySQL root user password.

| Setting | Auth Database | ERP Database |
| :--- | :--- | :--- |
| **URL Base** | `jdbc:mysql://localhost:3306/university_auth` | `jdbc:mysql://localhost:3306/university_erp` |
| **Username** | `root` | `root` |

### 3. Running the Application (Executable JAR)

The application is provided as a single, self-contained executable JAR (built using the Maven Shade Plugin).

#### A. Launch Command

1.  Navigate your terminal (Command Prompt/PowerShell) to the **`target`** folder of the project.
2.  Execute the following command:

    ```bash
    java -jar univ-erp-java-swing-executable.jar
    ```

#### B. Default Login Credentials

| Role | Username | Password | Notes |
| :--- | :--- | :--- | :--- |
| **Admin** | `admin1` | `password123` | Full system control. |
| **Instructor** | `inst1` | `temp123` | Assigned to all initial sections. |
| **Student** | `stu1` | `temp123` | Used for acceptance tests. |
| **Temporary** | (Any user) | `temp123` | Temporary password after an Admin forces a reset. |

***
