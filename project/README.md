# Game reversi

#### Video Demo:  <https://youtu.be/oC6HmlYUud8>

#### Description:

This is a game reversi using javascript.

##### [Video Demo](https://youtu.be/oC6HmlYUud8)

##### [Slide](./slide.pdf)

##### Description

This is a reversi using javascript.

It is possible to play human vs machine.

##### How to play

1. Choose first and second player.

you can choose from:

* player: (human)

* CPU(xxx): (machine) machine has some thinking routines.

1. Select move (click mouse at a move position)

1. you can undo and redo, click "[<]", "[>]".

This is a sample play. (animation gif)

* human vs machine
![human vs machine](./images/reversi-001.gif)

* machine vs machine
![machine vs machine](./images/reversi-002.gif)

##### machine thinking routines

| name       | description                                                                           |
| ---------- | ------------------------------------------------------------------------------------- |
| First      | Choose first hand.                                                                    |
| Random     | Choose randomly.                                                                      |
| Gain       | Choose the hand with the most stones that can be flipped.                             |
| Montcarlo  | Select the hand with the highest winning rate after repeating the GAME several times. |
| Negamax(2) | negamax method (depth 2)                                                              |
| Negamax(3) | negamax method (depth 3)                                                              |
| Negamax(4) | negamax method (depth 4)                                                              |
| Negamax(5) | megamax method (depth 5)                                                              |


The lower the routine, the stronger the player. However, it takes a lot of time to make a decision.


##### files

```text
reversi/js
├── Reversi.coffee       # base of game
├── ai_base.coffee       # machine routins
├── ai_first.coffee      # ...
├── ai_gain.coffee       # ...
├── ai_montecarlo.coffee # ...
├── ai_negamax.coffee    # ...
├── ai_random.coffee     # ...
├── main.coffee          # main
└── game.js              # concated all files
```
##### make and run

##### make

```bash
cd reversi
npm install
./node_modules/cake/bin/cake compile
```

##### run

on Mac,

```
open index.html
```

You can start the game by opening index.html in your web browser.

##### memo

There is a lot of information on the web about the riversi game's thought routine.

This project implements only the basic ones in it.

Using machine learning to strengthen the machine side player is one of the most fascinating challenges.

If there is an opportunity, I would like to work on its implementation.

