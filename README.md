# TicTacToe

This is a simple two-player Tic Tac Toe game for Windows, written in C++ with the Win32 API. I wanted to take a beginner project, play a little bit more with C++ and learn how Windows desktop apps work, just to get an idea of how windows, messages and drawing fit together.

Game screen:

![main](https://user-images.githubusercontent.com/55879009/97782708-59764e00-1b93-11eb-8dd9-322365238615.PNG)


## Layout

As you can see, in the top-left and top-right corners of the screen there is a player "profile" (the player's name and their playing icon/symbol). Player 1 plays with X and Player 2 plays with O.
Between them, in the middle, there is a game counter that shows how many games have been played so far, and below it is the current score.
The game window is also resizable, although it can't be made smaller than 600 × 600 pixels.
At the bottom there is a line of text that shows whose turn it is, so players can easily check if they forget.


## Gameplay

The gameplay is the same as in standard Tic Tac Toe. For more info, see https://en.wikipedia.org/wiki/Tic-tac-toe

Players take turns clicking an empty cell on the board, and Player 1 always makes the first move of a game. When a player gets three in a row, the winning line is highlighted.

Two message boxes show up at the end of each round. The first one shows the result of the round: if Player 1 wins, it says "Player 1 is the winner!", and so on.
The second one asks whether you want to start a new game. Clicking "Yes" starts the next game, while clicking "No" closes the game.

The menu bar has a few more options:

- **File → New Game...** shows the same "start a new game?" question.
- **File → Exit** closes the game.
- **Help → About...** shows the version information. You can also open it with **Alt + ?** or **Alt + /**.


## Building

Requirements:

- Windows
- Visual Studio 2019 with the **Desktop development with C++** workload (the project uses the v142 platform toolset and the Windows 10 SDK)

Steps:

1. Clone the repository.
2. Open `TicTacToe.sln` in Visual Studio.
3. Choose a configuration (`Debug` or `Release`) and a platform (`x64` or `x86`).
4. Press **F5** to build and run the game.

If you use a newer version of Visual Studio, either install the v142 build tools from the Visual Studio Installer, or accept the prompt to retarget the project to your installed toolset.


## Project structure

```
TicTacToe.sln          Visual Studio solution
TicTacToe/
├── TicTacToe.vcxproj  Visual Studio project (plus .vcxproj.filters)
├── TicTacToe.cpp      Game logic, drawing and window handling
├── TicTacToe.h        Main header
├── TicTacToe.rc       Resources (icons, menu, About dialog, strings)
├── resource.h         Resource IDs
├── framework.h        Windows and C runtime includes
├── targetver.h        Target Windows version
└── res/               Icons and images referenced by TicTacToe.rc
```
