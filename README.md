# BlockFall (Python Edition)

A classic falling blocks game built from scratch in Python with Pygame.

**Play it in your browser:** [raulesteveza.github.io/demos/BlockFall_Python](https://raulesteveza.github.io/demos/BlockFall_Python/) (web version with touch controls, source in [BlockFall_Python_Demo](https://github.com/RaulEstevezA/BlockFall_Python_Demo))

[![Watch the demo on YouTube](https://img.youtube.com/vi/EJYO5XpEWvg/0.jpg)](https://youtu.be/EJYO5XpEWvg)

## Inspiration

The other day, I was watching the movie *Tetris* (2023), which tells the fascinating story behind the discovery of the game and the challenges of obtaining its licensing rights. After finishing the film, I felt the urge to play a classic Tetris game.

I started searching for a legal version online, but most of the ones I found were modern remakes. I really wanted to play the original, classic version. After some time browsing, I thought to myself, *"I'm a programmer, why not build my own version?"* So I opened my laptop, launched Visual Studio Code, and started coding.

I chose **Python** for this project since it's the language I’m most comfortable with. Here's how it came together!

## Technologies Used

- **Python 3.12.6** – Main programming language.
- **Pygame 2.6.1** – For rendering graphics, handling events, and managing game loops.
- **PyInstaller** – To package the game into a standalone executable.
- **Blackhole (macOS)** – To record in-game audio during development.
- **VSCode** – The primary code editor.

## Challenges Faced

- **Key Repeat Logic:** Implementing smooth and responsive key hold functionality for moving and dropping pieces took several iterations to perfect.
- **Scoring System:** Designing a balanced scoring mechanism that factors in both the number of cleared lines and the current level.
- **Instant Drop Feature:** Implementing a "hard drop" that allows the piece to instantly fall to the bottom and lock in place.
- **Game Packaging:** Creating a working `.exe` (and `.app` for macOS) using PyInstaller while ensuring all dependencies, like music and assets, were bundled correctly.

## How to Play

### Objective

Clear as many lines as possible by completing horizontal rows without gaps. The game speeds up as you level up, increasing the challenge.

### Controls

| Action             | Default Key |
|--------------------|-------------|
| Move Left          | Left Arrow  |
| Move Right         | Right Arrow |
| Soft Drop          | Down Arrow  |
| Hard Drop          | Spacebar    |
| Rotate Piece       | Up Arrow    |
| Pause Game         | Esc         |
| Configure Controls | C (in Menu) |
| Start Game         | Enter       |

*Note:* You can reconfigure movement keys in the menu.

### Scoring

The scoring system is based on a combination of lines cleared, level multipliers, and bonus coefficients:

- **Base Formula:** `(10 × number of lines) × (line coefficient × level multiplier)`

- **Line Clear Coefficients:**
  - 1 line → ×1.0
  - 2 lines → ×1.2
  - 3 lines → ×1.6
  - 4 lines → ×2.0

- **Level Multipliers:**
  - Level 1 → ×1.0
  - Level 2 → ×1.1
  - Level 3 → ×1.2
  - … up to Level 10 → ×2.0

You need **300 points** to advance to the next level.

## How to Run

### Run from Source

1. **Clone the repository:**
   ```bash
   git clone https://github.com/RaulEstevezA/BlockFall_Python.git
   cd BlockFall_Python
   ```

2. **Install Dependencies:**
   ```bash
   pip install pygame
   ```

3. **Run the Game:**
   ```bash
   python blockfall.py
   ```

## Audio & Music

- The background music is **Korobeiniki**, a 19th-century Russian folk song in the public domain.
- No third-party recording or arrangement is used: the track is synthesized from scratch by [`tool/generate_music.py`](tool/generate_music.py) using only the Python standard library (`python tool/generate_music.py` regenerates `music/theme.ogg`, it needs ffmpeg).
- Music playback is handled using Pygame's mixer.
- Volume is set to 60% by default but can be adjusted in the source.

## Demo Video

Check out the gameplay demo on [YouTube](https://youtu.be/EJYO5XpEWvg) to see it in action!

## License

This project is for educational and personal use.  
Inspired by the classic falling blocks games, but all code here is original.

BlockFall is a personal project and is not affiliated with, endorsed by or sponsored by The Tetris Company. *Tetris* is a trademark of The Tetris Company, mentioned here only to describe the inspiration behind the project.

## Final Thoughts

This project was a fun dive into game development using Python. It helped me sharpen my skills with Pygame, understand game loop logic, and tackle challenges like input handling, scoring systems, and packaging for distribution.

If you enjoy it, feel free to leave feedback or suggest improvements. Happy stacking!

 **Thanks for playing!** 

