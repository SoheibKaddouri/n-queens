# ♛ N-Queens Solver (BFS Visualizer)

This is an interactive web application that solves and visualizes the classic **N-Queens Problem** using the **Breadth-First Search (BFS)** algorithm. It is implemented purely with **HTML, CSS, and JavaScript**.

The N-Queens problem asks for the number of ways to place $N$ non-attacking queens on an $N \times N$ chessboard.

## 🔗 Demos and Links

| Link Type | URL |
| :--- | :--- |
| **Live Demo** | [https://soheibkaddouri.github.io/n-queens/](https://soheibkaddouri.github.io/n-queens/) |
| **GitHub Repository** | [https://github.com/SoheibKaddouri/n-queens](https://github.com/SoheibKaddouri/n-queens) |

---

## ✨ Features

* **Interactive Solver:** Users can select a board size **$N$ (from 4 to 10)**.
* **BFS Implementation:** Solves the N-Queens problem using a Breadth-First Search approach.
* **Solution Visualization:** Displays all unique solutions found for the given $N$, visualizing each board configuration one after another.
* **Total Count:** Shows the total number of non-attacking queen configurations found.
* **Pure Client-Side:** Built entirely with standard web technologies (HTML, CSS, JavaScript) with no backend dependencies.

---

## 📸 Screenshot

A visual example of the solver in action:


**Note:** The actual path should be adjusted if the image file has a different name or is placed outside the `images` folder. For this example, we assume `images/screenshot.png` is the correct path.

---

## 🛠️ Technology Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Structure and layout of the application. |
| **CSS3** | Styling for the chessboard and interface. |
| **JavaScript (ES6+)** | Core logic for the BFS algorithm and DOM manipulation for visualization. |

---

## 🚀 Getting Started

To run this project locally, simply clone the repository and open the `index.html` file in your web browser.

### Prerequisites

You only need a modern web browser (Chrome, Firefox, Edge, etc.).

### Installation

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/SoheibKaddouri/n-queens.git](https://github.com/SoheibKaddouri/n-queens.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd n-queens
    ```
3.  **Open the file:**
    Open the `index.html` file directly in your web browser.

### Usage

1.  Enter the desired board size $N$ in the input field (must be between 4 and 10).
2.  Click the **"Start BFS"** button.
3.  The application will calculate the solutions and then cycle through the visual display of each valid configuration.

---

## 🧠 Code Overview (N-Queens BFS Logic)

The core logic is contained within the `<script>` tag of the `index.html` file.

The **Breadth-First Search** is implemented using a **queue** (`queue = []`) where each item represents a partial solution (a board configuration up to the current row).

* **`solveBFS(N)`:** The main function that uses a queue to explore the state space. It starts with an empty board and, for each configuration, iterates through all possible safe column placements for the next queen.
* **`isSafe(board, row, col)`:** A helper function that checks if placing a queen at `(row, col)` attacks any previously placed queens (checks column, upper-left diagonal, and upper-right diagonal).
* **`displaySolutions()`:** Handles the presentation of the final solutions, iterating through the `solutions` array with a set delay.
