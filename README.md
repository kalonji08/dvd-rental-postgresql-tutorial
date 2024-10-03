# DVD Rental PostgreSQL Tutorial

## Introduction

Welcome to the **DVD Rental PostgreSQL Tutorial** repository!

This project is designed to help me and anyone else interested in learning PostgreSQL and SQL, using the popular **DVD Rental** sample database. The database represents the business processes of a DVD rental store and is perfect for practising various PostgreSQL features.

The sample database, along with some of the content in this repository, has been sourced from [PostgreSQL Tutorial](https://www.postgresqltutorial.com/). I will be using it to demonstrate key concepts in SQL and PostgreSQL.

### Features of the DVD Rental Database:

- **15 Tables**: Includes actor, film, customer, rental, payment, and more.
- **1 Trigger**: Automatically updates the last modification date.
- **7 Views**: Simplifies data access for reporting.
- **8 Functions**: Built-in PostgreSQL functions to extend functionality.
- **1 Domain**: A custom data type.
- **13 Sequences**: Used to auto-generate primary key values.

This repository is intended for anyone looking to sharpen their PostgreSQL skills. Feel free to explore the database, run the scripts, and contribute by adding new content!

---

## Getting Started

### 1. Prerequisites

To get started, make sure you have the following installed on your machine:

- **PostgreSQL**: You can download it [here](https://www.postgresql.org/download/).
- **DBeaver** (Optional): A database management tool that can be used to connect and manage your PostgreSQL databases. [Download DBeaver](https://dbeaver.io/download/).

### 2. Install PostgreSQL

Once you have PostgreSQL installed, you can use the `psql` command-line interface to interact with the PostgreSQL server.

### 3. Download the DVD Rental Sample Database

The sample database can be downloaded from the PostgreSQL Tutorial website:

- [Download DVD Rental Sample Database](https://www.postgresqltutorial.com/wp-content/uploads/2019/05/dvdrental.zip)

After downloading, extract the `dvdrental.zip` file to get the `dvdrental.tar` file.

### 4. Restoring the DVD Rental Database

#### Step 1: Connect to PostgreSQL
Open a terminal and connect to PostgreSQL using the following command:

```bash
sudo -u postgres psql
```

#### Step 2: Create a New Database
Create a new database named `dvdrental`:

```sql
CREATE DATABASE dvdrental;
```

Exit the `psql` terminal by typing:

```bash
\q
```

#### Step 3: Restore the Database
Run the following command to restore the `dvdrental` database from the `.tar` file:

```bash
pg_restore -U postgres --dbname=dvdrental --verbose dvdrental.tar
```

#### Step 4: Verify the Database
Connect to PostgreSQL again and switch to the `dvdrental` database:

```bash
psql -U postgres
\c dvdrental
```

Now, you're ready to run queries on the `dvdrental` database.

---

## Folder Structure

Here’s the structure of this repository:

```bash
dvd-rental-postgresql-tutorial/
│
├── dataset/                  # Contains the dataset files
│   ├── dvdrental.tar         # Extracted sample database file
│   └── ER_Diagram.pdf        # Optional: Printable ER Diagram
│
├── sql_scripts/              # Collection of SQL scripts for different tasks
│   ├── 01_create_database.sql  # Script to create the database
│   ├── 02_basic_queries.sql    # Basic SQL queries
│   ├── 03_joins.sql            # SQL joins (INNER, LEFT, RIGHT, etc.)
│   ├── 04_advanced_queries.sql # Functions, views, triggers, and more
│   └── 05_data_analysis.sql    # Data analysis queries
│
├── docs/                     # Documentation and tutorials
│   ├── connecting_to_postgresql.md  # Guide on setting up PostgreSQL
│   ├── interacting_with_database.md # CRUD operations and queries
│   ├── advanced_features.md         # Guide on triggers, views, functions
│   └── dbeaver_integration.md       # Guide to connect PostgreSQL with DBeaver
│
├── images/                   # Image resources used in documentation
│   └── ER_Diagram.png        # Optional: PNG version of the ER Diagram
│
├── .gitignore                # Specifies files to ignore in the repository
├── LICENSE                   # License for open-source contribution (optional)
└── README.md                 # Main README file with project instructions
```

---

## Learning SQL with DVD Rental

This repository provides a set of SQL scripts to help you learn and practice SQL using the `dvdrental` database. The scripts are organised into the `/sql_scripts/` folder, categorised by topic:

1. **Creating the Database** (`01_create_database.sql`)
2. **Basic Queries** (`02_basic_queries.sql`)
3. **Joins** (`03_joins.sql`)
4. **Advanced Queries** (`04_advanced_queries.sql`)
5. **Data Analysis** (`05_data_analysis.sql`)

You can load these scripts in your PostgreSQL environment or use a tool like **DBeaver** to run them interactively.

---

## Connecting PostgreSQL to DBeaver

You can use [DBeaver](https://dbeaver.io/download/) to visually manage your PostgreSQL database. Refer to the [DBeaver Integration Guide](./docs/dbeaver_integration.md) for detailed steps on how to connect your `dvdrental` database to DBeaver for easier management.

---

## Contributing

Feel free to contribute by adding more SQL scripts, improving documentation, or suggesting ways to better learn PostgreSQL. Whether you're a beginner or an advanced user, your contributions are welcome!

---

## Resources

- [PostgreSQL Documentation](https://www.postgresql.org/docs/)
- [PostgreSQL Tutorial - DVD Rental Database](https://www.postgresqltutorial.com/postgresql-sample-database/)
- [DBeaver](https://dbeaver.io/)

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

### Acknowledgement

The DVD Rental sample database and some content were sourced from [PostgreSQL Tutorial](https://www.postgresqltutorial.com/). Please refer to their website for further information and resources.
