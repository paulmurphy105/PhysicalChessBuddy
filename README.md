# Chess Board Assistant

A single-file chess application for playing on a physical board with grandmaster-level computer assistance powered by Stockfish.

## Features

- ♟️ Play against AI (800-2800 ELO range)
- 💡 Hint button shows best move using Stockfish
- 📊 Visual chess board (optional)
- 📝 Move history tracking
- 🎯 Move builder with buttons
- ⚙️ Hybrid engine: Stockfish (preferred) with js-chess-engine fallback
- 🚀 Single HTML file - no build step required!

## Perfect for:
- Players who prefer physical boards
- Practicing against different skill levels (800-2800 ELO)
- Learning chess notation
- Quick deployment to GitHub Pages

## Deployment

See [DEPLOYMENT.md](DEPLOYMENT.md) for full instructions.

**Quick start:**
1. Upload `chess-board-assistant.html` and `stockfish.js` to your GitHub repo
2. Enable GitHub Pages
3. Done!

## Local Testing

```bash
python3 -m http.server 8000
# Open: http://localhost:8000/chess-board-assistant.html
```

## How to Use

1. Select your desired computer ELO rating (800 = beginner, 2800 = grandmaster)
2. Choose your color (White or Black)
3. Click "Start New Game"
4. Enter moves in standard notation (e.g., "e4", "Nf3", "O-O")
5. Click the 💡 hint button for best move suggestions
6. Toggle the board view to see the current position

## Move Notation Examples

- Pawn moves: `e4`, `d5`
- Piece moves: `Nf3` (knight to f3), `Bb5` (bishop to b5)
- Captures: `exd5`, `Nxe5`
- Castling: `O-O` (kingside), `O-O-O` (queenside)
- Pawn promotion: `e8=Q` (promote to queen)
- Check/Checkmate indicators: `Qh5+` (check), `Qh7#` (checkmate)

## Tech Stack

- **Single HTML file** - Vanilla JavaScript, no framework
- **Chess Engine**: Stockfish (lichess.org build) with js-chess-engine fallback
- **Chess Logic**: chess.js (loaded from CDN)
- **Deployment**: Works on any static host (GitHub Pages, Netlify, etc.)
