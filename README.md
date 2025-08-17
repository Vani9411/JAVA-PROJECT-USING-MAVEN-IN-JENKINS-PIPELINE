🚀 Build & Deploy Java Application Using Maven in Jenkins Pipeline

This project was created by me to demonstrate how to build and deploy a Java application using Maven in a Jenkins pipeline (CI/CD).


---

📌 Objective

The goal of this project is to:

Automate the Java build lifecycle using Maven.

Generate artifacts (.jar file) from source code.

Automatically deploy the application after a successful build.

Showcase a complete CI/CD pipeline with Jenkins.



---

🛠 Tools & Technologies Used

Jenkins – CI/CD automation server

Maven – Java build and dependency management tool

Java (JDK 11/17) – Application programming language

GitHub – Source code repository

Pipeline (Jenkinsfile) – Pipeline as Code

Tomcat / Docker / AWS EC2 – Deployment options



---

📂 Detailed Workflow

🔹 Step 1: Source Code Management

Application source code is stored in GitHub.

Jenkins is connected to GitHub via Webhooks for automatic build triggers.


🔹 Step 2: Jenkins Setup

Jenkins installed with required plugins (Git, Maven, Pipeline, Deploy to Container).

Configured Maven and JDK under Jenkins Global Tool Configuration.


🔹 Step 3: Build Process

1. Checkout Stage → Fetch source code from GitHub.


2. Build Stage → Compile, test, and package using Maven.


3. Artifact Stage → Store the .jar file in the target/ directory.


4. Archive Stage → Save the artifact inside Jenkins for future deployments.



🔹 Step 4: Deployment Process

After the artifact is built, it is automatically deployed:

Option 1: Deploy to Tomcat Server

Jenkins copies the generated .war or .jar file to Apache Tomcat.

The application becomes available on http://<server-ip>:8080/app-name.


Option 2: Deploy using Docker

Build a Docker image containing the Java application.

Push the image to Docker Hub.

Run the container on any server or cloud instance.


Option 3: Deploy on AWS EC2

Copy the JAR file to an EC2 instance.

Run the application with java -jar.

Expose it through a security group for external access.




---

📊 Benefits of this Pipeline

Fully Automated CI/CD – From code commit to deployment.

Reliability – Ensures only successfully built code is deployed.

Flexibility – Supports multiple deployment targets (Tomcat, Docker, AWS).

Scalable – Can easily be extended with monitoring, notifications, and approvals.



---

✅ Deliverables

Successfully built Java artifact (.jar file).

Automated deployment on Tomcat / Docker / AWS EC2.

Jenkins pipeline execution logs with build & deployment history.



---

📌 Conclusion

This project was created by me to practice setting up a complete CI/CD pipeline for Java applications using Maven and Jenkins.
The pipeline covers everything from source code checkout → build → test → package → deploy.
