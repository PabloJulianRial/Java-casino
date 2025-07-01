# Java Casino

A simple console-based casino simulator in Java featuring 3-Card Poker and Blackjack.

## Features

- **3-Card Poker**  
  - Ante & Pair Plus bets  
  - Dealer qualification rules  
  - Payouts for Pair, Flush, Straight, Three-of-a-Kind, Straight-Flush  

- **Blackjack**  
  - Hit or Stand gameplay against dealer  
  - Ace counts as 1 or 11  
  - Dealer must hit on 16 and stand on 17+  

## Prerequisites

- Java Development Kit (JDK) 8 or higher installed  
- (Optional) Maven or Gradle if you want to integrate a build tool  

## Installation & Build

1. **Clone the repo**  
   ```bash
   git clone https://github.com/PabloJulianRial/Java-casino.git
   cd Java-casino

2. **Compile**  
   ```bash
   javac -d out src/*.java

3. **Run**  
   ```bash
   java -cp out Main.java



## How to Play

### 3-Card Poker

1. **Bet** an ante and/or pair plus.  
2. **Deal**: You and the dealer each get 3 cards, face down.  
3. **Inspect your hand**:
   - **Play**: place a Play wager equal to your Ante.  
   - **Fold**: lose Ante and Pair Plus.  
4. **Dealer Qualifies** on Queen-high or better:
   - If dealer doesn’t qualify, your **Ante pushes** (Play is returned).  
   - If dealer qualifies:
     - **Win**: Ante & Play pay 1:1.  
     - **Lose**: Dealer collects Ante & Play.  
5. **Pair Plus** always pays based on your hand:
   - Pair, Flush, Straight, Three-of-a-Kind, Straight-Flush.

**Winning Hands (best → worst):**  
Straight-Flush > Three-of-a-Kind > Straight > Flush > Pair > High Card

---

### Blackjack

1. **Bet** your chips.  
2. **Deal**: You and the dealer each get 2 cards (your cards face up).  
3. **Player Turn**:
   - **Hit** to take another card.  
   - **Stand** to keep your total.  
   - **Bust** if > 21: you lose immediately.  
4. **Dealer Turn**:
   - Reveal hole card.  
   - Hit on 16 or less.  
   - Stand on 17 or more.  
5. **Payout**:
   - Your total > dealer’s (≤ 21): **Win 1:1**.  
   - **Blackjack** (Ace + 10-value): **Win 3:2**.  
   - **Push**: bet returned.  
   - Else: you lose your bet.

---

## Configuration

Starting credits, bet limits, or other settings can be adjusted in `config.properties` (or by editing the constants in `src/...`, if you haven’t externalized them).  





***PROJECT STRUCTURE***

Java-casino/
├── src/
│   ├── com/pablo/casino/
│   │   ├── CasinoMain.java
│   │   ├── PokerGame.java
│   │   └── BlackjackGame.java
│   ├── model/
│   │   ├── Card.java
│   │   └── Deck.java
│   └── util/
│       └── ConsoleIO.java
├── out/                      ← compiled classes
└── README.md


