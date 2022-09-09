# internet history trivia pseudo-code

<!-- *I will update the wire-frame, as there are a few elements I'm missing.* -->

## quiz game (basic) requirements

- include 4 categories
- scoring
- score mechanics
- art
- sound
- timer
- separate data file for prompts/answers

## guidelines / rules

- the player has limited amount of time to answer each question
- the player gets a point for each correct answer
- the player loses a life for each incorrect answer
- if the player runs out of lives (amount undecided), the game is over
- if the player answers all the questions right, they win

## pseudo-code

*expanding this further, but here is the introductory pseudo-code to get a sneak peak*

### step 1: define required variables used to track state of the game

- score, number of lives, time remaining, timer id, question index, etc.

### step 2: store cached element references

- buttons (answer, next, reset...), question element, score element, lives element, etc.

### step 3: initialize game state

- score to 0, timer to 0, lives to (?)
- start button

### step 4: when game is not over, render game state

- render the current question, the player's current score, the number of lives the player has remanding

### step 5: define constants

- quesitons, time limits, number of lives, etc.
- questions (array of objects, each representing a question, with properties for the question text, answer choices, and correct answer)

### step 6: handle clicks

- next page
- set off timer
- if the player chooses correct answer, increment score and trigger a sound and color change
- if player choose wrong answer, decrement the lives, there is a color change, trigger a sound
- if timer goes out, they lose a life, and a sound is triggered
- track player progress with a score, and show how many lives the players have remaining
- go to the next quesiton

### step 7: build a winner function

- if player runs out of (?) lives, game over
- if the player answers all the questions right, and didn't die, winner
- winner celebration with sounds, animation, etc.
- reset button

---

### sound effects

  - sound effect for when the player answers a question correctly
  - sound effect for when the player answers a question incorrectly
  - sound effect for when the player wins
  - sound effect for when the player loses- sound effect for when the player