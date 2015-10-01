# Tournament Database
Project 2 for Full Stack Nanodegree

This is a database schema to store matches between players in a Swiss style tournament (non-elimination).
An overview of the files:
  - `tournament.sql` creates the database, tables, and view
  - `tournament.py` contains a number of functions to add to and access the database
  - `tournament_test.py` contains a number of test functions
  
# Required Libraries
  - bleach
  - psycopg2
  
# How to run

1. Initialize the database using `psql`
  `\i tournament.sql`
2. Quit `psql`
3. Run `tournament_test.py` to ensure correct initialization
  `python tournament_test.py`
  
# Functions in `tournament.py`
`tournament.py` contains many functions for interacting with the database:

  - `connect()` connects to the database
  - `deleteMatches()` deletes all matches from the database
  - `deletePlayers()` deletes all players from the database
  - `countPlayers()` counts the number of registered players
  - `registerPlayer(name)` registers the player `name`
  - `playerStandings()` outputs the list of registered players ordered by total wins
  - `reportMatch(winner, loser)` records the match played by `winner` and `loser`
    Note: `winner` and `loser` should be player ID numbers, not names
  - `swissPairings()` returns the next round of matches
  
