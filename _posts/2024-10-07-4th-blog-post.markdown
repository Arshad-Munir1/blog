---
layout: post
title:  "4th blog post: Turtle Race!"
date:   2024-10-07
categories: jekyll update
---
Still on the topic of turtle graphics currently. The latest project which i really enjoyed has been the turtle race!
Getting the turtles to starting points, randomising colours and giving them random distances to move was cool.
The tricky part was introducing a "while loop" that kept the race going until one hit the end of the screen (or near the end of the screen)

Here’s a quick peek at the code I’ve been playing with:


{% highlight python %}
while is_race_on:
    for turtle in all_turtles:
        if turtle.xcor() > 230:
            is_race_on = False
            winning_colour = turtle.pencolor()
            if winning_colour == user_guess:
                print(f"you won! The {winning_colour} turtle is the winner")
            else:
                print(f"you lost! The {winning_colour} turtle is the winner")
{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/turtle_race)

This is the output:
![Output: ]({{ site.url }}{{ site.baseurl }}/assets/Videos/turtle_race.mp4)