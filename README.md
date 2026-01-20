# 🎮 2048 Game — Vanilla JavaScript OOP

![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-yellow?logo=javascript)
![CSS3](https://img.shields.io/badge/CSS3-Grid-blue?logo=css3)
![License](https://img.shields.io/badge/License-MIT-green)

This is a modern implementation of the popular game **2048**. The main feature of the project is the use of **object-oriented approach (OOP)** and classes in pure JavaScript without external libraries.

🚀 **[Live Preview](https://VictorKomara.github.io/2048game/)**

---

## 📸 Screenshots and Audit
<p align="center">
  <img src="./src/images/reference.png" width="400" display="block" alt="2048 game image">
  <img src="./src/images/lighthouse-result.png" width="800" alt="Lighthouse Result">
</p>

---

## ✨ Features

* **OOP Architecture:** The game logic is divided into classes (`Game`, `Cell`, `Tile`), which ensures code cleanliness and ease of maintenance.
* **Dual Input Support:**
    * 💻 **Keyboard:** Arrow control (Up, Down, Left, Right).
    * 📱 **Touch Support:** Implemented swipe handling for mobile gaming.
* **Smooth Animations:** Using CSS Transitions and Keyframes to smoothly move and appear tiles.
* **Dynamic Grid:** Automatic generation of the playing field via JavaScript using CSS Variables.
* **Game Status System:** Condition tracking system: *Idle*, *Playing*, *Win*, *Lose*.
* ♿ **Accessibility:**
    * 100% compliance with standards.
    * Contrast optimized colors for visual accessibility (WCAG AA compliant).
    * Full keyboard navigation and touch-friendly interaction.

---

## 🛠️ Technologies

| Technology | Description |
| :--- | :--- |
| **Vanilla JS** | Using classes, private fields (`#`), asynchronous functions (`async/await`), and modules. |
| **CSS Grid** | Flexible construction of a $4 \times 4$ game grid. |
| **CSS** | Adaptive layout and tile state animations. |
| **HTML5** | Semantic markup using `<header>`, `<main>` and `<footer>`. |

---

## 🏗️ Code architecture

The project is built on three main pillars:
1.  **`Game` Class:** Manages game state, scoring, movement logic, and win/loss checking.
2.  **`Cell` Class:** Responsible for each individual grid cell, its coordinates, and the ability to accept a new tile.
3.  **`Tile` Class:** Controls the visual tile, its value, and its movement animation.

---

## 🧠 Game Logic & Merge Algorithm

The code uses elegant tile moving logic based on grouping cells by rows and columns.

How it works:

1. **Grouping:** Depending on the direction (Up, Down, Left, Right), the playing field is divided into arrays of cells. For example, to move up, we work with columns from top to bottom.

2. **Can Accept:** Each tile has a canAccept(tile) method that checks:

    * Is the cell empty?
    * Or whether the value of the tile in the cell matches the new tile (provided that there has not yet been a "merge" into this cell during this turn).

3. **Asynchronous animation:** Promise.all and waitForTransition() are used to ensure that a new tile only appears after all transition animations have completed.

---

## 🚀 Getting Started

To run the project locally, follow these steps:
1. **Clone the repository:**
```bash
git clone https://github.com/VictorKomara/2048game.git
```

2. **Go to the project folder**
```bash
cd 2048game
```

3. **Install dependencies**
```bash
npm install
```

4. **Start the development server**
```bash
npm start
```
---

## 📱 Responsive Design (Breakpoints)

The interface is optimized for compact display:
* **Container width:** 350px — ideal for mobile devices and desktop browsers.
* **Touch threshold:** 50px — swipe sensitivity threshold to avoid accidental movements.

---

## 📫 Contacts and Feedback
The project was developed as part of my learning journey in web development. I am always open to constructive criticism and interesting suggestions!


GitHub: [@VictorKomara](https://github.com/VictorKomara)

Live Demo: [Play 2048 online](https://VictorKomara.github.io/2048game/)


---

## 📄 License
This project is distributed under the MIT license. You are free to use the code for learning or your own projects.
