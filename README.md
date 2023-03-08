# Bowling Code Kata
This code kata is aimed to teach the concept of TDD or BDD. In this Kata you will need to implement the logic of counting bowling game rules. 

## General Requirements
1. Write tests first - TDD describes approach where one first write tests and then the code. Below are the summary of the TDD approach. For more details please visit (TDD wiki page)[https://en.wikipedia.org/wiki/Test-driven_development]
    1. Write a single test that checks specific logical requirments
    2. Run tests and observe that it fails
    3. Write the minimum code required for this test to pass
    4. Refactor as necessary
    5. Observe that all tests pass
    6. Repeat...

## Bowling Score Rules
Below are the rules to count score in bowling:
1. Each game lasts 10 turns (or "frames")
1. In each frame the player gets 2 tries to knock down all pins
1. If in 2 tries the player fails to knock down all the pins his score for this specific frame is the number of pins knocked down.
1. If in the second try the played knocked all the pins, this is called a "spare" and his score for **this** frame is 10 + the number of pins knocked down on the next throw (at the next frame)
1. If on the first try in a frame a player knocks down all the pins this is called a "strike". The frame is over and his score for this frame is 10 + the total of his 2 next throws.
1. If player gets "spare" or "strike" at the last (tenth) frame. The player gets to throw one or two more bonus balls, respectively. These bonus throws are taken as part of the same turn. If the bonus throws knock down all the pins, the process does not repeat: the bonus throws are only used to calculate the score of the final frame.
1. The game score is the total of all scores in all frames

## Code Kata Rules
In this code kata you will be required to implement the same logic (and tests) twice. In both cases you will have to start with the class `Game` in which you will have to implement the `beginGame`, the `nextTurn` and the `endGame` functions.

* `beginGame` function receives a names of 2 players and initiates their scores to 0
* `nextTurn` receives the player name and the number of pins the player knocked down. This function calculates automatically the frame (turn) number

### First Implementation
* In the first implementation you will need to implement the logic with TDD approach. Then, you will need to refactor the code and "pull out" the score logic into a new class called `ScoreCalculator`
* All the relevant tests must be moved into a separate test file and broken tests in `Game` class must be fixed.

### Second Implementation
* In this implementation the same must happen in the first step
* Do not pull the tests to a separate file
* Check that all tests still pass

## Discussion
* Did tests tests work in the second implementation after refactor?
* Do you still consider the tests "unit tests" after refactor?
* In your opinion, would it be harder 