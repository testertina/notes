# Sudoku

## How to play

* Choose between basic, intermediate or hard.  There are two games for each difficulty.  Timer.
* Click the blank square you would like to fill and select the number you would like to fill it with.
* Can click for hints.
* Can click to see how you are doing? The PC will tell you what is incorrect.
* 


## Logic

* The title screen needs to load.
* Button for difficulty.
* Swipe homescreen up and load game. I.e. if basic is selected give options for basic I or II.
* User must be able to click a box and have an option of numbers between 1 to 9.
* There must be buttons for hints.
* Users must be able to check whether they are right or not. Button to check if they are on track.
* When the user is done they need to be able to click an I'm done button that checks whether they have succeeded.
* If they have succeeded, then display player wins would you like to play basic II or return to homescreen to change difficulty.
* Scoreboard so user can add their name to input their time it took to solve.  So we can create a leaderboard.

### HTML

Homepage

* Sudoku title.
* Instructions button - pop up with instructions.
* Difficulty button - Pop up with basic I or Basic II, intermediate I or II or hard I or II buttons.

Gamepage

* Large square div that contains 9 mini divs, which each contain 9 mini divs.
* Each div filled with numbers.
* Timer
* Buttons: How am I doing? Hint/Reveal a random number? I'm done?

### Javascript and jQuery

* Event handlers for buttons.
* Change colour of boxes.

# Asteroids

## How to play

* Start as a spaceship in the center of the screen, as asteroids approach you must click on them to disintergrate them.
* Your XP and points boost with each destroyed asteroid.
* Once XP bar is filled, the speed of the asteroids increase in the next round.
* Third round the size of the asteroid decrease/vary. Speed remains the same as round 2.
* Fourth round the speed of the asteroids increase.
* Fifth round you get asteroids and comets/space junk. 
* At the end of the game the users points get added to the leaderboard.

## Logic

* The title screen needs to load.
* Buttons for begin game, how to play, leaderboard.
* Swipe homescreen up and load game if begin game is selected.
* On gamepage there should be an XP bar and a points bar which increase with each asteroid.
* Player must be able to click on the asteroids and it should explode.  
* If the asteroid reaches the player then it is game over.
* If the player sucessfully destroys all asteroids in the round then the XP bar is filled and they move on to the next round where the XP bar resets.
* At the end of the game user should be prompted with a scoreboard so user can add their name to input their time it took to solve.  So we can create a leaderboard.


### HTML

Homepage

* Asteroids title (div h1)
* Begin game button - pop up with gamepage. (div h2)
* Instructions button - pop up with instructions. (div h2)
* Leaderboard button to check high scores. (div h2)

Gamepage

* Background set to image
* Spaceship (div)
* 12 asteroids coming in sporadically (divs)
* XP bar (div)
* Points bar (div)
* Quit button (returns to homepage)

Instructions

* Background set to image
* Instructions title (div h1)
* Instructions text (div h2)
* Begin game button (div)
* Back to homepage button (div)

Leaderboard

* Leaderboard title (div h1)
* Array containing inputted user names and corresponding scores. (Array)
* Back to homepage button (div).

### CSS


### Javascript and jQuery

Homepage

* Load page
* Event handlers for begin game button, instructions button and leaderboard button


Gamepage

* set Interval 12 asteroids coming in sporadically (divs)
* setInterval XP bar (div)
* setInterval Points bar (div)
* Event handler Quit button.
* Click event handler which use explosion gif when asteroids are clicked.

Instructions

* Event handler begin game button (div)
* Event handler back to homepage button (div)

Leaderboard

* Append: Array containing inputted user names and corresponding scores. (Array)
* event handler back to homepage button (div).

# Pairs

## How to play

* Choose between basic, intermediate or hard.  There are two games for each difficulty.  
* Timer starts when first card is selected.
* Basic: 20 cards, Intermdiate: 40 cards and hard: 80 cards.
* Match the paired cards.

## Logic

* The title screen needs to load.
* Button for difficulty.
* Swipe homescreen up and load game. I.e. if basic is selected load 20 randomly shuffled cards (10 pairs).
* Player must be able to click card and it should turn around and reveal itself.  When the player selects the second card, if they match it should stay turned around otherwise both cards should turn around after a delay.
* Once all pairs are found the player should know they have won.
* Scoreboard so user can add their name to input their time it took to solve.  So we can create a leaderboard.
