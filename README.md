### Dish Diaries

Dish Diaries is a Java-based desktop application that allows users to manage their favorite recipes. The application provides features to add, view, update, delete, and search for recipes. The recipes are stored in a MySQL database.

## Features

- Add new recipes with names, descriptions, ingredients, and ratings.
- View details of each recipe in a dedicated details frame.
- Update existing recipes.
- Delete recipes.
- Filter recipes by name.
- Sort recipes by rating.
- Persist recipes using a MySQL database.

## Project Structure

The project is organized into the following packages and classes:

### FoodBook

- **Recipe**: Represents a recipe with attributes like serial number, name, description, ingredients, and rating.
- **RecipeTableModel**: Manages the data model for displaying recipes in a table format.
- **DetailsFrame**: Displays the details of a selected recipe.
- **RecipeBookMain**: The main entry point for the application.

### FoodBook.db

- **DatabaseManager**: Manages database connections and operations for adding, retrieving, updating, and deleting recipes.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or higher
- MySQL Database
- An IDE or text editor of your choice

### Setting Up the Database

1. Install MySQL and start the MySQL server.
2. Create a database named `practicejdbc`.
3. Create a table named `recipes` with the following structure:

   ```sql
   CREATE TABLE recipes (
       serial_no INT PRIMARY KEY,
       name VARCHAR(255) NOT NULL,
       description TEXT,
       ingredients TEXT,
       rating INT
   );
   ```

4. Update the database connection details in `DatabaseManager.java`:

   ```java
   connection = DriverManager.getConnection("jdbc:mysql://localhost:3307/practicejdbc", "root", "Password");
   ```

### Running the Application

1. Clone the repository:

   ```bash
   git clone https://github.com/Ishan-Parnami/Recipe-Book-Java.git
   cd dish-diaries
   ```

2. Open the project in your IDE.

3. To start the application, Build and run the `RecipeBookMain` class.

## Usage

- **Add Recipe**: Use the form to enter the recipe details and click 'Add'.
- **View Details**: Select a recipe from the table to view its details.
- **Update Recipe**: Modify the selected recipe's details and save.
- **Delete Recipe**: Remove the selected recipe from the list.
- **Filter Recipes**: Use the search box to filter recipes by name.
- **Sort Recipes**: Click the 'Sort by Rating' button to sort the recipes in descending order of their ratings.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

```
