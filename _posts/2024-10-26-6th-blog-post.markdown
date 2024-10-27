---
layout: post
title:  "6th blog post: Pong Game!"
date:   2024-10-26
categories: jekyll update
---
Excited to share my latest coding project in Python—a throwback to the classic Pong game!

Ironically, I never actually played Pong as a kid, but building it was incredibly fun and rewarding. The process was similar to my previous Snake game project, where I created a paddle, screen, and ball using Python’s Turtle graphics. Thanks to my earlier experience, building Pong felt smoother and more intuitive this time around. It’s a great reminder of the power of consistency—the more you practice, the easier it becomes!

Looking forward to diving into my next project and keeping the momentum going!


Here’s a quick peek at the code I’ve been playing with:


{% highlight python %}
game_is_on = True
while game_is_on:
    time.sleep(ball.move_speed)
    screen.update()
    ball.move()

    #detect collision
    if ball.ycor() > 280 or ball.ycor() < -280:
        ball.bounce_y()

    #detect collision with paddle
    if ball.distance(r_paddle) < 50 and ball.xcor() > 320 or ball.distance(l_paddle) < 50 and ball.xcor() < -320:
        ball.bounce_x()

    #detect r_paddle miss
    if ball.xcor() > 380:
        ball.reset_position()
        scoreboard.l_point()

    # detect l_paddle miss
    if ball.xcor() < -380:
        ball.reset_position()
        scoreboard.r_point()

{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/pong)