Best Store
A Spring Boot web application for managing products in an online store. The application allows you to create, list, and upload product details including product images.

Features
List all products
Create a new product with details such as name, brand, category, description, price, and an image
Image file upload with automatic saving of the file path
Data persistence using Spring Data JPA
Technologies Used
Java 17+
Spring Boot
Spring Data JPA
Thymeleaf (for rendering views)
Bootstrap (for basic UI styling)
H2 Database (or any other database you prefer)
Maven (for project management)
Prerequisites
Before you begin, ensure you have met the following requirements:

Java 17+ installed
Maven installed
Any IDE that supports Java (e.g., IntelliJ IDEA, Eclipse)
Git installed
Setup
Clone the repository:

bash
Copy code
git clone https://github.com/victor-butita/beststore.git
cd beststore
Update application properties:

Open src/main/resources/application.properties and update the database configuration as per your setup:

properties
Copy code
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=password
spring.jpa.database-platform=org.hibernate.dialect.H2Dialect
You can replace the H2 database with your preferred database.

Run the application:

Inside the project directory, run the following command to start the Spring Boot application:

bash
Copy code
mvn spring-boot:run
The application will be available at http://localhost:8080.

File Uploads
The product image is uploaded and saved to the public/images/ directory. Make sure to create this directory in your project root or modify the upload path in the controller if necessary.

Endpoints
/products - Displays a list of all products
/products/create - Displays a form to create a new product
Project Structure
css
Copy code
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com
│   │   │       └── victor
│   │   │           └── beststore
│   │   │               ├── controllers
│   │   │               │   └── ProductsController.java
│   │   │               ├── models
│   │   │               │   ├── Product.java
│   │   │               │   └── ProductDto.java
│   │   │               └── services
│   │   │                   └── ProductRepository.java
│   │   └── resources
│   │       ├── templates
│   │       │   └── products
│   │       │       ├── index.html
│   │       │       └── CreateProduct.html
│   │       └── application.properties
├── public
│   └── images
How to Contribute
Fork the repository
Create a new branch (git checkout -b feature-branch)
Make your changes
Commit your changes (git commit -m 'Add some feature')
Push to the branch (git push origin feature-branch)
Create a new Pull Request