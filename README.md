# PicnicGo

A terminal-based deck-building card game where you draft the most delicious picnic meal! Inspired by [Sushi Go](https://gamewright.com/pdfs/Rules/SushiGoTM-RULES.pdf), PicnicGo brings strategic card drafting to your command line with colorful ANSI graphics and turn-based multiplayer gameplay.

[Play the original online version here](https://www.freeboardgames.org/en/play/picnicGo)

## Features

- **Local Multiplayer**: 3-5 players on one machine with turn-based privacy
- **Strategic Drafting**: Rotating hands create dynamic decision-making each turn
- **10 Unique Card Types**: Each with distinct scoring mechanics and combos
- **Three-Round Structure**: Accumulate points across rounds with end-game cupcake scoring
- **Colorful Terminal UI**: ANSI color codes bring the picnic to life
- **Fork Mechanic**: Use forks strategically to draft two cards in one turn

## Prerequisites

- Java Development Kit (JDK) 8 or higher
- Terminal with ANSI color support

## Installation & Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/talonlikeaclaw/picnic-go.git
   cd picnic-go
   ```

2. Compile all Java files:
   ```bash
   javac *.java
   ```

3. Run the game:
   ```bash
   java PicnicGo
   ```

## How to Play

### Game Overview

PicnicGo uses a deck of 108 cards containing 10 different picnic treats and forks. Each round, players draft cards from rotating hands to build their meal. After three rounds, the player with the most points wins!

### Game Flow

1. **Setup**: Players enter their names and receive their initial moving hand (7-9 cards depending on player count)
2. **Each Turn**:
   - View your moving hand and current set hand
   - Choose one card to keep (or use a fork to choose two)
   - Hands rotate to the next player
3. **End of Round**: Points are calculated and set hands are discarded
4. **After 3 Rounds**: Cupcake bonuses are applied and the winner is declared

## Card Values & Scoring

### Sandwiches

- **Chicken Sandwich**: 1 point each
- **Pork Sandwich**: 2 points each
- **Beef Sandwich**: 3 points each

### Mayonnaise

- **Effect**: Triples the value of your best sandwich
- You can have multiple mayonnaise cards played
- Only one mayonnaise per sandwich (they don't stack)

### Potato Chips

- Worth 1, 2, or 3 points according to the number shown on the card
- Straightforward scoring with no combos required

### Devilled Eggs

- **Set Scoring**: Each pair (set of 2) is worth 5 points
- Odd eggs score nothing
- You can score multiple pairs in one round

### Fried Chicken

- **Set Scoring**: Each set of 3 is worth 10 points
- Incomplete sets score nothing
- You can score multiple sets in one round

### Pizza

- **Progressive Scoring**:
  - 1 pizza = 1 point
  - 2 pizzas = 3 points
  - 3 pizzas = 6 points
  - 4 pizzas = 10 points
  - 5+ pizzas = 15 points
- You **cannot** score multiple sets (only your first 5 count)

### Cupcake

- Cupcakes are tallied across all 3 rounds
- **End-game scoring**:
  - Player(s) with the **most** cupcakes gain 6 points
  - Player(s) with the **least** cupcakes lose 6 points
  - Ties result in both players receiving the bonus/penalty

### Fork

- Scores no points but provides a powerful ability
- **Effect**: Use during a turn to pick 2 cards instead of 1
- Only one fork can be used per round
- Must have at least one fork in your set hand to use

## Player Count & Hand Sizes

- **3 Players**: 9 cards per moving hand
- **4 Players**: 8 cards per moving hand
- **5 Players**: 7 cards per moving hand

## Technologies Used

- **Java**: Core game logic and object-oriented design
- **ANSI Escape Codes**: Terminal color formatting
- **Scanner**: Console input handling

## Project Structure

```
PicnicGo/
├── PicnicGo.java      # Entry point and main method
├── GameManager.java   # Game flow orchestration
├── Player.java        # Player state and turn logic
├── Deck.java          # Deck initialization and shuffling
├── CardPile.java      # Dynamic array for card collections
├── Card.java          # Individual card wrapper
└── CardType.java      # Enum with all card types and metadata
```

## Author

**Talon Dunbar**
Java II: 210

## License

This project was created as an educational assignment.

## Acknowledgments

- Inspired by [Sushi Go](https://gamewright.com/pdfs/Rules/SushiGoTM-RULES.pdf) by Gamewright
- Original online version: [Free Board Games](https://www.freeboardgames.org/en/play/picnicGo)
