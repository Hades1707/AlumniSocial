AlumniSocial!
Overview
AlumniSocial! is a web-based application designed for Solent University alumni to connect, shop for university-branded items, and manage their profiles. The application includes user authentication, privacy settings, and an admin panel for user management.

Features
User Features:
Search for news, events, and alumni connections.
Shop for university-branded items.
Manage connections and update privacy settings.
Admin Features:
View and manage all registered users.
Handle fraudulent accounts and user reports.
Prerequisites
Before running the application, ensure the following software and tools are installed on your system:

Java Development Kit (JDK) (Version 11 or later)
Apache Tomcat (Version 10 or later)
SQLite Database (Version 3 or later)
Integrated Development Environment (IDE): NetBeans, Eclipse, or IntelliJ IDEA.

Web Browser for accessing the application.
Setup Instructions
1. Clone the Repository
Clone the project files from the repository or download the zip file and extract it.

bash
Copy code
git clone 
2. Configure the Database
Locate the AlumniSocial.db file in the resources folder.
Use SQLite tools to view or edit the database if needed.
The database includes predefined tables: users, products, orders, and connections.
3. Update Database Connection
Open DatabaseUtil.java and ensure the DATABASE_URL points to the correct location of the AlumniSocial.db file.
the database within the resources folder gets copied to the building Environment in the target folder /classes any changes made will be showed in the target
folder

4. Deploy the Application
Import the project into your IDE.
Build the project to resolve dependencies.
Deploy the compiled .war file to Apache Tomcat:
Copy the .war file to the webapps directory of your Tomcat installation.
Start the Tomcat server using:
bash
Copy code
bin/startup.sh
5. Access the Application
Open your web browser and navigate to:
arduino
Copy code
http://localhost:8080/AlumniSocial
Use the default admin credentials to log in:
Username: admin
Password: admin123
Running Tests
JUnit Tests:
Open the project in your IDE.
Run the test suite using the built-in test runner.
Ensure all tests pass before deployment.
Folder Structure
graphql
Copy code
AlumniSocial/
│
├── src/                  # Source code
│   ├── servlets/         # Servlets (e.g., AddToBasketServlet.java)
│   ├── models/           # Java models (e.g., User.java, Product.java)
│   ├── dao/              # Data Access Objects (e.g., UserDAO.java)
│
├── web/                  # Web content
│   ├── WEB-INF/          # Web application configuration files
│   ├── jsp/              # JSP files (e.g., index.jsp, shop.jsp)
│   ├── css/              # CSS files for styling
│
├── resources/            # Database and configuration files
│   ├── AlumniSocial.db   # SQLite database file
│
└── README.md             # Setup and usage instructions
Troubleshooting
Application Not Running:

Verify that Apache Tomcat is running on port 8080.
Check for errors in the Tomcat logs.
Database Issues:

Ensure the SQLite database file is accessible at the configured path.
Confirm table structures match the required schema.
Missing Dependencies:

Rebuild the project and check for missing dependencies in the IDE.
Author
David
For further assistance, please contact [bejandavid2003@gmail.com].
