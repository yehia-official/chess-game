
A complete and interactive chess game developed with React, Next.js and shadcn/ui. The game offers a player vs player mode and a mode against artificial intelligence.

### 📋 Features

#### Complete Game Rules

- ✅ All piece movements (pawn, knight, bishop, rook, queen, king)
- ✅ Special rules:
  - Castling (kingside and queenside)
  - En passant
  - Pawn promotion
- ✅ Check, checkmate, and stalemate detection
- ✅ Draw rules:
  - Threefold repetition
  - 50-move rule
  - Insufficient material
  - Mutual agreement

#### Game Modes

- 🎮 **Player vs Player Mode**: Two players on the same device
- 🤖 **AI Mode**: 6 difficulty levels (400 to 2500 Elo)
  - LN Beginner (400 Elo)
  - LN Amateur (800 Elo)
  - LN Intermediate (1200 Elo)
  - LN Advanced (1600 Elo)
  - LN Expert (2000 Elo)
  - LN Master (2500 Elo)

#### Game Variants

- ♟️ **Standard Chess**: Classic game with traditional starting position
- 🎲 **Chess960 (Fischer Random)**: Random starting position among 960 possibilities
  - Automatic generation according to FIDE rules
  - King placed between the two rooks
  - Bishops on opposite-colored squares
  - Adapted castling with final destinations identical to classical chess
  - Complete documentation: [CHESS960.md](./CHESS960.md)

#### User Interface

- 🎨 Minimalist design inspired by chess.com
- 🎨 **16 customizable color themes**
- 🎭 **3 piece styles** (Classic, Modern, Colorful)
- 📱 Responsive (mobile, tablet, desktop)
- 🎯 Visual indicators for possible moves
- 🔴 Check highlighting
- 📊 Game information display
- 📜 Move history in FIDE algebraic notation
- 💾 PGN export (FIDE standard format) with clipboard copy
- 🎮 Game controls (new game, resign, draw offer)
- ⏱️ **Chess clock** with multiple time controls
- 🔊 **Sound effects** (move, capture, check, victory)
- ✨ **Smooth animations** for piece movements
- 🌐 **Bilingual interface** (French / English)
- 🎬 **Victory animation** on checkmate

#### Customization

- 🎨 16 pre-defined color themes
- 🎭 3 piece styles to choose from
- ⏱️ 6 different time controls
- 🔊 Volume control
- 💾 Automatic preference saving

### 🛠️ Technologies Used

- **Next.js 15** - React Framework
- **TypeScript** - Static typing
- **Tailwind CSS** - Styling
- **shadcn/ui** - UI components
- **Lucide React** - Icons
- **Zustand** - State management
- **next-intl** - Internationalization
- **Motion** - Animations

### 📥 Installation

1. Clone the project

```bash
cd chess-game/
```

2. Install dependencies

```bash
npm install
```

3. Start the development server

```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

### 🎮 How to Play

1. Choose your game mode (PvP or vs AI)
2. If playing against AI, select the difficulty level
3. White always starts first
4. Click on a piece to select it
5. Valid moves are indicated by circles
6. Click on a valid square to move the piece
7. The game automatically detects checks, checkmates, and stalemates
8. Customize the board with 16 available color themes
9. Choose from 3 different piece styles
10. Export your game in PGN format to save or share it

### 📂 Project Structure

```
chess-game/
├── app/                      # Next.js pages
├── components/               # React components
│   ├── AIDifficultySelector.tsx # AI difficulty selector
│   ├── AnimatedPiece.tsx    # Piece animations
│   ├── BoardContainer.tsx   # Board container
│   ├── CapturedPieces.tsx   # Captured pieces
│   ├── CheckmateAnimation.tsx # Checkmate animation
│   ├── ChessBoard.tsx       # Chess board
│   ├── ChessClock.tsx       # Chess clock
│   ├── ChessGame.tsx        # Main component
│   ├── ChessPiece.tsx       # Chess piece
│   ├── ChessSquare.tsx      # Individual square
│   ├── ExportPGNDialog.tsx  # PGN export dialog
│   ├── FullscreenButton.tsx # Fullscreen button
│   ├── GameControls.tsx     # Game controls
│   ├── GameInfo.tsx         # Game information
│   ├── GameModeSelector.tsx # Mode selector
│   ├── LanguageSelector.tsx # Language selector
│   ├── MoveHistory.tsx      # Move history
│   ├── PieceStyleSelector.tsx # Style selector
│   ├── PreferencesDialog.tsx # Preferences dialog
│   ├── PromotionDialog.tsx  # Promotion dialog
│   ├── SoundControl.tsx     # Sound control
│   ├── ThemeSelector.tsx    # Theme selector
│   ├── TimeControlSelector.tsx # Time control selector
│   └── ui/                  # shadcn UI components
├── lib/                     # Game logic
│   ├── chess-ai.ts          # Artificial intelligence
│   ├── chess-engine.ts      # Game engine
│   ├── chess-sounds.ts      # Sound effects
│   ├── chess-themes.ts      # Color themes
│   ├── chess-utils.ts       # Utility functions
│   ├── constants.ts         # Game constants
│   ├── export-utils.ts      # Export utilities
│   ├── pgn-utils.ts         # PGN utilities
│   ├── piece-styles.ts      # Piece styles
│   ├── preferences.ts       # Preferences management
│   ├── time-controls.ts     # Time controls
│   └── utils.ts             # General utilities
├── store/                   # Zustand state management
├── types/                   # TypeScript types
│   └── chess.ts            # Chess game types
├── messages/               # Translations
│   ├── en.json            # English
│   └── fr.json            # French
├── public/                 # Static files
│   └── pieces/            # SVG piece images
├── README.md              # Main documentation
├── QUICK-START.md         # Quick start guide
├── RULES.md              # Complete rules
├── PGN-NOTATION.md       # PGN format and notation
└── THEMES.md             # Color themes
```

### 🎯 Implemented Rules

All official FIDE (International Chess Federation) rules are implemented:

- All piece movements according to official rules
- Castling (with condition checking)
- En passant capture
- Pawn promotion (choice between queen, rook, bishop, knight)
- Check and checkmate
- Stalemate
- Draw by threefold repetition
- Draw by 50-move rule
- Draw by insufficient material
- Resignation and draw offer

### 💻 Development

#### Available Commands

```bash
npm run dev      # Start development server
npm run build    # Build for production
npm run start    # Start production server
npm run lint     # Lint code
```
