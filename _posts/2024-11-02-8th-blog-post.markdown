---
layout: post
title:  "8th blog post: Snake Game update!"
date:   2024-11-02
categories: jekyll update
---
Are you growing by 1% each day? The power of compounding progress is incredible, and that’s exactly what I’m aiming for in my Python coding journey!

I’ve committed to writing at least one line of code daily, believing that small steps will add up over time.

Improving isn’t just about learning something new each day, but also about refining previous projects. Recently, I revisited my snake game and decided to enhance it by adding a permanent high score feature—one that remains even after you exit and restart the game.

To make this possible, I modified the game_over method to "reset" instead of stopping, saving the score into a high_score variable stored in a text file. Here’s the key code:

{% highlight python %}
    with open("data.txt") as data:
        self.high_score = int(data.read())

{% endhighlight %}

This initialises the high score from data.txt.

{% highlight python %}
    with open("data.txt", mode="w") as data:
        data.write(f"{self.high_score}")

{% endhighlight %}

And this saves the high score whenever it changes.

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/snake_game)