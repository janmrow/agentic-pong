# Product specification

## Purpose

Build a minimal desktop-browser Pong game: one player against one computer opponent.

The game should be immediately understandable, visually coherent, responsive, and deliberately small in scope. The project exists primarily as a high-quality workload for an agentic software-engineering workflow.

## Experience goals

The game should feel:

* immediate;
* crisp;
* calm;
* responsive;
* deliberately retro rather than decorative or nostalgia-heavy.

Nothing should distract from the paddle-and-ball interaction.

Difficulty should feel progressively more challenging without feeling erratic or unfair.

## Gameplay

* The player controls one paddle.
* The computer controls the opposing paddle.
* One ball moves continuously between both sides.
* Paddles and arena boundaries affect the ball in a predictable way.
* Missing the ball immediately ends the game.
* The game ends after that single miss; there is no multi-round score.
* The result clearly identifies whether the player or computer won.
* The player can start another game without reloading the page.

## Controls

* Desktop browser is the target environment.
* The player's paddle follows vertical mouse or pointer movement within the arena.
* Input should feel direct and smooth.

## Difficulty

The player can choose:

* Easy
* Medium
* Expert

All three modes use the same rules and gameplay.

Higher difficulty increases challenge through:

* higher ball speed;
* stronger computer-paddle performance.

Difficulty must not introduce separate game modes, rules, or feature sets.

## Game states

The product has three primary states:

1. menu;
2. playing;
3. game over.

Keep state transitions obvious and minimal.

## Visual direction

Use a restrained retro style:

* simple geometric shapes;
* high contrast;
* limited color palette;
* clean typography;
* smooth motion;
* no decorative animation;
* no external visual assets unless clearly justified.

The interface should look intentional and cohesive rather than feature-rich.

## Non-goals

Do not add:

* multiplayer;
* sound;
* music;
* accounts;
* persistence;
* multi-round scoring;
* levels;
* achievements;
* settings;
* analytics;
* backend services;
* mobile-specific controls;
* unnecessary visual effects.

## Acceptance criteria

The product is complete when:

* it runs in a current desktop browser;
* the player can choose Easy, Medium, or Expert;
* mouse or pointer movement controls the player paddle;
* the computer paddle behaves consistently with the selected difficulty;
* the ball interacts correctly with paddles and arena boundaries;
* missing the ball ends the game;
* the result is clearly displayed;
* another game can be started without a page reload;
* higher difficulty produces observably stronger opposition;
* motion feels smooth during normal play;
* the visual result matches the defined retro, minimal direction;
* no non-goal features are present.
