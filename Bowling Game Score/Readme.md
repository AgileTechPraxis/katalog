
---
![](../kata.png)

## Bowling Game Scoring

Write a program to calculate the score of a game of Ten-Pin Bowling.

***Input***: a string representing a bowling game score (* scoring rules following).

***Output***: the score as integer.

***Conventions***:

* `X` indicates a strike

* `/` indicates a spare

* `-` indicates a miss

* `|` indicates a frame boundary

* The characters after the `||` are bonus balls


#### Examples

> Examples:
>
> score string | total
> --- | ---
> `"X|X|X|X|X|X|X|X|X|X||XX"` | **300** [10 frames x 30]
> `9-|9-|9-|9-|9-|9-|9-|9-|9-|9-||` | **90** [10 frames x 9]
> `5/|5/|5/|5/|5/|5/|5/|5/|5/|5/||5` | **150** [10 frames x 15]
> `X|7/|9-|X|-8|8/|-6|X|X|X||81` | **167**

#### Scoring Rules

- Each game, or "line" of bowling, includes ten turns, or "frames" for the bowler.
- In each frame, the bowler gets up to two tries to knock down all ten pins.
- If the first ball in a frame knocks down all ten pins, this is called a "strike". The frame is over. The score for the frame is ten plus the total of the pins knocked down in the next two balls.
- If the second ball in a frame knocks down all ten pins, this is called a "spare". The frame is over. The score for the frame is ten plus the number of pins knocked down in the next ball.
- If, after both balls, there is still at least one of the ten pins standing the score for that frame is simply the total number of pins knocked down in those two balls.
- If you get a spare in the last (10th) frame you get one more bonus ball. If you get a strike in the last (10th) frame you get two more bonus balls.
- These bonus throws are taken as part of the same turn. If a bonus ball knocks down all the pins, the process does not repeat. The bonus balls are only used to calculate the score of the final frame.
- The game score is the total of all frame scores.
