# FlipIt

This is a Python project I made while learning Python and GUI development.

## What it does

FlipIt is a fast-paced, memory-matching card game built with a modern desktop interface using CustomTkinter. The objective of the game is simple: flip over hidden cards to find matching emoji pairs. The game shuffles the card deck on launch, tracks your flips, automatically handles match validations, and re-scrambles into a brand-new grid layout the moment you clear the board.

## Features

- **Responsive Grid:** A clean 6x6 layout matrix containing 32 cards (16 matching pairs) that scales smoothly if you resize the window.
- **Dynamic Turn Validation:** Game logic automatically identifies matches, turns successful pairings bright green (`#2ecc71`), and disables them from being clicked again.
- **Visual Memory Pause:** Built-in half-second (`500ms`) display delay when cards mismatch, allowing players a clear opportunity to memorize layouts before the cards turn back face-down.
- **Smart Game Engine Resets:** A robust board-clearing system that purges old game buttons and shuffles fresh pairs completely seamlessly without affecting on-screen text components like the main game title.
- **Victory Alerts:** Seamless integration with desktop notification systems to prompt a victory popup when all 16 pairs are solved.

## What I learned

- How to build a fully dynamic layout by calculating coordinates on-the-fly using integer floor division (`//`) and modulo arithmetic (`%`).
- How to preserve unique element definitions inside loops by utilizing `lambda` arguments with frozen defaults (`lambda btn=card, symbol=symbol:`).
- How to filter through active window interfaces safely using `isinstance()` checks to dismantle buttons while leaving tracking labels unbothered.
- How to enforce immediate graphic loops across delayed function calls by leveraging native `root.update()` and non-blocking `root.after()` intervals.
- How to leverage column and row weighting configurations (`weight=1`) to construct structural, scale-independent, fluid interfaces.

## How to run

1. **Install Python:** Ensure you have Python 3.8 or newer installed on your computer.
2. **Install CustomTkinter:** Open your terminal or command prompt and install the dependencies:
   ```bash
   pip install customtkinter
   ```
3. **Execute App:** Run the python script directly:
   ```bash
   python flipit.py
   ```

## Built With

- **Python** - Core language execution and game condition math.
- **CustomTkinter** - Flat, modern interface wrapping, geometry grid adjustments, and button mechanics.

## Future improvements

- Add a dynamic turn counter to rate player efficiency.
- Build an ongoing score history file tracking your best/fastest clear records.
- Introduce customized card deck sets (e.g., animals, sports icons, flags) chosen through an onboarding screen.
- Implement an option to scale the difficulty grid up or down (4x4, 6x6, 8x8).
