---
layout: post
title: Game of life - FCC Challenge - Part 1
date: 2018-02-16
---

## The problem

There is a "board", kind of a set or a matrix of cells. Each cell is either empty (dead) or full (alive), and has neighbours (adyacent cells: up, down, left, right, corners).

The board starts with an initial configuration of cells (seed) and the following states will derive from applying some simple rules to each cell.

The rules are:

- If the cell is empty and
  - has less than 3 neighbours full, then in the next state of the board remains empty.
  - has exactly 3 neighbours full, then there will be a full cell.
  - has more than 3 full neighbours, it will remain empty.
- If the cell is full and
  - has less than 2 full neighbours, it will become empty.
  - has 2 or 3 full neighbours, it will remain full (survives).
  - has more than 3 full neighbours, then it will be empty next time.

#### What do you need to know of the board, what can you observe from the board? 

Its cells (the dimensions could be deduced from the cells).

#### What do you need to know of the cells?

Its position (which cell it is), its state of emptyness or fullness, its neighbours.

#### How do you create a board? 

You can create the initial board by giving x and y coordinates and the seed (which cells begin full and which empty). I am implying that the board is rectangular.

Then you can get to other state by taking an existing board and applying the rules to each cell.

## User stories:

From [https://www.freecodecamp.org/challenges/build-the-game-of-life](https://www.freecodecamp.org/challenges/build-the-game-of-life)

* [ ] When I first arrive at the game, it will randomly generate a board and start playing.
* [ ] I can start and stop the board.
* [ ] I can set up the board.
* [ ] I can clear the board.
* [ ] When I press start, the game will play out.
* [ ] Each time the board changes, I can see how many generations have gone by.

## Readings

* [Conway's game of life by himself](https://www.youtube.com/watch?v=E8kUJL04ELA) youtube video
* Wikipedia on [Conway's game of life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life)


## La ludo de la vivo

Estas dudimensia, rektangula tabelo dispartigita en kvadrataj ĉeloj. Ĉiu ĉelo povas esti plena aux malplena kaj havas najbaraj ĉeloj (dekstre, maldekstre, supre, malsupre, anguloj).

La ludo komencas kun certa agordo kaj la postaj statoj de ĉiu ĉelo sekvas el tre simplaj reguloj:

- Se la ĉelo estas plena kaj havas malpli ol 2 plenaj najbaroj aux pli da 3 plenaj najbaroj, do poste ĝi malpleniĝos. Se ĝi havas ĝuste 2 aux 3, en la sekvanta vico ĝi restos plena.
- Kiam la ĉelo estas malplena kaj havas pli ol malpli ol 3 aux pli da 3 plenaj najbaroj, ĝi restos malplena. Sed se ĝi havas ĝuste 3 plenaj najbaroj, ĝi fariĝos plena.