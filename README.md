# Java Maven Build with Jenkins

## Objective
To run a simple Java application using Maven in Jenkins — a foundational CI/CD task.

---

## 🛠 Tools Used

- **Jenkins** (Dockerized)
- **Java JDK 8**
- **Apache Maven 3.8.6**
- **Git & GitHub**

---

## Project Structure

project Folder/
├── pom.xml
└── src/
     └── main/
          └── java/
                └── HelloWorld.java

---

## Step-by-Step Process

### 1. Set up Jenkins using Docker

```bash
docker run -p 9090:8080 -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```
- Access Jenkins at: http://localhost:9090

- Unlocked Jenkins using the initial admin password from the container

- Installed suggested plugins

- Created an admin user account

### 2. Configure Maven in Jenkins

- Navigated to Manage Jenkins → Global Tool Configuration

- Added Maven 3.8.6

- Checked “Install automatically”

- Saved the configuration

### 3. Created Java Maven Project

Created a local project with the following files:
- HelloWorld.java
- pom.xml

### 4. Pushed Project to GitHub
- Initialized a Git repository

- Pushed code to GitHub Repo

### 5. Created Jenkins Freestyle Job
- Created a new Freestyle project: Java-Maven-Build1

- Selected Git in "Source Code Management"

- Added GitHub repo URL

- In Build section:

  - Chose “Invoke top-level Maven targets”

  - Goal: clean package

  - Selected Maven 3.8.6 as the Maven version

### 6. Ran the Build
- Clicked Build Now

- Build succeeded with message:
  `SUCCESS`

### Took a screenshot.

### Outcome
- Successfully integrated Git, Jenkins, Java, and Maven

- Built and packaged a simple Java app using Jenkins CI

- Learned how to configure tools and jobs in Jenkins
