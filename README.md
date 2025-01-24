# ::BiblioConnect: Gestion de Bibliothèque Partagée::

+ **::Description::**
   + **::BiblioConnect::** is a project designed to manage a shared library system. The project consists of three main components:
      1. **::Backend::**: A ::Spring Boot:: application that provides RESTful APIs to interact with the library database.
      2. **::Frontend - Desktop::**: A ::JavaFX::-based desktop application for admin users to manage the library and users.
      3. **::Frontend - Web::**: A web-based application for general users to view and manage library resources, built using ::ReactJS::.

   This project demonstrates how to build both desktop and web applications that interact with the same backend, offering a flexible and scalable solution for a shared library system.

+ ::Folder Structure::

   > ::BiblioConnect::/

      > ::backend::/ *# ::Spring Boot:: backend (::IntelliJ IDEA::)*

      > ::frontend::/

         > ::desktop::/ *# ::JavaFX:: desktop app (::IntelliJ IDEA::)*

         > ::web::/ *# ::ReactJS:: Web app (::VS Code::)*

      > [README.md](http://README.md) *# Project documentation*

   1. **::Backend:: (::Spring Boot::)**

   > The backend is built using **::Spring Boot::** and provides the API for communication with the frontend applications. It uses **Spring Data JPA** to interact with a **::PostgreSQL::** database.

   - > **Technologies**: Spring Boot, PostgreSQL, Spring Data JPA, Spring Security (optional).
   - > **Main Features**:
      - > User authentication (e.g., login, admin user management).
      - > Management of books, users, and library transactions.
      - > RESTful APIs for frontend communication.
   2. **::Frontend - Desktop:: (::JavaFX::)**

   > The desktop application is built using **::JavaFX::**. It provides the admin interface for managing users and library resources.

   - > **Technologies**: JavaFX.
   - > **Main Features**:
      - > Admin login page.
      - > Dashboard for managing books and users.
      - > nteraction with backend APIs to display and update data.
   3. **::Frontend - Web:: (::ReactJS::)**

   > The web application is designed using **::ReactJS::** to provide a dynamic and interactive user interface for general users to view and manage library resources.

   - > **Technologies**: ReactJS, HTML, CSS, JavaScript.
   - > **Main Features**:
      - > User login page.
      - > Display of available books in the library.
      - > User interaction with the backend to borrow books and manage their account.
+ **::Getting Started::**

   Follow these instructions to set up and run the **::BiblioConnect::** project on your local machine.

   - [ ] **Prerequisites**
      1. **JDK** (Java Development Kit) 17 or higher.
      2. **::PostgreSQL::** database.
      3. **::IntelliJ IDEA::** (for backend and desktop app).
      4. **::VS Code::** (for web frontend).
   - [ ] **::Backend:: Setup (::Spring Boot::)**
      1. Clone the repository:

```bash
git clone https://github.com/your-username/BiblioConnect.git
cd BiblioConnect/backend
```

      1. Configure ::PostgreSQL:::
         - Make sure your PostgreSQL server is running.
         - Create a database for the project (e.g., `biblio_connect_db`).
         - Configure database connection in `src/main/resources/application.properties`:

```other
spring.datasource.url=jdbc:postgresql://localhost:5432/biblio_connect_db
spring.datasource.username=your-username
spring.datasource.password=your-password
```

      1. Build and run the ::Spring Boot:: application:

```bash
mvn spring-boot:run
```

         The backend will be available on [http://localhost:8080](http://localhost:8080).

   - [ ] **::Desktop App:: Setup (::JavaFX::)**
      1. Open the `desktop/` folder in **::IntelliJ IDEA::**.
      2. Set up the JavaFX SDK by following [this guide](https://openjfx.io/).
      3. Configure the backend API URLs to match the Spring Boot application running at [http://localhost:8080](http://localhost:8080).
      4. Run the JavaFX desktop app by launching the main JavaFX class.
   - [ ] **::Web App:: Setup (::ReactJS::)**
      1. Open the `web/` folder in **::VS Code::**.
      2. If you’re using **React**, initialize the project with:

```bash
npx create-react-app .
```

      1. Configure the frontend to make API calls to the backend using `fetch` or `axios`.
      4. Open the project in **::VS Code::** and run the server :

```bash
npm start
```

         The web app will be available on [http://localhost:3000](http://localhost:3000).

+ **::Usage::**

   Once all components are running, the system can be used as follows:

   - **::Backend:: (API)**
      - API endpoints are available for managing users, books, and library transactions.
         - Example: `GET /api/books` – Fetch all books in the library.
         - Example: `POST /api/users/login` – User login endpoint.
   - **::Desktop:: (Admin Interface)**
      - Admins can log in and manage books and users using the JavaFX interface.
      - Admin functionality includes adding, updating, and deleting books, as well as managing user accounts.
   - **::Web:: (User Interface)**
      - General users can log in and view available books.
      - Users can borrow books and manage their profiles.
+ **::Project Versions::**
   + **Version 0:**
      1. > **0.0**: ::Spring Boot:: backend setup.
      2. > **0.1**: ::JavaFX:: desktop application setup.
      3. > **0.2**: Web app setup with ::ReactJS.::
+ **::Contributing::**

   If you want to contribute to this project, feel free to fork the repository and submit a pull request. You can also report issues or suggest new features.

+ **::License::**

   This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

