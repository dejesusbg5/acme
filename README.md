# ACME Voting System

A simple and effective voting system designed for educational institutions to conduct student government elections with transparency and security. It supports various user roles, including administrators, voters, and witnesses, ensuring a fair and auditable election process.

## Installation

Follow these steps to set up the ACME Voting System on your local machine.

### Prerequisites

- PHP 7.4 or higher
- MySQL 5.7 or higher

### Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/dejesusbg/acme-voting.git
   cd acme-voting
   ```

2. **Set up the database:**
   - Create a new MySQL database.
   - Import the `acme.sql` file from the `sql/` directory to create the necessary tables and populate them with sample data.

3. **Configure the application:**
   - Open `config.json` and update the database connection settings:
     ```json
     {
         "host": "your_host",
         "username": "your_username",
         "password": "your_password",
         "database": "your_database"
     }
     ```

4. **Adjust server settings (if necessary):**
   - If you change the project folder name, update the following files:
     - `.htaccess` (line #3): `RewriteBase /new_folder_name/`
     - `index.php` (line #3): `<?php $name = 'new_folder_name'; ?>`
   - If you change the database name, update `config.json` as described in step 3.

## Usage

Once the installation is complete, you can access the application by navigating to the project folder in your web browser.

### User Roles and Credentials

The system comes with predefined user roles, each with specific permissions:

- **Admin:** Manages the election process, users, and candidates.
- **Voter:** Can cast a vote.
- **Witness:** Monitors the voting process.
- **Jury:** Validates votes.

Sample credentials are available in the `usuario` table in the database.

## Project Structure

The project follows a simplified MVC-like pattern:

- `base/`: Core database connection logic.
- `controllers/`: Handles business logic and user interactions.
- `libs/`: Contains helper libraries and utilities.
- `models/`: Manages data and database operations.
- `sql/`: Contains database schema and sample data.
- `views/`: Includes all UI components and pages.

## Contributing

Contributions are welcome! Please feel free to submit a pull request.
