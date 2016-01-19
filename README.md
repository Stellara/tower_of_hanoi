# tower_of_hanoi
A breakable toy to practice principles of OO Design as laid out in [Practical Object Oriented Design](http://www.poodr.com/) by Sandi Metz.

## Rules of the Game:
- Move all the pieces from Tower 1 to Tower 3.
- You can only move one disc at a time.
- You can never put a big disc on top of a smaller one.

## Player Stories:
- When a player starts a new game, the player may choose the number of discs they would like to solve for.
- A player will be given the games rules on start.
- A player may see the game rules whenever they type the command.
- A player may restart or quit the game whenever they wish to.
- A player has solved the puzzle when Tower 3 holds the starting number of discs.
- A player will know how many moves they have used.
- A player will be told as soon as they have surpassed minimum moves to solve, so they may restart if they wish.
- A player will know how much time they are taking.
- A player will know as soon as they have solved the puzzle.
- A player will know if they solved the puzzle in the minimum amount of moves or higher or lower(!).

## Game Stories:
- The timer will continue to run as long as the player has not quit, restart, or solved the puzzle.
- The game will validate each placement of disc.
- The game will verify solved status when the third tower has a size equal to the starting discs.
  - Only required at this step because the placement logic will not allow for anything else

## Features:
- towers
  - have a position
  - hold discs
- discs
  - have a position
  - have a size
- placing discs
- validating disc placement
- basic graphic representation of towers and discs
- check for solved status (placement checking algorithm)
- ability to restart or quit a game
- game loop that runs until, quit, restart, or solve

### Extras:
- counting moves
- timer
- variable tower sizes
- calculate minimum moves per tower size
- score player moves against minimum moves

## Specs:
- adding a disc to a tower registers as added
- removing a disc from a tower registers as removed
- only one disc may be moved at a time
- >1 disc may not be moved
- smaller discs can be placed atop larger discs
- larger discs cannot be placed atop smaller discs
