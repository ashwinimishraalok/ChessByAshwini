# ChessByAshwini
A two player chess game in java

System Requirements:

We’ll focus on the following set of requirements while designing the game of chess:

The system should support two online players to play a game of chess.

All rules of international chess will be followed.

Each player will be randomly assigned a side, black or white.

Both players will play their moves one after the other. The white side plays the first move.

Players can’t cancel or roll back their moves.

The system should maintain a log of all moves by both players.

Each side will start with 8 pawns, 2 rooks, 2 bishops, 2 knights, 1 queen, and 1 king.

The game can finish either in a checkmate from one side, forfeit or stalemate (a draw), or resignation.


Use case diagram:

We have two actors in our system:

Player: A registered account in the system, who will play the game. The player will play chess moves.
Admin: To ban/modify players.
Here are the top use cases for chess:

Player moves a piece: To make a valid move of any chess piece.
Resign or forfeit a game: A player resigns from/forfeits the game.
Register new account/Cancel membership: To add a new member or cancel an existing member.
Update game log: To add a move to the game log.

![chess_UseCase_Diagrampng](https://user-images.githubusercontent.com/46497650/122637112-8bc8c180-d10a-11eb-85a5-255cfe2750c0.png)

Class diagram
Here are the main classes for chess:

Player: Player class represents one of the participants playing the game. It keeps track of which side (black or white) the player is playing.

Account: We’ll have two types of accounts in the system: one will be a player, and the other will be an admin.

Game: This class controls the flow of a game. It keeps track of all the game moves, which player has the current turn, and the final result of the game.

Box: A box represents one block of the 8x8 grid and an optional piece.

Board: Board is an 8x8 set of boxes containing all active chess pieces.

Piece: The basic building block of the system, every piece will be placed on a box. This class contains the color the piece represents and the status of the piece (that is, if the piece is currently in play or not). This would be an abstract class and all game pieces will extend it.

Move: Represents a game move, containing the starting and ending box. The Move class will also keep track of the player who made the move, if it is a castling move, or if the move resulted in the capture of a piece.

GameController: Player class uses GameController to make moves.

GameView: Game class updates the GameView to show changes to the players.

![chess](https://user-images.githubusercontent.com/46497650/122637203-f24ddf80-d10a-11eb-889c-ffe5c20f521a.png)




