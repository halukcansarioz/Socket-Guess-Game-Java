
# 🎮 Socket-Guess-Game-Java
### (Number Guessing Game with Server-Client Socket Communication)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)](#)
[![Socket](https://img.shields.io/badge/Socket%20Programming-4D4D4D?style=flat&logo=java&logoColor=white)](#)
[![Made with Learning](https://img.shields.io/badge/Made%20with-Learning-1f425f.svg)](#)

A simple number guessing game built in Java using client/server socket communication. The server generates a random number and the client attempts to guess it within a limited number of tries, receiving real-time feedback after each attempt.

## 📚 Table of Contents
- [About the Project](#about-the-project)
- [Features](#features)
- [How It Works](#how-it-works)
- [Tech Stack](#tech-stack)
- [Installation & Usage](#installation--usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [Contact](#contact)
- [License](#license)

---

## About the Project

This project is a practical implementation of **socket programming** in Java. It demonstrates how a server and a client can communicate over a network using TCP sockets, with the server hosting a number guessing game and the client interacting with it remotely.

- **Developer:** Haluk Can SARIÖZ
- **Type:** Console Application (Server-Client)
- **Purpose:** Learning Java socket programming and network communication

---

## Features

- **Client-Server Architecture:** The server runs the game logic while the client provides the user interface.
- **Random Number Generation:** The server picks a random number between 1 and 10 at the start of each game.
- **Limited Guesses:** The client has a maximum of 3 attempts to guess the correct number.
- **Real-Time Feedback:** After each guess, the server responds with:
  - `Yukselt!` (Go higher!) if the guess is too low
  - `Dusur!` (Go lower!) if the guess is too high
  - `Dogru` (Correct!) if the guess is right
  - `Yanlis - Olmasi gereken rakam: X` (Wrong - the correct number was X) if all attempts are used
- **Input Validation:** Out-of-range numbers (outside 1–10) cause the server to terminate the connection.

---

## How It Works

1. The **server** starts and listens on port `7985`.
2. The **client** connects to the server at `localhost:7985`.
3. The server generates a random number (1–10) and sends an initial prompt to the client.
4. The client prompts the user to enter a guess, which is sent back to the server.
5. The server evaluates the guess and sends a result code:
   - `1` → Correct
   - `2` → Too low (increase)
   - `3` → Too high (decrease)
   - `4` → Game over (out of attempts)
6. The game ends when the client guesses correctly or runs out of attempts.

---

## Tech Stack

| Layer | Technology |
|:-------|:-----------|
| **Language** | Java |
| **Networking** | `java.net.ServerSocket`, `java.net.Socket` |
| **I/O** | `java.io.PrintWriter`, `java.io.BufferedReader`, `java.util.Scanner` |
| **Utilities** | `java.util.Random` |
| **Version Control** | Git & GitHub |

---

## Installation & Usage

### Prerequisites
- [Java JDK 8+](https://www.oracle.com/java/technologies/downloads/)
- Git

### Steps

**1. Clone the repository:**

```bash
git clone https://github.com/halukcansarioz/Socket-Guess-Game-Java.git
```

**2. Navigate to the project directory:**

```bash
cd Socket-Guess-Game-Java
```

**3. Compile both files:**

```bash
javac Server.java Client.java
```

**4. Start the server (in one terminal):**

```bash
java Server
```

**5. Start the client (in another terminal):**

```bash
java Client
```

**6. Play the game:**

Follow the prompts in the client terminal to enter your guesses (1–10).

> ⚠️ **Note:** The server must be started before the client. Both programs run on `localhost` (port `7985`).

---

## Project Structure

```text
Socket-Guess-Game-Java/
├── Server.java           # Server-side game logic
├── Client.java           # Client-side user interface
├── .gitattributes        # Git configuration file
└── README.md             # Project documentation
```

---

## Contributing

Contributions, bug reports, and feature requests are welcome!

1. **Fork** this repository.
2. Create a **Branch** (`git checkout -b feature/NewFeature`).
3. Make your changes and **Commit** (`git commit -m 'Add: New feature'`).
4. **Push** your code (`git push origin feature/NewFeature`).
5. Open a **Pull Request**.

---

<a name="contact"></a>
## Contact

**Haluk Can Sarıöz**

- GitHub: [@halukcansarioz](https://github.com/halukcansarioz)
- Email: [halukcansarioz19@gmail.com](mailto:halukcansarioz19@gmail.com)
- LinkedIn: [Haluk Can Sarıöz](https://www.linkedin.com/in/halukcansarioz)

---

*If you found this project helpful, don't forget to ⭐ it!*

---

## License

This project is licensed under the [MIT License](LICENSE).
