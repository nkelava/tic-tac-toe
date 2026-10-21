# TicTacToe

This is a simple Tic Tac Toe game created in C++. I wanted to take a beginner project and play a little bit more with C++ and learn a bit more about Forms, just to get an idea of how they work.

Game screen:

![main](https://user-images.githubusercontent.com/55879009/97782708-59764e00-1b93-11eb-8dd9-322365238615.PNG)


# Layout

As you can see, in the top-left and top-right corners of the screen there is a player "profile" (the player's name and their playing icon/symbol).
Between them, in the middle, there is a game counter that shows how many games have been played so far, and below it is the current score.
The game window is also resizable, although I've set the minimum width and height to match the starting size, so you can't make it any smaller than that.
At the bottom there is a line of text that shows whose turn it is, so players can easily check if they forget.


# Gameplay

The gameplay is the same as in standard Tic Tac Toe. For more info, see https://en.wikipedia.org/wiki/Tic-tac-toe

Two message boxes show up at the end of each round. The first one shows the result of the round: if Player 1 wins, it says "Player 1 is the winner!", and so on.
The second one asks whether you want to start a new game. Clicking "Yes" starts the next game, while clicking "No" closes the game.
