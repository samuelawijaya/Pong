# 🕹️ Perpetual Pong
This project is a dynamic, terminal-based implementation of **Pong**, developed in **C++**. Built for continuous gameplay, it features real-time motion, dynamic difficulty scaling, and responsive keyboard input — all rendered in the console using ASCII characters.

Inspired by classic Pong mechanics but enhanced for long-term playability, the game ramps up challenge by shrinking the paddle and adding more balls as the player scores.

---

## 🎮 Features

- **Real-Time Paddle & Ball Physics**  
  Simulates smooth motion using a time-stepped update system.

- **Dynamic Difficulty**  
  The paddle shrinks and new balls spawn as your score increases.

- **Multi-Ball Collision Detection**  
  Supports simultaneous bouncing, overlap detection, and response.

- **ASCII-Based Rendering**  
  Uses a 2D character buffer to display the paddle, balls, and game field.

- **Non-blocking Keyboard Input**  
  Responsive key controls using custom input handler.

---

## 🧠 Technical Highlights

- **Language**: C++
- **Rendering**: ASCII console rendering using frame buffers
- **Motion**: Updated at 5000 simulation steps per frame for smoothness
- **Input**: Real-time keyboard polling with `getchar()` and `termios`
- **OOP Design**:
  - Polymorphic `overlap()` method for `Ball–Ball` and `Ball–Player` interaction
  - Modular classes: `Ball`, `Player`, `Screen`, `Globals`, `IO`
  - Clean separation between game logic, drawing, and input

---


The player starts with one ball. Every **5 points**, a new ball is introduced, and every **2 points**, the paddle shrinks slightly to increase difficulty.

---

## 📁 Project Structure

| File          | Purpose                                 |
|---------------|------------------------------------------|
| `main.cpp`    | Game loop and gameplay logic             |
| `Ball.*`      | Ball movement, physics, and collision    |
| `Player.*`    | Paddle movement and collision detection  |
| `Screen.*`    | Frame buffer and ASCII rendering engine  |
| `io.*`        | Keyboard input handler (non-blocking)    |
| `Globals.h`   | Shared constants and config              |

---

## 📷 Gameplay

![Gameplay](https://drive.google.com/file/d/1-W72vM9GKahwqG_QvDQsyeDjl3d3hdLf/view?usp=sharing)
