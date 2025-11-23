# 🐍 Snake Game for Terminal programmed in C++ 

## Overview
This project is a classic **Snake game** implemented entirely in the terminal using C++. The game is designed to run without any graphical interface, representing all elements using text characters. The player controls a snake that moves across the board, consuming food to grow in length while avoiding collisions with walls or its own body.

The main objective is to survive as long as possible while maximizing the score by eating fruits.

---

## Features

### Game Board
- The game board is automatically generated at the start of the program.
- The board size is **20 x 10**, with boundaries represented by `|` and `-`.
- The snake starts **stationary in the center** of the board, represented by `X` for the head and `x` for the body.
- The game only begins moving once the player presses a movement key.

### Movement
- Movement is controlled via keyboard keys (`W`, `A`, `S`, `D`) using the provided `keyboard` header functions (`IsWPressed()`, `IsAPressed()`, `IsSPressed()`, `IsDPressed()`), which detect key presses in real-time.
- The snake moves continuously once it starts.
- The tail follows the head smoothly, and the snake can turn at **90-degree angles**.

### Gameplay
- Fruits appear randomly on the board in empty spaces, represented by `O`.
- Each fruit consumed increases the snake's length by one segment.
- Collisions with the snake's own body or with the board boundaries trigger a **game over**.
- A scoring system is implemented:
  - 1 point per tail segment per frame while the player survives.
  - 15 points for each fruit eaten.
- The current score is displayed continuously above the game board.

## 🧱 Visual example in terminal

```text
+--------------------+
|       O            |
|                    |
|     xxxX           |
|                    |
|                    |
|                    |
|                    |
|                    |
|                    |
|                    |
+--------------------+

O = food  
Xx = snake body
