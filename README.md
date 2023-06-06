# Football Data Import and Table Relationships in PostgreSQL

This project demonstrates a Python script in a Jupyter Notebook that imports football data from CSV files into PostgreSQL tables and establishes relationships between the tables. It utilizes pandas for data reading, psycopg2 for database connection, and SQLAlchemy for interaction with the database.

The football data used in this project is sourced from the Kaggle dataset: [International Football Results from 1872 to 2017](https://www.kaggle.com/martj42/international-football-results-from-1872-to-2017).

## Prerequisites

- Python
- Jupyter Notebook
- PostgreSQL

## Getting Started

1. Clone this repository or download the project files.

2. Import the football data into the PostgreSQL database:

   - Open the Jupyter Notebook file `import_data.ipynb`.

   - Execute the code cells in the notebook to import the data, create tables, establish relationships, and perform database operations.

   - Make sure to update the database connection parameters (`host`, `port`, `database`, `user`, `password`) in the notebook according to your PostgreSQL setup.

3. Review and modify the code as needed for your specific requirements.

## Project Structure

The project contains the following files:

- `import_data.ipynb`: Jupyter Notebook containing the code for importing data and establishing table relationships.

- `datasets/results.csv`: CSV file containing match results data.

- `datasets/shootouts.csv`: CSV file containing shootout data.

- `datasets/goalscorers.csv`: CSV file containing goalscorers data.

## Database Structure

The script creates the following tables in the PostgreSQL database:

- `results`: Table containing match results data.
- `shootouts`: Table containing shootout data.
- `goalscorers`: Table containing goalscorers data.

The tables are related as follows:
- `shootouts` and `goalscorers` have a foreign key `result_id` referencing the `id` column in the `results` table.

## Contributing

Contributions to the project are welcome! If you have any suggestions, improvements, or feature requests, please feel free to submit an issue or a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
