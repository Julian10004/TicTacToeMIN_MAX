# TicTacToeMIN_MAX
An implementation of the min-max algorithim with two agents playing a game of Tic Tac Toe


# 🎮 Tic-Tac-Toe AI (Minimax Algorithm)

## 📌 Overview

This project implements a fully automated Tic-Tac-Toe game using the **Minimax algorithm**, a fundamental concept in artificial intelligence and game theory.

Two AI agents play against each other:

* **X (Maximizer)** → tries to maximize the score
* **O (Minimizer)** → tries to minimize the score

The algorithm evaluates all possible game states and always chooses the optimal move.

---

## 🧠 Minimax Algorithm Explained

Minimax works by exploring the full game tree recursively:

* Simulate all possible future moves
* Evaluate terminal states (win, loss, draw)
* Propagate values back up the tree

### 🎯 Scoring System

| Outcome | Score |
| ------- | ----- |
| X wins  | +10   |
| O wins  | -10   |
| Draw    | 0     |

### 🔁 Decision Logic

* X chooses the **maximum** value
* O chooses the **minimum** value

---

## 🏗️ Project Structure

The implementation is built around a single class:

### `TicState`

Represents the current game state.

#### Attributes:

* `state` → 3×3 board
* `actions` → available moves
* `turn` → current player (`0 = X`, `1 = O`)

---

## ⚙️ Key Methods

### 🎲 `RandomLoc()`

Chooses a random starting move.

---

### 📋 `TakeAction(action)`

* Updates the board
* Removes move from available actions

---

### 🌳 `Next_States()`

Generates all possible next states:

```python
[(next_state, action), ...]
```

---

### 🧮 `value()`

Core Minimax function:

* Returns score for terminal states
* Recursively evaluates future states

---

### 🔼 `max_algo()`

Returns the maximum value from child states.

---

### 🔽 `min_algo()`

Returns the minimum value from child states.

---

### 🤖 `ChooseAction()`

Selects the best move using Minimax.

---

### 🏁 Game State Checks

* `IsWin()` → checks if a player has won
* `IsComplete()` → checks if board is full

Helper functions:

* `Row_Same()`
* `Col_Same()`
* `Diag_Same()`

---

### 🖥️ `DisplayBoard()`

Prints the board:

```
X O -
- X -
- - O
```

---

### ▶️ `PlayGame()`

Runs the full game loop:

1. Random starting move
2. Alternate Minimax decisions
3. Print board after each move
4. Stop on win or draw

---

### 🔄 `ResetGame()`

Resets the game to initial state.

---

## ▶️ How to Run

```python
game = TicState()
game.PlayGame()
game.ResetGame()
```

---

## 📌 Example Output

```
X - -
- - -
- - -

X O -
- - -
- - -

X O X
- O -
- - -
```

---

## ⚠️ Limitations

* ❌ No alpha-beta pruning (inefficient for larger games)
* ❌ First move is random (not optimal strategy)
* ❌ No human interaction (AI vs AI only)
* ❌ No caching/memoization

---

## 🚀 Future Improvements

* ✅ Add alpha-beta pruning
* ✅ Human vs AI mode
* ✅ GUI (Tkinter / Pygame)
* ✅ Memoization for faster evaluation
* ✅ Smarter opening move (center/corners)

---

## 📚 Concepts Used

* Minimax Algorithm
* Recursion
* Game Trees
* Adversarial Search
* State Space Exploration



