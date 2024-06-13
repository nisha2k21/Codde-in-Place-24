### Baby Snake Game Project

**Project Description:**

In this assignment, we are going to create a simplified version of the classic Atari game Snake. This game was famously available on original Apple II computers and Nokia phones. Our goal is to build a basic version and gradually extend it. 

**Milestone #1: Set up the World**

In the first milestone, we'll set up the game world. The game world will consist of a grid where a blue square represents the "player" and a red square represents the "goal". Both the player and the goal will be 20 pixels by 20 pixels.

**Objectives:**

1. **Draw the Game World:**
   - Create a game window where the player and the goal will be displayed.
   - The player should start in the top left corner of the window.
   - The goal can be placed anywhere within the window, but its x and y coordinates should both be multiples of 20 for simplicity.

**Configuration Example:**
- Player's initial position: (0, 0)
- Goal's position: (360, 360)

**Requirements:**
- Implement the game world setup using a graphical library (e.g., Pygame in Python).
- Ensure the player and the goal are correctly displayed with the specified dimensions and positions.

### Implementation Steps:

1. **Set Up the Environment:**
   - Install and import the necessary graphical library.
   
2. **Create the Game Window:**
   - Define the dimensions of the game window.
   
3. **Draw the Player and the Goal:**
   - Create a blue square for the player at the starting position (0, 0).
   - Create a red square for the goal at the position (360, 360) or any other position with x and y values being multiples of 20.

### Sample Code:

Here is a sample implementation using Pygame:

```python
import pygame
import sys

# Initialize Pygame
pygame.init()

# Constants
WINDOW_SIZE = 400
GRID_SIZE = 20
PLAYER_COLOR = (0, 0, 255)  # Blue
GOAL_COLOR = (255, 0, 0)    # Red
BACKGROUND_COLOR = (0, 0, 0) # Black

# Set up the display
window = pygame.display.set_mode((WINDOW_SIZE, WINDOW_SIZE))
pygame.display.set_caption('Baby Snake Game')

# Player and Goal Positions
player_pos = [0, 0]
goal_pos = [360, 360]

# Main game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Clear the screen
    window.fill(BACKGROUND_COLOR)
    
    # Draw the player and the goal
    pygame.draw.rect(window, PLAYER_COLOR, (*player_pos, GRID_SIZE, GRID_SIZE))
    pygame.draw.rect(window, GOAL_COLOR, (*goal_pos, GRID_SIZE, GRID_SIZE))
    
    # Update the display
    pygame.display.flip()

# Quit Pygame
pygame.quit()
sys.exit()
```

### Explanation:
1. **Initialize Pygame:** Sets up the Pygame library.
2. **Constants:** Defines the window size, grid size, and colors for the player and goal.
3. **Display Setup:** Creates the game window and sets its title.
4. **Player and Goal Positions:** Specifies the starting positions for the player and goal.
5. **Main Game Loop:** 
   - Listens for events (e.g., quitting the game).
   - Clears the screen and redraws the player and goal.
   - Updates the display to reflect changes.
6. **Quit Pygame:** Ends the game and closes the window when the game loop exits.

This sets up the basic game world where the player and the goal are displayed in their initial positions. Future milestones will add functionality such as player movement, goal collection, and more complex game mechanics.
 
