
# Marble & Liquid Sorting Game

A puzzle game where players sort colored marbles into tubes by matching colors. This same game can be changed into a liquid game (switch top right-hand corner).

## Start (nodejs) server
```
npm install express
node server.js
```

## Game objective
Arrange all marbles so that **each of the `N` tubes contains `H` marbles of a single color**, with all tubes filled to capacity.

## Setup
- **Tubes**: `C` identical tubes (each holds max `H` marbles)  
- **Marbles**: `N` distinct colors × `H` marbles per color (total: `N•H` marbles)  
- **Initial State**:  
  - `N` tubes randomly filled with all marbles  
  - `K = C - N` empty tubes  

## Game rules
1. **Valid moves**:  
   - Move the top marble from tube A to tube B if:  
     - Tube B is **empty**, OR  
     - The top marble of tube B **matches the color** of the moved marble.  

2. **Movement options** (configurable):  
   - Move **one marble at a time**, OR  
   - Move **all consecutive same-colored marbles** from the top of a tube in one action.  

3. **Color visibility** (optional gameplay mode):  
   - Only the **top marble** in each tube is visible initially.  
   - Lower marbles are revealed when they become the top marble.  

## Winning condition
The puzzle is solved when **every color occupies exactly one tube** with all `H` marbles. Empty tubes may remain.

## Sources

Based on: [ball sort game](https://github.com/frarosset/ball-sort-game)