# Chess Board Assistant - Deployment Guide

## Files to Upload to GitHub Pages

Upload these 2 files to your GitHub repository:

1. **chess-board-assistant.html** (35KB) - Main application
2. **stockfish.js** (932KB) - Stockfish chess engine from lichess.org

Both files must be in the **same directory**.

## How It Works

- **On file://** → Uses js-chess-engine (fallback, works locally without server)
- **On http://localhost:8000** → Uses Stockfish (grandmaster level, ~3000 ELO)
- **On GitHub Pages** → Uses Stockfish (grandmaster level, ~3000 ELO)

## Features

- ♟️ Play chess against AI (800-2800 ELO range)
- 💡 Hint button shows best move using Stockfish (when available) or js-chess-engine
- 📊 Visual chess board
- 📝 Move history tracking
- 🎯 Move builder with buttons
- ⚙️ Hybrid engine: Stockfish (preferred) with js-chess-engine fallback

## Testing Locally

```bash
cd /path/to/your/repo
python3 -m http.server 8000
# Open: http://localhost:8000/chess-board-assistant.html
```

Check browser console for:
- ✅ `🚀 Attempting to load Stockfish...`
- ✅ `✅ Stockfish loaded! (Grandmaster mode)`

## Backups

- `chess-board-assistant-working.html` - Checkpoint from Sep 29, 2026 (Stockfish working)
- `chess-board-assistant-backup.html` - Pre-Stockfish version (js-chess-engine only)

## Unused Files (Safe to Delete)

- `stockfish-wasm-version.html` - Failed WASM attempt
- `index.html` - Original stub
- `vite.config.js` - From React experiment
