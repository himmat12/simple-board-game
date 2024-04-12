# Simple board game build in scala (scala-coursework)
This is a simple board game build in scala and was a coursework for Computer Science BSC (Hons) Programming module in Block 3 Year 1.

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Game features](#game-features)
  
### Getting started
- Clone the repository:
```
git clone https://github.com/himmat12/scala-coursework.git
```

### Prerequisites
- get the latest intellij community version IDE
- install "scala" plugin from plugins section of intellij
- open this project and configure the SDK version to `3.3.1` or higher and set your JDK version to 8  or higher
- setup the junit4 library into the project

And finally you are good to go!! 
> If you are struggling to understand my not so good explanation then go through installation guide referenced below in installation section.

### Installation
- here is installation guide to make things easy (https://docs.scala-lang.org/getting-started/intellij-track/getting-started-with-scala-in-intellij.html#installation)

### Game features
- player can move to all directions in board (top, left, right, down)
- player cannot move beyond the board
- player can collect coins which are spread in the board
- player cannot walk through walls
- save the current player position in the board
- player can collect every coins inside the rectangle space created from the saved position to current position by player
> 'S' is saved position, 'W' is walls, 'C' is coins, and 'P' is player in the board
```
   0  1  2  3  4  5  6  7  8  9
 0 .  .  .  .  W  .  .  .  .  .
 1 .  .  .  .  W  .  .  .  .  .
 2 .  .  .  .  W  .  .  .  .  .
 3 .  S  .  .  W  .  .  .  .  .
 4 .  .  .  .  .  .  .  .  .  .
 5 .  .  .  C  .  .  .  .  .  .
 6 .  .  .  .  .  .  .  .  .  .
 7 .  .  .  .  .  C  .  .  P  .
 8 .  .  .  .  .  .  .  .  .  .
 9 .  .  .  .  .  .  .  .  .  .
```
> saved position (1,3) and current position (8,7) in this board creates the rectangle (1,3) top-left angle, (8,3) top right angle, (1,7) bottom-left angle, and (8,7) bottom-right angle as illustrated below:
```
   0  1  2  3  4  5  6  7  8  9
 0 .  .  .  .  W  .  .  .  .  .
 1 .  .  .  .  W  .  .  .  .  .
 2 .  .  .  .  W  .  .  .  .  .
 3 .  S  #  #  W  #  #  #  #  .
 4 .  #  .  .  .  .  .  .  #  .
 5 .  #  .  C  .  .  .  .  #  .
 6 .  #  .  .  .  .  .  .  #  .
 7 .  #  #  #  #  C  #  #  P  .
 8 .  .  .  .  .  .  .  .  .  .
 9 .  .  .  .  .  .  .  .  .  .
 ```
- game engine can suggest moves from player current position to given target position
- game engine can suggest solution to complete the game (this means it can suggest move pattern which collects every coins in the board)


