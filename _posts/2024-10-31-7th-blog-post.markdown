---
layout: post
title:  "7th blog post: Turtle Crossing Game!"
date:   2024-10-31
categories: jekyll update
---
🚀 Excited to share my latest Python coding project: The Turtle Crossing Game! 🐢

Inspired by classic games like Snake and Pong, this project challenged me to dive deeper into object-oriented programming by working with classes and objects. The most interesting part? Figuring out how to get the "cars" to move across the screen!

Here’s how it works:

Each "car" is created at a random point along the Y-axis, added to a list, and then continuously moves “backward” across the screen.
This loop keeps the cars moving until the game ends, adding complexity and fun!
Take a look at some of the code I’ve been working on:


{% highlight python %}
    def create_car(self):
        random_choice = random.randint(1,6)
        if random_choice == 1:
            new_car = Turtle("square")
            new_car.shapesize(stretch_wid=1, stretch_len=2)
            new_car.penup()
            new_car.color(random.choice(COLORS))
            random_y = random.randint(-250, 250)
            new_car.goto(300, random_y)
            self.all_cars.append(new_car)

    def move_car(self):
        for car in self.all_cars:
            car.backward(self.car_speed)

{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/turtle_crossing_game)