# Hello-my-mevan
**TASK 8:  Run a Simple Java Maven Build Job in Jenkins**
 
**🛠 Objective**

 Learn how to use Jenkins to build a simple Java application using Maven — your first step into CI/CD.
 
**Tools Required (All Free):**
 Jenkins (installed locally or via Docker)
 Java JDK 8 or 11
 Maven
 Git (optional — can run from local folder)
 
**📂 Deliverables:**
 A basic Java HelloWorld app (with pom.xml)
 Jenkins Freestyle job configured to build it
 Screenshot of successful build console output
 
**Jenkins Freestyle** is one of the basic types of jobs (or projects) you can create in Jenkins, a popular open-source automation server often used for continuous integration/continuous delivery (CI/CD).

A **Freestyle project** provides a simple, flexible way to configure a Jenkins build process.

### 🔧 Key Features of Jenkins Freestyle:
- **GUI-based Configuration**: You set it up using the web UI, without writing code.
- **Build Triggers**: You can configure the job to run on a schedule, when code is pushed to a repository, or after another job completes.
- **Source Code Management (SCM)**: Supports Git, SVN, and more.
- **Build Steps**: You can define steps like shell scripts, batch commands, or calling build tools (like Maven or Gradle).
- **Post-build Actions**: Email notifications, archiving artifacts, publishing test reports, and more.

### 🧱 Basic Flow:
1. **Pull code** from a repository.
2. **Run some commands** (build, test, etc.).
3. **Publish results** or trigger further jobs.

### ✅ When to Use Freestyle Projects:
- For **simple build pipelines**.
- When you’re new to Jenkins and want a quick setup.
- For **legacy projects** that don't require complex logic.

---

> 🔁 If you're working on more complex pipelines (branching logic, parallel steps, etc.), consider using **Jenkins Pipeline** instead — it offers more control via code (`Jenkinsfile`).





**🐱 What is Apache Tomcat?**
Tomcat is an open-source Java Servlet Container developed by the Apache Software Foundation. It's used to run Java web applications, specifically ones that follow the Java EE (Jakarta EE) specifications like:

Servlets

JSP (JavaServer Pages)

WebSockets

It’s not a full-blown Java EE app server like WildFly or GlassFish — it’s a lightweight, fast, and widely-used option for serving Java web apps.






.

**🚀 What Can You Do with Tomcat?**
Deploy WAR files (Web Application Archives)

Host dynamic web content using Java

Integrate with Jenkins for automated deployments

Run on local machines or cloud servers (e.g., AWS EC2, DigitalOcean)




**📦 Basic Tomcat Folder Structure:**
When you unzip/install Tomcat, here are key folders:

/bin – startup/shutdown scripts

/webapps – drop your WAR files here to deploy

/conf – configuration files (server.xml, web.xml)

/logs – server logs




**🔗 Jenkins + Tomcat**
Jenkins can automatically deploy Java apps to Tomcat. Here's how:

Build your project in Jenkins.

Package it as a .war file.

Use a plugin (like Deploy to Container Plugin) or custom shell scripts to push it to the Tomcat server.

Great question! The `pom.xml` file is the **core config file used by Maven**, which is a popular **build automation and dependency management tool** for Java projects.

---

### 📄 What is `pom.xml`?
**POM** stands for **Project Object Model** — it's an XML file that describes your project and defines how it's built, including:

- Project metadata (name, version, description, etc.)
- Dependencies (other libraries your code needs)
- Build plugins
- Repository info
- Build lifecycle steps (like compile, test, package, deploy)

---

### 🧱 Example `pom.xml` (Simple)
```xml
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 
                             http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.example</groupId>
    <artifactId>myapp</artifactId>
    <version>1.0.0</version>
    <packaging>war</packaging>

    <dependencies>
        <dependency>
            <groupId>javax.servlet</groupId>
            <artifactId>javax.servlet-api</artifactId>
            <version>4.0.1</version>
            <scope>provided</scope>
        </dependency>
    </dependencies>

    <build>
        <plugins>
            <!-- Plugin to compile Java code, package WAR, etc. -->
        </plugins>
    </build>
</project>
```

---

### 🛠 What Can You Do with `pom.xml`?
- Add **libraries** like Spring, Hibernate, etc. (Maven downloads them for you)
- Compile your Java code
- Run tests
- Create a `.jar` or `.war` file
- Deploy to a remote server or repository
- Integrate with Jenkins for CI/CD

---

### 🔗 Jenkins + Maven + Tomcat Flow:
1. Jenkins reads your project (`pom.xml`)
2. Uses Maven to **build** it
3. Packages your app into a `.war`
4. Deploys the `.war` to **Tomcat**

---![Screenshot (83)](https://github.com/user-attachments/assets/55054e73-9b2f-4d7f-9036-e49750de074c)

![Screenshot (84)](https://github.com/user-attachments/assets/1f9fe5c1-f3df-4338-92c6-46682e4f8ddf)

![Screenshot (85)](https://github.com/user-attachments/assets/0dcc9bcc-ab39-4d9a-a25c-e1d87a4d4c07)
![Screenshot (86)](https://github.com/user-attachments/assets/e2600cbf-a5ef-458c-9437-c035dd6530d7)

![Screenshot (87)](https://github.com/user-attachments/assets/78f6fe47-f106-489c-8325-e1a126693766)

![Screenshot (88)](https://github.com/user-attachments/assets/f8d2a578-613b-4836-bd7d-70ef3494234c)
