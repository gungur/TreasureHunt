# Treasure Hunt Game

## Overview
This Java program implements an interactive "Treasure Hunt" adventure game using the Processing library. The game features clickable objects, draggable items, and interactive clues that guide players through a treasure hunt scenario.

## Features
- Interactive game window with background images
- Clickable objects that provide clues when interacted with
- Draggable objects that can be moved around the screen
- Droppable objects that trigger actions when placed on specific targets
- Game buttons for restarting and taking screenshots
- Object activation/deactivation system for progressive clue discovery

## Class Structure

### Core Classes
1. **TreasureHunt** (Main class)
   - Extends PApplet to create the game window
   - Manages game state and object interactions
   - Handles mouse events and rendering

2. **InteractiveObject**
   - Base class for all interactive game objects
   - Implements Clickable interface
   - Handles mouse interactions and visual representation

3. **DraggableObject**
   - Extends InteractiveObject
   - Can be dragged around the screen with mouse
   - Tracks dragging state and position

4. **DroppableObject**
   - Extends DraggableObject
   - Can be dropped on specific targets to trigger actions
   - Checks for overlaps with target objects

### UI Components
1. **Button**
   - Abstract base class for game buttons
   - Implements visual feedback for mouse hover
   - Handles click events

2. **RestartGameButton**
   - Resets the game state when clicked

3. **ScreenshotButton**
   - Captures and saves the current game screen

### Interfaces
1. **Clickable**
   - Defines common behavior for interactive elements
   - Requires mouse event handling methods

## How to Run
1. Ensure you have Java and the Processing library installed
2. Compile all Java files
3. Run the `TreasureHunt` class (main method)

## Game Mechanics
1. The game loads clues and objects from a configuration file
2. Players interact with objects by clicking or dragging them
3. Some objects activate other objects when interacted with
4. The game progresses as players discover and activate new clues
5. Buttons provide additional functionality (restart, screenshot)

## File Structure
```
src/
├── Button.java              // Base button class
├── Clickable.java           // Interface for clickable objects
├── DraggableObject.java     // Draggable object implementation
├── DroppableObject.java     // Droppable object implementation
├── InteractiveObject.java   // Base interactive object class
├── RestartGameButton.java   // Restart game button
├── ScreenshotButton.java    // Screenshot button
└── TreasureHunt.java        // Main game class
```

## Dependencies
- Processing Core library (included in Processing IDE or available separately)

## Configuration
Game settings and clues are loaded from text files in the `clues` directory. The format is:
- First line: background image filename (without extension)
- Second line: introductory text
- Subsequent lines: object definitions (format described in code comments)

## Known Limitations
- Game window size is fixed at 800x600 pixels
- Requires specific image files in an `images` directory
- Limited error handling for malformed configuration files

## Future Enhancements
- Add sound effects
- Implement scoring system
- Support for multiple levels
- Mobile device compatibility

For more details, refer to the extensive inline documentation in each source file.
