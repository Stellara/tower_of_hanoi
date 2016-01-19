# tower_of_hanoi
A breakable toy to practice principles of OO Design as laid out in [Practical Object Oriented Design](http://www.poodr.com/) by Sandi Metz.

## Rules of the Game:
- Move all the pieces from Tower 1 to Tower 3.
- You can only move one disc at a time.
- You can never put a big disc on top of a smaller one.

## Player Stories:
- A player will:
  - choose the number of discs they would like to solve for.
  - know how many moves they have used.
  - be told as soon as they have surpassed minimum moves to solve, so they may restart if they wish.
  - know how much time they are taking.
  - solve the puzzle when Tower 3 holds the starting number of discs.
  - will know as soon as they have solved the puzzle.
  - if they solved the puzzle in the minimum amount of moves or higher or lower(!).

- A player may:
  - see the game rules whenever they type the command.
  - restart or quit the game whenever they wish to.
  - play as many games as they would like to.
  - choose for the game to select a random number of discs to start with.


## Game Stories:
- A game will:
  - output the game rules on start.
  - validate each placement of disc.
  - verify solved status when the third tower has a size equal to the starting discs.
    - * Only required at this step because the placement logic will not allow for anything else*

## Timer Stories:
- A timer will
  - display the current amount of time to the player.
  - start when a new game starts.
  - stop when a game is quit.
  - stop when a game is restarted and clear its time.
  - continue to run as long as the player has not quit, restart, or solved the puzzle.


## Features:
- start a new game
  - see welcome output
  - see rules output
- game loop that runs until quit, restart, or solve
  - basic graphic representation of towers and discs
  - place one disc at a time
  - disc placement validation
    - error sound and message when the disc is bigger than the one below it
  - check for solved status (placement checking algorithm)
  - update graphical representation

- towers
  - have a position
  - hold discs

- discs
  - have a position
  - have a size

- timer
- placement validator
- move counter
- move scorer (against minimum)

## Specs:
- adding a disc to a tower registers as added
- removing a disc from a tower registers as removed
- only one disc may be moved at a time
- >1 disc may not be moved
- smaller discs can be placed atop larger discs
- larger discs cannot be placed atop smaller discs
