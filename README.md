# Django React PostgreSQL Integration

## Introduction
This Django application serves as an API endpoint for a React frontend, with PostgreSQL as the database backend.

## Setup Instructions

### Prerequisites
- Python 3.x installed on your system.
- Node.js and npm installed on your system.
- PostgreSQL installed and running on your local machine.

### Installation Steps

1. Clone this repository to your local machine:
git clone https://github.com/sjkrta/djrpsq.git
cd djrpsq

2. Set up a virtual environment for Python (recommended):
python3 -m venv .venv
source env/bin/activate # For Unix/MacOS
env\Scripts\activate # For Windows

3. Install Python dependencies:
pip install -r requirements.txt


4. Create a PostgreSQL database:
- Open your PostgreSQL command line or GUI tool.
- Run the following SQL commands to create a database named `djrpsq` and a user named `djrpsq` with the password `djrpsq`:
  ```
  CREATE DATABASE djrpsq;
  CREATE USER djrpsq WITH PASSWORD 'djrpsq';
  ALTER ROLE djrpsq SET client_encoding TO 'utf8';
  ALTER ROLE djrpsq SET default_transaction_isolation TO 'read committed';
  ALTER ROLE djrpsq SET timezone TO 'UTC';
  GRANT ALL PRIVILEGES ON DATABASE djrpsq TO djrpsq;
  ```

5. Apply database migrations:
python manage.py migrate

6. Install Node.js dependencies for the React frontend:
cd djrpsq-client
npm install

<!-- 7. Set up environment variables for Django:
- Create a `.env` file in the root directory of the project.
- Add the following environment variables to the `.env` file:
  ```
  DATABASE_URL=127.0.0.1
  ``` -->

8. Start the Django development server:
python manage.py runserver

<!-- 9. Start the React development server:
d frontend
npm start -->

10. Access the application:
 - Open your web browser and go to http://localhost:8000 to access the React frontend.

## Additional Notes
- This setup assumes you are running Django and React on your local machine.
- Make sure your PostgreSQL server is running before starting the Django server.

