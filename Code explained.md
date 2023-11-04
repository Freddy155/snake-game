Code Documentation
========================

This documentation explains the Python code for a simple Snake game using the Pygame library. The code is divided into various sections to manage the game's functionality.

Game Setup
----------

-   Import the necessary modules, such as `pygame`, `time`, and `random`.
-   Set the game's speed (frames per second) as `snake_speed`.
-   Define the game window's size with `window_x` and `window_y`.
-   Define colors using Pygame's `pygame.Color()` function.

Initialize Pygame
-----------------

-   Initialize the Pygame library using `pygame.init()`.
-   Set the game window's title to 'Snake Game' using `pygame.display.set_caption()`.
-   Create the game window using `pygame.display.set_mode()` with the defined window size.

FPS Controller
--------------

-   Initialize the FPS (frames per second) controller using `fps = pygame.time.Clock()`.

Snake and Fruit Setup
---------------------

-   Define the initial position of the snake head with `snake_position`.
-   Define the initial snake body with the head and the first three body segments in `snake_body`.
-   Initialize the fruit's position randomly using `fruit_position` and set `fruit_spawn` to True.

Game Variables
--------------

-   `direction` is set to 'RIGHT' initially, representing the snake's movement direction.
-   `change_to` is used to temporarily store the desired direction of movement.
-   Initialize the `score` to 0.

Display Functions
-----------------

### `show_score()`

-   This function displays the current score on the game window.

### `game_over()`

-   This function is called when the game ends.
-   It displays the player's final score and waits for 2 seconds before quitting the game.

Main Game Loop
--------------

The main game loop runs continuously and handles various aspects of the game.

### Event Handling

-   It listens for keyboard events using `pygame.event.get()`.
-   When arrow keys are pressed, the `change_to` variable is updated to change the snake's direction.

### Direction Handling

-   Ensures that the snake can't move in the opposite direction immediately.

### Snake Movement

-   Moves the snake's head in the chosen direction based on the current `direction`.
-   Updates the snake's body to make it grow.

### Fruit Collection

-   Checks if the snake's head collides with a fruit.
-   If so, increments the score by 10 and respawns the fruit.

### Game Over Conditions

-   Checks if the snake hits the game window's boundaries or collides with its own body.
-   Calls the `game_over()` function when any of these conditions are met.

### Drawing Game Elements

-   Draws the snake's body and the fruit on the game window.

### Displaying Score

-   Calls `show_score()` to continuously display the score.

### Refresh Game Screen

-   Updates the game window to reflect the changes.

### Frame Per Second

-   Controls the game's frame rate using `fps.tick()`.