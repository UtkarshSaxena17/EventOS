# Setting Up EventOS 🚀

Follow these instructions to run EventOS locally on your machine. This guide is perfect for setting up a local testing environment for hackathons or contributing to the project.

## Prerequisites
Before you begin, ensure you have the following installed:
- **Node.js** (v18.0 or higher) - [Download here](https://nodejs.org/)
- **MySQL Server** (v8.0 or higher) - [Download here](https://dev.mysql.com/downloads/mysql/)
- **Git** - [Download here](https://git-scm.com/)

## 1. Clone the Repository
Clone the repository to your local machine and navigate into the directory:
```bash
git clone https://github.com/modeduser/EventOS.git
cd EventOS
```

## 2. Install Dependencies
Install the required Node.js packages using npm:
```bash
npm install
```

## 3. Database Setup
1. Open your MySQL client or command line.
2. Create a new database named `eventos`:
   ```sql
   CREATE DATABASE eventos;
   ```
   *(Note: The server will automatically create all required tables upon starting.)*

## 4. Environment Configuration
1. In the root directory, create a file named `.env`.
2. You can use the provided `.env.example` as a template:
   ```bash
   cp .env.example .env
   ```
3. Open `.env` and update the database credentials to match your local MySQL setup:
   ```env
   DB_HOST=localhost
   DB_USER=root
   DB_PASSWORD=your_mysql_password
   DB_NAME=eventos
   PORT=3000
   ```

## 5. Run the Application
Start the Node.js server:
```bash
npm start
```

You should see: `Server is running on http://localhost:3000`. 
The database tables will be automatically seeded, and an initial admin account will be created:
- **Email:** `admin@eventos.local`
- **Password:** `admin123`

Enjoy using EventOS! 🎉
