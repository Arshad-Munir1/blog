---
layout: post
title:  "3nd blog post: My Art Dot Paiting"
date:   2024-10-05
categories: jekyll update
---
Over the last week i've been using the turtle module to produce images.
I've been looking at some of Damien Hirst's art and wanted to prodcue a dot image that he is famous for.
Some of his paintings had sold for £1.5M!!!

So again, using the turtle module, i've created a dot image.

The first part of this challenge was to lift colours from a dot image. I used the colorgram Python Library
to help me with this.
I would say, using the above library and then getting the output into a usable form (i.e. a list of tuples),
was the most challenging part of this task.
Once you have a list of colours it was quite straight forward to randomise the colours to make a dot image.

Here’s a little snippet of the code I’ve been working on:


{% highlight python %}
for dot_count in range(1, number_of_dots + 1):
    timmy.dot(20, random.choice(color_list))
    timmy.forward(50)

    if dot_count % 10 == 0:
        timmy.setheading(90)
        timmy.forward(50)
        timmy.setheading(180)
        timmy.forward(500)
        timmy.setheading(0)
{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/Art-dot-painting)

This is the output:
![Output: ]({{ site.url }}{{ site.baseurl }}/assets/Images/dot.jpg)