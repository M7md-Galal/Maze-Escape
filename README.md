# MazeEscape

MazeEscape is a simple console-based maze game written in C#. The player navigates through a maze, avoiding walls and finding the exit.

## Features

- Randomly generated maze
- Player movement using arrow keys
- Console-based graphics

## Installation

1. Clone the repository:
    2. Open the solution in Visual Studio 2022.
3. Build the solution to restore the necessary packages.

## Usage

1. Run the application.
2. Use the arrow keys to move the player (`^`) through the maze.
3. Avoid walls (`=`) and navigate to the exit.

## Project Structure

- `Program.cs`: Entry point of the application. Initializes the maze and starts the game loop.
    - Initializes a `Maze` object with a fixed size of 20 rows and 40 columns.
    - Continuously draws the maze and updates player movement in a loop.

- `Maze.cs`: Contains the logic for generating and drawing the maze, as well as handling player movement.
    - `Maze`: Class representing the maze.
        - `Maze(int rows, int cols)`: Constructor to initialize the maze with specified dimensions.
        - `DrowMaze()`: Method to draw the maze on the console.
        - `Move(int dx, int dy)`: Method to move the player within the maze.
        - `UpdatePlayerMovement()`: Method to handle player input and update movement.

- `IMazeObj.cs`: Interface for maze objects, defining properties for symbol and walkability.
    - `IMazeObj`: Interface representing a maze object.
        - `char Symbol { get; }`: Property representing the symbol of the maze object.
        - `bool IsWalkable { get; }`: Property indicating if the object is walkable.

- `Wall.cs`: Represents a wall in the maze. Walls are not walkable and are represented by the `=` symbol.
    - `Wall`: Class implementing `IMazeObj` for walls.
        - `char Symbol => '='`: Symbol representing a wall.
        - `bool IsWalkable => true`: Indicates that walls are not walkable.

- `EmptySpace.cs`: Represents an empty space in the maze. Empty spaces are walkable and are represented by a space character.
    - `EmptySpace`: Class implementing `IMazeObj` for empty spaces.
        - `char Symbol => ' '`: Symbol representing an empty space.
        - `bool IsWalkable => false`: Indicates that empty spaces are walkable.

- `Player.cs`: Represents the player in the maze. The player is represented by the `^` symbol and can move through walkable spaces.
    - `Player`: Class implementing `IMazeObj` for the player.
        - `char Symbol => '^'`: Symbol representing the player.
        - `bool IsWalkable => true`: Indicates that the player can move through walkable spaces.
        - `int X { get; set; }`: X-coordinate of the player.
        - `int Y { get; set; }`: Y-coordinate of the player.

## Game Mechanics

- The maze is generated with a fixed size of 20 rows and 40 columns.
- The player starts at position (1, 1) in the maze.
- Walls are placed around the perimeter of the maze and at regular intervals within the maze.
- The player can move up, down, left, or right using the arrow keys.
- The game loop continuously updates the maze and player movement until the application is closed.

## Requirements

- .NET 6
- Visual Studio 2022

## License

This project is licensed under the MIT License.
