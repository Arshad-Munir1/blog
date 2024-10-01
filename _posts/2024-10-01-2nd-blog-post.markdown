---
layout: post
title:  "2nd blog post: My Spirograph"
date:   2024-10-01
categories: jekyll update
---
Over the past few months, I've been diving deep into learning for loops and the while operator. It’s been a great experience, giving me a solid foundation to work from.

Now, I've reached an exciting phase in my learning journey: working with more graphical elements! I’m using the turtle module to create fun shapes and designs, which is a big step up from just writing basic loops.

The best part? Thanks to my understanding of for loops, I’ve been able to create something really cool—a spirograph! It’s such an elegant, simple bit of code that uses random colors and some math (like knowing that a circle has 360 degrees, and how to divide it evenly).

Here’s a little snippet of the code I’ve been working on:


{% highlight python %}
def draw_spirograph(size_of_gap):
    for _ in range(int(360 / size_of_gap)):
        tim.color(random_color())
        tim.circle(100)
        tim.setheading(tim.heading() + size_of_gap)
{% endhighlight %}

![Output: ]({{ site.url }}{{ site.baseurl }}/assets/Images/spirograph.jpg)