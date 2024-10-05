---
layout: post
title:  "3rd blog post: My Art Dot Painting"
date:   2024-10-05
categories: jekyll update
---
This past week, I've been diving into Python’s turtle module to create some eye-catching art! Inspired by the legendary Damien Hirst, whose dot paintings have sold for as much as £1.5 million, I wanted to try my hand at producing my own dot masterpiece.

To get started, I needed to extract colors from one of Hirst's famous dot images. For this, I turned to the colorgram Python library, which helped me pull out the perfect color palette. I have to admit, transforming that data into something usable—a neat list of tuples—was the trickiest part! But once I cracked that, it was smooth sailing, as I randomised the colors to form my own unique dot image.

Here’s a quick peek at the code I’ve been playing with:


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

I commented out the code that I used for extracting the colours using the colorgram library, as once i had the colours in tuples, i didn't need to run the code again.

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/Art-dot-painting)

This is the output:
![Output: ]({{ site.url }}{{ site.baseurl }}/assets/Images/dot.jpg)