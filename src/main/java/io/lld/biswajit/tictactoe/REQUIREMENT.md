## Design a tic tac toe game

### Must Have Requirements
- it's single game with nxn board
- there are minimum 2 players and maximum n-1 player
- each player uses a unique symbol
- there can be different strategies to win, and it can be a combination of multiple strategies e.g. - row, column, diagonal, corner
- a randomized draw chooses the order in which players will play and that order will be maintained throughout the game
- the game has only one bot
- the difficult level of the bot will be taken as an input. options - easy, medium, hard
- there can be different strategies to decide the winner. the strategy in the problem statement is that the game ends as soon as someone wins or there is a draw
- only the latest move can be undone. so it should have a global undo feature
- a cell can have any of the 3 states - blocked, filled and empty

### Requirements Not needed now
- no timer
- no tournament
- players can't pause, pass or exit
- a player can take any amount of time to make their move


### System behaviour
- how to decide whose turn comes next
- when is the game over
- what does winning the game mean
- when does the game start
- how many undo can be done

### Approach
- list the nouns/ entities involved in the game
- start from outside in

### Entities involved
- Game
  - board
  - a list of players
  - a list of moves
  - state of the game
  - next player to make the move
- Board
  - list of cells (nxn matrix)
- Player
  - name
  - symbol
  - type
- Cell
  - player
  - position
- Position
  - row
  - column
- Cell state
  - empty
  - filled
  - blocked
- Player type
  - human
  - bot
- Bot difficulty level
  - easy
  - medium
  - hard
- Move
  - Player
  - Cell

### Design patterns
- game is created through builder pattern
- winning strategy is poly-morphed through strategy pattern
- bot playing strategy is poly-morphed through strategy pattern
- the strategies can be chosen through factory pattern
- Game can be notified about the move through observer pattern
- 