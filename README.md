# Java_game_application
# Player.java 
• getName(): Retrieve the player's name. 
• setName(String name): Set the player's name. 
• getGamesPlayed(): Get the number of games played by the player. 
• getTotalMoves(): Get the total number of moves made by the player. 
• incrementGamesPlayed(): Increase the number of games played by the player. 
• incrementTotalMoves(int moves): Increase the total moves made by the player. 
# GamePlayer.java 
• This class implements the Player interface. 
# GuessNumber.java 
• startNewGame(): Start a new game. 
• makeGuess(guess): Make a guess in the game. 
• isGameOver(): Check if the game is over. 
• getWinner(): Get the winner of the game. 
• getGuessResult(guess): Get the result of a guess (e.g., "The number is larger," 
"The number is smaller"). 
# PlayerRepository.java 
• Manages players and their data. 
• Methods: 
• createPlayer(name): Create a new player. 
• getPlayer(name): Get a player by name. 
• savePlayersToFile(): Save player data to a text file. 
# GameController.java 
• Handles HTTP requests and game interactions. 
• Endpoints: 
• /player: Create a player and get player information. 
• /game: Create a game and make moves in the game. 
# Class Interactions 
• Player and GamePlayer handle player-related data and statistics. 
• GuessNumber manages the game logic. 
• PlayerRepository manages player data and file I/O. 
• GameController handles HTTP requests, interacts with PlayerRepository, and 
controls game flow. 
# API Endpoints 
# Base URL: http://localhost:8080 
# Player API 
• Create a Player 
• URL: POST /player 
• Parameters: name (string) - The name of the player. 
• Demo Call: curl -X POST 
"http://localhost:8080/player?name=JhonMartin" 
• Get Player Information 
• URL: GET /player 
• Parameters: name (string) - The name of the player. 
• Demo Call: curl "http://localhost:8080/player?name=JhonMartin" 
# Game API 
• Create a Game 
• URL: POST /game 
• Parameters: playerName (string) - The name of the player who starts the 
game. 
# Demo Call: curl -X POST 
"http://localhost:8080/game?playerName=JhonMartin" 
• Make a Move in the Game 
• URL: PUT /game 
• Parameters: move (int) - The number guessed by the player (0-99). 
• Demo Calls: 
• curl -X PUT "http://localhost:8080/game?move=53" 
• curl -X PUT "http://localhost:8080/game?move=82" 
• curl -X PUT "http://localhost:8080/game?move=6" 
• Get Game Moves 
• URL: GET /game/moves 
• Demo Call: curl "http://localhost:8080/game/moves" 
• Player Information After the Game 
• URL: GET /player 
• Parameters: name (string) - The name of the player. 
• Demo Call: curl "http://localhost:8080/player?name=JhonMartin" 
Notes 
# When checking endpoints in Thunder Client, ensure that the Java application is 
running, and replace localhost:8080 with the actual base URL. 
# Enjoy playing the Number Guessing Game! 
