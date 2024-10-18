---
layout: post
title:  "5th blog post: Snake Game!"
date:   2024-10-18
categories: jekyll update
---
This project was both challenging and incredibly rewarding! The development journey involved several key steps:

Creating the snake body
Implementing movement
Adding controls
Detecting collisions with food
Building a scoreboard
Detecting collisions with walls and the snake's tail

While the initial steps went smoothly, things got tricky when it came to creating separate classes and managing objects. But once the classes were set up, the main.py file became much cleaner and easier to work with.

I'm excited about how much I’ve learned from this project – it’s a huge step forward in my coding journey!


Here’s a quick peek at the code I’ve been playing with:


{% highlight python %}
game_is_on = True
while game_is_on:
    screen.update()
    time.sleep(0.1)
    snake.move()

    #Detect collision with food
    if snake.head.distance(food) < 15:
        food.refresh()
        snake.extend()
        scoreboard.increase_score()

    #Dectect collision with wall
    if snake.head.xcor() > 280 or snake.head.xcor() < -280 or snake.head.ycor() > 280 or snake.head.ycor() < -280:
        game_is_on = False
        scoreboard.game_over()

    #detect collision with tail
    for segment in snake.segments[1:]:
        if snake.head.distance(segment) < 10:
            game_is_on = False
            scoreboard.game_over()

{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/snake_game)