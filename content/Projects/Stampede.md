**Project Overview** Stampede is a console-based chess engine and user interface developed in C#. It is designed to run in a terminal environment, utilizing efficient bitboard representations for game state management and a custom artificial intelligence implementation for move generation. The project demonstrates the application of complex search algorithms, heuristic evaluation, and rich text-based UI rendering without reliance on graphical user interface (GUI) libraries.

**Technical Architecture**

- **Board Representation:** The engine utilizes a bitboard-based approach (using 12 distinct `ulong` bitboards) to represent piece locations. This allows for high-performance bitwise operations to determine board state, attacks, and move validity.
    
- **Move Generation:** Implements a pseudo-legal move generator that handles sliding piece logic via raycasting and pre-calculated attack tables for knights and kings. It fully supports special moves including Castling and En Passant.
    
- **Zobrist Hashing:** The system employs Zobrist hashing to generate unique identifiers for board positions, enabling rapid state comparison and efficient storage in transposition tables.
    

**AI and Search Algorithms** The core intelligence is built upon a Negamax search framework enhanced by several optimization techniques:

- **Alpha-Beta Pruning:** Optimizes the search tree by eliminating irrelevant branches.
    
- **Iterative Deepening:** Progressively searches deeper into the game tree within a defined time limit (defaulting to 2500ms).
    
- **Transposition Table:** Caches previously analyzed positions to prevent redundant calculations.
    
- **Search Extensions & Reductions:** Utilizes Null Move Pruning, Late Move Reduction (LMR), and Principal Variation Search (PVS) to focus resources on the most promising lines.
    
- **Quiescence Search:** Extends the search at leaf nodes to resolve unstable positions (captures) and mitigate the horizon effect.
    
- **Evaluation Function:** A static evaluation system that scores positions based on material weight, Piece-Square Tables (PST), mobility, pawn structure analysis (isolated, doubled, and passed pawns), and king safety.
    
- **Opening Book:** Includes a deterministic opening book for standard lines (e.g., Sicilian, Queen's Gambit).
    

**User Interface (CLI)** The interface is constructed using the `Spectre.Console` library to provide a structured and visual terminal experience:

- **Visual Rendering:** Renders the board using ASCII/text characters with distinct colors for pieces and squares.
    
- **Real-Time Feedback:** Displays a dynamic evaluation bar, move history (PGN format), and system logs during gameplay.
    
- **Interactive Input:** Features a command-line input loop for move entry (algebraic notation) and system commands (resign, restart).
    
- **Animations:** Includes terminal-based animations for "booting" sequences and thinking indicators.

**Tech Stack**

- **Language:** C#
    
- **Framework:** .NET Framework 4.7.2
    
- **Dependencies:** Spectre.Console (for terminal UI rendering)