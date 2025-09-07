🎮 5-Day Python Pygame Zero Project: Side-Scroller Builder
Create simple side-scrolling screens where you control a character and interact with moving objects!
---
### Day 1: Moving Your Hero
1.  Open your `game.py` file.
2.  Set `WIDTH = 800` and `HEIGHT = 600` at the top.
3.  Create your `player = Actor('alien')` below that.
4.  Write an `update()` function to make your `player` move left when `keyboard.left` is pressed, and right when `keyboard.right` is pressed.
5.  *Hint:* Change `player.x` inside `update()`.
---
### Day 2: Collecting a Star
1.  Add a new `Actor` named `star = Actor('star')` to your `game.py` file. (You'll need an empty `star.png` file in your `images` folder).
2.  Place your `star` at a starting position, like `star.x = 600`.
3.  Inside `update()`, add an `if` statement to check if your `player.x` is very close to `star.x`.
    *   *Hint:* You can use `if player.x > star.x - 30 and player.x < star.x + 30:`
4.  If the player is close, print "You got the star!" and move the `star` to a new `x` position, like `star.x = 100`.
---
### Day 3: A Moving Obstacle
1.  Add a new `Actor` named `obstacle = Actor('slime')` to your `game.py`. (Add `slime.png` to `images`).
2.  Make `obstacle` move automatically left and right across the screen.
    *   *Hint:* Create a variable `obstacle_direction = 1` at the top. Inside `update()`, add `obstacle.x += obstacle_direction * 2`.
    *   Add `if` statements to change `obstacle_direction` when `obstacle.x` reaches the left or right side (e.g., `if obstacle.x < 100:` or `if obstacle.x > 700:`).
3.  (After core implementation) Change the image for your `obstacle` actor to something else you imagine, or try making it move a little faster.
---
### Day 4: Keeping Score
1.  Add a variable `score = 0` at the very top of your `game.py`.
2.  When your `player` "collects" the `star` (from Day 2), add 1 to your `score`.
3.  After increasing the score, `print()` the new `score` to the console.
    *   *Hint:* `print("Score:", score)`
---
### Day 5: Game Goal
1.  Inside your `update()` function, add an `if` statement to check if `score` reaches 3.
2.  If the `score` is 3, print "YOU WIN!" and reset the `player` to `player.x = 50`. Also, reset `score` back to 0.
3.  (Open-ended) Make the `star` (from Day 2) move automatically like the `obstacle` from Day 3, but perhaps at a different speed or in a smaller area.
