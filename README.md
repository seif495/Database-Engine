# Java Database Engine

A lightweight, relational database management system built from scratch using **Java** and **ANTLR**. This engine is designed to parse SQL-like queries and perform efficient CRUD (Create, Read, Update, Delete) operations on data.

## Features

- **SQL Query Parsing**: Utilizes [ANTLR](https://www.antlr.org/) to parse and validate complex SQL-like commands.
- **CRUD Operations**: Full support for:
  - **Create**: Define new tables and schema.
  - **Read**: Select and filter data from tables.
  - **Update**: Modify existing records based on conditions.
  - **Delete**: Remove records or drop tables.
- **Metadata Management**: Handles schema definition and persistence via `metadata.csv`.
- **Custom Storage**: Implements direct file I/O for data persistence.

## 🛠️ Tech Stack

- **Language**: Java (JDK 1.8+)
- **Parser**: ANTLR 4
- **Build Tool**: Maven

## Project Structure

The core logic is located in the `Java_Database_Engine` directory:

```text
Java_Database_Engine/
├── src/               # Source code (Engine logic, B+ Tree, Page management)
├── target/            # Compiled classes
├── metadata.csv       # Schema definition and table metadata
├── pom.xml            # Maven dependencies (including ANTLR)
└── starter_code/      # Initial setup and utility classes
```

## Getting Started

### Prerequisites

- Java Development Kit (JDK)
- Maven

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/seif495/Database-Engine.git
   ```

2. Navigate to the project directory:
   ```bash
   cd Database-Engine/Java_Database_Engine
   ```

3. Build the project using Maven:
   ```bash
   mvn clean install
   ```

## Usage

To start the engine, run the main application entry point (check the `src` folder for the Main class). You can execute commands such as:

**Creating a Table:**
```sql
CREATE TABLE Student (id int, name varchar, gpa double, PRIMARY KEY(id));
```

**Inserting Data:**
```sql
INSERT INTO Student VALUES (1, "John Doe", 3.8);
```

**Selecting Data:**
```sql
SELECT * FROM Student WHERE gpa > 3.5;
```

## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any bugs or feature enhancements.
