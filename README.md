# Zombie In My Pocket - ONLINE!
Based on https://boardgamegeek.com/boardgame/33468/zombie-my-pocket by Jeremiah Lee

## Rules
- One Tile on table to start
- Take tile off stack
- Place adjacent to existing tile with doorways matching up
- action
  - cower
    - discard dev card (effectively skips turn)
    - regain 3 hp
  - Move to adjacent tile
- draw dev card for current time (if you moved)
  - time increments when dev cards for the hour are used up

# Dev
## IMPORTANT
- E-mail the creator for permission to deploy a non-paper version of their game.

## Tasks
- Create components
  - match JSX to structure of information on game piece
  - create states
  - create functions
  - basic styling
- redux
  - reducers
  - separate container components
  - connect components
- UX review
  - visual design
  - layout
  - animations/feedback
- first demo and playtest

## Major Components
Many of these will need to be further broken down into subcomponents not listed here.
- Dev card
  - 3 decks
    - 9, 10, 11 am
  - 9 cards each deck
  - card has a property one of:
    - item
    - zombies
    - buff
    - debuff
- Tiles
  - Doorways - 0 or 1 per wall
  - Types
    - Interior (8)
      - Kitchen
      - Storage
        - let's you draw another dev card
    - Exterior (8)
      - Patio
- Inventory
  - cannot receive more than one of each kind in a turn
  - Items (3 of each kind)
    - Totem
    - weapons
    - can of soda
      - regain 2 hp

- Player
  - token indicating location
  - hitpoints (6)
    - cannot lose more than 4 per battle
    - subtract number of zombies plus attack
    - lose one if you run away
  - attacks (1)
    - increment when receiving weapon
