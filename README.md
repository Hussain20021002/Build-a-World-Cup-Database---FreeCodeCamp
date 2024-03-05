# Build-a-World-Cup-Database---FreeCodeCamp
This is one of the required projects to earn your certification. For this project, you will create a Bash script that enters information from World Cup games into PostgreSQL, then query the database for useful statistics.




This project involves creating a database, inserting data from a CSV file, and querying the database to analyze World Cup data. The database contains information about the final three rounds of the World Cup tournament since 2014, including the year of each game, the round of the game, the winner, their opponent, and the number of goals each team scored.

## Project Structure
---------------------------

The project consists of the following files:

- `games.csv`: A CSV file containing the data for the final three rounds of the World Cup tournament since 2014.
- `create_database.sql`: SQL script to create the database structure.
- `insert_data.sh`: Bash script to insert data from `games.csv` into the database.
- `queries.sh`: Bash script to query the database and analyze the World Cup data.
- `README.md`: This README file.

## Database Structure
------------------------------

The database structure includes two tables:

- `teams`: Contains information about the teams participating in the World Cup.
  - Columns: `team_id` (SERIAL, primary key), `name` (UNIQUE).
- `games`: Contains information about the World Cup games.
  - Columns: `game_id` (SERIAL, primary key), `year` (INT), `round` (VARCHAR), `winner_id` (foreign key referencing `team_id`), `opponent_id` (foreign key referencing `team_id`), `winner_goals` (INT), `opponent_goals` (INT).

## Usage
------------
1. **Create the Database**: Log into the psql interactive terminal and run the `create_database.sql` script to create the database structure.

2. **Insert Data**: Execute the `insert_data.sh` script to insert data from `games.csv` into the database.

3. **Query the Database**: Run the `queries.sh` script to analyze the World Cup data. The script contains queries to retrieve various statistics, such as total number of goals, average goals, most goals scored in a single game, etc.

4. **Expected Output**: The output of the queries should match the expected output provided in the project description.

## Testing
--------------
To test the project, execute the `queries.sh` script and compare the output with the expected output.

## Notes
----------------
- Ensure that you have the necessary permissions to execute the scripts and access the database.
- Make sure to replace the database credentials in the scripts if they differ from the provided ones.
