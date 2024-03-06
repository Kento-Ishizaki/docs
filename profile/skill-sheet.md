# **Skill Sheet 2024.03.01**

## **Basic Information**

- **Name:** K・I
- **Gender:** Male
- **Age:** 33
- **Residence:** Cebu Island (moving to Japan from April)

## **Overview**
- After 5 years of experience in corporate sales, I started my career as a Ruby on Rails engineer in web engineering, and subsequently gained experience mainly in Flutter → Golang. Recently, I have had increasing opportunities to be involved in the cloud infrastructure area.
- Frequently involved in projects from inception (0 to 1) since the beginning of my career, gaining experience in database design and client negotiations. Strengths include reading English documents—utilizing study abroad experience, quick learning of new languages/technologies, and high communication skills, aided by a background in sales.

## **Skills (Only technologies used in professional settings are listed)**

### **Languages**
- Ruby
- Dart
- Golang
- TypeScript
- JavaScript
- Swift
- Kotlin
- Python
- PHP

### **Frameworks & Libraries**

- Ruby on Rails
- Revel
- Gin
- React
- Next.js
- Vue
- Flask
- WordPress

### **Cloud**

- AWS
  - VPC
  - S3
  - Lambda
  - EC2
  - Route53
  - ACM
  - IAM
  - CloudWatch
  - EventBridge
  - Step Functions
  - AWS Batch
  - SES
  - SNS
  - ALB
  - GuardDuty
  - Config

### **Others**
- MySQL
- PostgreSQL
- SQLite
- Docker
- Terraform
- nginx
- VPS

## **Qualifications**

- Fundamental Information Technology Engineer Examination (May 2021)
- AWS Certified Solutions Architect – Associate (November 2021)

## **Languages**

- Japanese
  - Native
- English
  - TOEIC: 735 (as of January 2023)
  - Conversational (studied abroad in the Philippines)

## **Professional Experience (in descending order)**

### **Infrastructure/Backend Development at a Startup Focused Company (August 2023 - Present)**

**Project Overview:**

- Addition of AWS resources managed by Terraform
- Backend design, development, and testing for new web system development projects

**Technologies Used:**

- Languages: Golang, TypeScript
- Frameworks: Revel, Next.js
- Others: AWS, Terraform, MySQL

**Responsibilities:**
- Addition of AWS resources using Terraform
  - Step Functions resources for executing ECS tasks
  - AWS Batch resources for scheduled execution of ECS tasks
  - Notification functionality to Discord via SNS/Lambda/EventBridge for ECS deployment success/failure, GuardDuty findings, CloudWatch alarms
- Backend development with Golang
  - Full development of a service with over 70 tables using Revel and an in-house code generation service.
  - Rebuilding a system written in TypeScript/NestJS by another vendor in Golang. Despite limited information from the other vendor and unclear specifications, successfully ported an image generation feature combining multiple images.

**Value Delivered:**

Despite being new to using Terraform in a professional setting, quickly caught up with the Terraform setup implemented by the predecessor and started creating and merging resource creation PRs within the first month of joining. Contributed to the stable operation of resources deployed across multiple projects. For backend development, took over when another vendor became unresponsive, and despite internal predictions of high difficulty in rewriting to Golang, successfully implemented image generation and batch processing functionalities within approximately two weeks. Also handled minor frontend adjustments implemented by the other vendor, delivering the project without critical bugs and before the client's desired deadline.

### **Management/Infrastructure Construction in Offshore Development (August 2023 - Present)**

**Project Overview:**

- Design and management of system development projects ordered by Japanese companies
- Construction of development, testing, and production environments

**Technologies Used:**

- Languages: AWS, Terraform, PHP, TypeScript
- Frameworks: Laravel, Next.js
- Others: MySQL, Docker, nginx, VPS, Tailwind CSS

**Responsibilities:**
- Construction of testing and production environments using AWS/sakura VPS
  - Implemented several testing environments using EC2/ACM/Route53/ALB. Designed and implemented according to client requests, such as allowing Next.js and WordPress to coexist on the same domain via path routing. Innovated solutions such as using EC2's memory swap feature to prevent memory resource pressure within a limited budget. For the production environment, built on the client-specified sakura VPS, including automatic SSL certificate renewal.
- Development environment setup using docker-compose
  - Introduced Docker for the first time in the company to improve the efficiency of environment setup tasks and to reduce errors due to environment differences. Implemented a Docker development environment for nginx/Laravel/Next.js/MySQL/Localstack that can be started with a single command using a Makefile.
- New project DB/architecture design
  - Responsible for DB design and technology stack selection based on client interviews. Introduced Mermaid Chart to ensure that changes in DB design are communicated to engineers in real-time. Also conducted architecture design for Flutter/Next.js and documented in English in READMEs. Provided examples of switching data sources using environment variable mock flags and Repositories, and outlined responsibilities for each directory with sample code.

**Value Delivered:**

Despite being in an English-speaking environment and a technology stack that was significantly different from past experiences, managed to refresh both frontend and infrastructure technologies, earning high praise from local engineers. Although development speed did not increase as expected in the initial phase of development with the new stack, it picked up from the second week, and by using the same technology stack in parallel with another project, contributed to the standardization of company technology. Eventually received feedback from management expressing a desire to use the same technology stack as much as possible in the future.

### **CI Tool Development & Modification (April 2022 - March 2023)**

**Project Overview:**

- Addition and modification of features for an in-house CI tool used during system development at a major company.
- Transition support from GOPATH to MODULE mode
- Go version upgrade (Ver1.12 to 1.19.5)

**Technologies Used:**

- Language: Golang
- Others: PostgreSQL, Bash, Kubernetes, Helm, GAE

**Responsibilities:**
- Backend development with Golang
- Package updates and code modifications related to the Go version upgrade.

**Value Delivered:**

Implemented test-driven development to minimize implementation errors in an environment where builds took 4-5 minutes. Despite being new to Golang, grew to the point of being able to submit 1-2 PRs every 1-2 days after the second month. The deployment method to GAE differs between GOPATH and MODULE modes, requiring specific actions such as "downloading packages from private repositories to a specific path" and "modifying the go.mod file" during deployment. Successfully implemented a Shell script that achieved this with a single command, contributing to the migration to the latest version of Go at the time.

### **Contract Management/Internal Asset Management App Development (June 2021 - November 2021) ※Full-time**

**Project Overview:**

- Full replacement of an iOS app displaying a WebView, and new development of an Android app

**Technologies Used:**

- Languages: Dart, Swift, Kotlin
- Framework: Flutter
- Others: SQLite

**Responsibilities:**
- Development of camera functions for each OS using native code (Swift/Kotlin) and OpenCV
  - Extended the WeScan (Swift) library and the SmartPaperScan (Kotlin) library to adjust the camera UI, crop rectangles, rotate, adjust contrast, sort, and more.
- App development with Flutter
  - Implemented mainly UI and communication with the backend in Flutter. To simplify Flutter code, images captured and processed in Swift and Kotlin libraries were passed to Flutter via MethodChannel with unified data types, allowing upload processing to be executed with common code.
- State management with Riverpod and Hooks
  - Successfully implemented minimal rebuilds by using StateProvider, StateNotifierProvider, Hooks, and avoiding the use of StatefulWidget classes.

**Value Delivered:**

Originally, the iOS app saved captured images in memory, and the same specification was initially implemented for the Android version. However, memory overflow occurred on some devices, leading to a design change to utilize SQLite. Later investigation revealed that the original iOS app also experienced overflow, but the design change contributed to bug resolution. For UI displaying multiple images, displayed resized thumbnail images to eliminate operational delays and stabilize performance. As much as possible, functions without OS differences were processed in Flutter, reducing native code to a minimum and striving for a codebase with less volume and higher maintainability.

### **Business Communication App Development (April 2020 - May 2021) ※Full-time**

**Project Overview:**

- Development of a business-oriented app specialized in calls using WebRTC
- Application submission and release to the Apple Store

**Technologies Used:**
- Languages: Dart, Swift
- Framework: Flutter

**Responsibilities:**
- Acted as a project leader, serving as a bridge between the company's upper management and the development team, and worked on schedule adjustments and documentation to solidify specifications.
- Took charge of the release single-handedly, challenging Flutter and Swift with no prior experience and catching up in both professional and personal capacities.

**Value Delivered:**

Despite the absence of engineers proficient in Flutter within the company and the low recognition of Flutter in Japan at the time, managed to release to the store by rapidly cycling through hypothesis testing and verification based on English documentation reading. Also implemented a call forwarding feature, differentiating it from existing calling apps, and successfully integrated with iOS call history. This led to a significant improvement in the evaluation from superiors, leading to a discussion of a raise and promotion before the appraisal.

### **Backend Development for LINE-style Chat & Integrated SNS Service (November 2019 - April 2020) ※Full-time**

**Project Overview:**

- App development aimed at increasing communication among drivers of a major logistics company and between headquarters and drivers
- Features text-based chat, bulletin boards, and an incentive mechanism through point exchange

**Technologies Used:**
- Languages: Ruby, JavaScript
- Frameworks: Ruby on Rails, Vue
- Others: MySQL, Chart.js

**Responsibilities:**
- Engaged in 0 to 1 backend design and development with RoR, venturing beyond simple CRUD to try features like real-time chat with Action Cable.

**Value Delivered:**

Rapidly iterated through "DB/model design → feedback with another backend engineer," minimizing rework and succeeding in delivering 2 weeks ahead of the deadline. Specifically, changed the cycle from implementing DB/models/controllers before submitting PRs to drafting PRs at the DB/model design phase, starting implementation after review approval. During the project, the frontend engineer became overloaded, contributing to the implementation of an admin panel using Vue and Chart.js for about 2 months, facilitating smooth project progress. Shared API specifications with Swagger to prevent halting the implementation of frontend and mobile engineers.
