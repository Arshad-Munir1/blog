---
layout: post
title:  "9th blog post: Creating Letters"
date:   2024-11-04
categories: jekyll update
---
Transitioning from coding games (though I might revisit them for improvements!) to working with data files. In my recent Snake project, I used a data file to keep track of the high score, but now I’m taking it further by using two data files to create personalised letters.

The setup is simple: one file contains a list of names, and another holds the letter template where only the name changes. With just a bit of code, I can automate the creation of multiple customised letters. This type of automation could simplify real-world tasks, such as:

Scenario: A company needs to send personalised thank-you notes or promotional messages to hundreds or thousands of customers.
Benefit: Automation ensures each customer gets a tailored message, fostering better relationships and potentially boosting customer retention and sales.

Scenario: Businesses need to notify suppliers about changes to purchase orders, delivery schedules, or policy updates.
Benefit: Automated communication helps maintain smooth operations and ensures that each supplier receives timely, accurate information.

There are many more scenarios where this concept can be applied to improve efficiency—but I’ll leave it at that for now!

Heres a peak at the code:

{% highlight python %}

PLACEHOLDER = "[name]"

with open("./Input/Names/invited_names.txt") as names_file:
    names = names_file.readlines()

with open("./Input/Letters/starting_letter.txt") as letter_file:
    letter_contents = letter_file.read()
    for name in names:
        stripped_name = name.strip()
        new_letter = letter_contents.replace(PLACEHOLDER, stripped_name)
        with open (f"./Output/ReadyToSend/letter_for_{stripped_name}.txt", mode="w") as completed_letter:
            completed_letter.write(new_letter)

{% endhighlight %}

See below link to the full code on GitHub
[My GitHub Repository](https://github.com/Arshad-Munir1/mail_merge)