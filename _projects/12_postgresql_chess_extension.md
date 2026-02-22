---
layout: page
title: PostgreSQL Chess Extension
description: Created a custom PostgreSQL extension for storing and analyzing chess games, introducing chess-specific data types, functions, and indices for efficient querying.
img: assets/img/chess_postgresql.png
importance: 4
year: 2023
semester: Fall 2023
github: https://github.com/kamrulkonok/ULB-H417-PGchess
technologies: PostgreSQL, C, SQL, Linux, Database Systems, Indexing
---

## Overview

A custom PostgreSQL extension developed as a course project for INFOH417 Database System Architecture (2023/24) at Université Libre de Bruxelles (ULB). The extension facilitates the storage and retrieval of chess games within PostgreSQL, supporting chess-specific data types, functions, and indices for efficient querying of chess game data.

## Features

The extension introduces two custom data types and several specialized functions:

### Custom Data Types

- **`chessboard`**: Represents a specific board state in a chess game
- **`chessgame`**: Represents a sequence of moves for an entire chess game

### Functions

- **`getBoard(chessgame, integer) -> chessboard`**: Returns the board state at a specified half-move count
- **`getFirstMoves(chessgame, integer) -> chessgame`**: Truncates and returns the first *N* half-moves of a game
- **`hasOpening(chessgame, chessgame) -> bool`**: Checks if a chess game begins with a specific sequence of moves
- **`hasBoard(chessgame, chessboard, integer) -> bool`**: Verifies if a specific board state appears within the first *N* half-moves

### Indices

- **`hasOpening_idx`**: B-tree index for efficient lookup of games with specific opening sequences
- **`hasBoard_idx`**: GIN index that uses `getAllStates(chessgame)` to index individual board states across moves

## Technical Implementation

Implemented in C as a PostgreSQL extension with PL/pgSQL components, leveraging PostgreSQL's extensibility framework. Supports standard chess notation formats: **Standard Algebraic Notation (SAN)** for move sequences and **Forsyth–Edwards Notation (FEN)** for board positions.

## Key Results

Enables efficient storage and querying of chess games within PostgreSQL, supporting advanced chess analysis queries such as finding games with specific opening sequences or board positions. Custom indices significantly improve query performance for common chess analysis operations.

## Technologies

PostgreSQL, C, SQL, Linux, Database Systems, Indexing

