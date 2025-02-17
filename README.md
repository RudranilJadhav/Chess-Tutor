# Ctrl_Shift_Intelligence

## Overview
This project is a **Chess AI Assistant** that leverages **Stockfish** for move calculations and **DeepSeek LLaMA-70B** for in-depth chess explanations. It provides:

- **Best move suggestions** using Stockfish
- **Detailed justifications** for best moves
- **Chess opening theory explanations**
- **Pros, cons, and counter-strategies** for openings

## Features
- **Best Move Evaluation**: Uses Stockfish to analyze a given FEN position and determine the best move.
- **Move Explanation**: Provides a detailed justification for the best move using an LLM-based chat model.
- **Opening Theory Analysis**: Retrieves and explains chess openings based on an ECO code and PGN notation.
- **Opening Strategy Breakdown**: Discusses the pros, cons, and counter-strategies of specific openings.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.x
- Required Python packages
- Stockfish chess engine

### Setup
1. **Clone the Repository**:
   ```sh
   git clonehttps://github.com/RudranilJadhav/Ctrl_Shift_Intelligence.git
   cd chess-ai-assistant
   ```
2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```
3. **Set Environment Variables**:
   Create a `.env` file and add:
   ```
   STOCKFISH_PATH=<path_to_stockfish>
   GROQ_API_KEY=<your_groq_api_key>
   ```

## Usage
### 1. Find the Best Move with Explanation
Run the script and input the **FEN (Forsyth–Edwards Notation)** of the chess position:
```sh
python script.py
```
Example:
```
You: rnbqkb1r/pppppppp/5n2/8/8/5N2/PPPPPPPP/RNBQKB1R w KQkq - 0 1
Bot: The best move is Nxe5, capturing the e5 pawn and gaining center control.
```

### 2. Get Opening Theory Explanation
Input the name of the chess opening:
```
You: Sicilian Defense
Bot: The Sicilian Defense (ECO B40) is an aggressive opening that leads to unbalanced positions...
```

## File Structure
```
chess-ai-assistant/
├── theory/                # Opening theory datasets
│   ├── a.tsv
│   ├── b.tsv
│   ├── c.tsv
│   ├── d.tsv
│   ├── e.tsv
├── script.py              # Main script
├── requirements.txt       # Dependencies
├── README.md              # Documentation
└── .env                   # Environment variables (ignored in .gitignore)
```

## Dependencies
- `python-dotenv`
- `pandas`
- `numpy`
- `stockfish`
- `groq`
- `re`

## Contributing
Feel free to submit **issues, suggestions, or pull requests** to improve this project!

## License
MIT License

