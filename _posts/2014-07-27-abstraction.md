---
title: "Abstraction"
categories: ['conceptual', 'misc']
layout: post
---

# Abstraction

Before starting, I'd like to mention that I've added the ability to post comments on individual entry pages. Also, I've added rudimentary syntax highlighting for code examples. As always I greatly appreciate any feedback as I continue to make improvements and tweaks to the site. Enough with the maintenance, let's dive right in!

So I've decided to write my first "real" blog post about a subject that I am passionate about. Abstraction. To be clear, I define an abstraction as the separation of a tool/idea/method from its implementation. For instance there are several ways of communicating a message: by voice, email, letter, instant message, etc. The abstraction is simply 'communicating'. The medium is irrelevant.

For those that are not software developers or engineers, the concept of an abstraction may seem foreign but they are in fact vital to our way of life. The fact of the matter is that there is far too much information for any one person to process. Abstractions insulate us, protect us, and allow us to understand complex systems from a higher level. Because of this, you don't need to be a mechanic to drive a car, an electrician to operate a television, or a computer programmer to access a website.

This concept of abstraction is of vital importance to technology, but by design abstractions are generally to be ignored and taken for granted. Because of this we are able to live without convulsively having to know just exactly how every piece of technology that touches our lives is used. Increasingly, I find it useful to analyze these abstractions and traverse their different layers.

I recently finished [Code](http://www.amazon.com/dp/0735611319) by [Charles Petzold](http://en.wikipedia.org/wiki/Charles_Petzold) and really enjoyed his bottom-up way of teaching. He begins with an example of two children using flashlights late at night to shine messages into each other's bedroom windows. From this foundation he explains the fundamentals of morse code, the telegraph, and eventually the logic gate. To quote Joe Rose, my first programming boss and mentor, "Nothing we will ever do here is that complicated. Tedious? Yes. But complicated only if you try to look at it all at once." Going back to Petzold's book, this bottom-up approach really exposes the reader to every level as it is taught and then abstracted. By doing this it empowers the engineer-hopeful and gives them a powerful tool in analyzing the world around them.

While this ability to black-box things has been responsible for our technological growth, there are some consequences to its application. One thing I've seen time and time again in subjects of math, science, and engineering is a willful refusal to sometimes break abstractions and trying to understand things. I guess even outside those domains I see this as an issue sometimes. It blew my mind to save as much money as I did by learning some basic maintenance of a vehicle. I guess this is why I find the bottom-up approach so appealing. With it, working at any level of abstraction requires you to know at least a few layers deeper. With the incredible availability of information these days there's very little that you can't research and figure out yourself, given enough time.

On the other hand, undervaluing abstractions can easily lead to poor engineering, over-complication of a problem, and headaches. I guess my point is that like all tools they need to be understood in the context of their applications. In designing a full system, I think that a top-down approach helps to alleviate this. By designing interfaces at a single level, you can avoid making an issue overly complex by ignoring any of the details and not over-engineering a solution. For a simple example, the code block below demonstrates complexity by utilizing different levels of abstraction and not performing a singular identifiable task.

{% highlight py linenos %}
def cylinder_area(radius, height):
    print 2 * 3.142 * radius * height + 2 * 3.142 * radius * radius
{% endhighlight %}

While this isn't too difficult, imagine seeing that single evaluation in a couple-hundred lines of code. To make it more complicated, imagine replacing the 3.142 with a mathematical approximation of Pi with [Machin's formula](http://en.literateprograms.org/Pi_with_Machin's_formula_(Python)). Pi is a great example of just why abstractions are so useful to us.

To get back to the first example, a better solution would be as follows:

{% highlight py linenos %}
def cylinder_area(radius, height):
    pi = 3.142
    border_area = 2 * pi * radius * height
    end_area = pi * radius * radius
    print end_area * 2 + border_area  # 2 endpoints
{% endhighlight %}

Admittedly this example is incredibly simple and not one I would implement myself (most languages have an established Math.Pi constant as well). It does however illustrate my point of differing layers of abstraction. Imagine for a second that you had no clue what Pi approximates to or even the proper way of calculating the area of a cylinder. The first method is cryptic and assumes that the reader will understand the approximation of Pi. The second works at a single layer of abstraction by defining a constant before executing and then building up a solution progressively. In both of these examples, the same answer is returned and as such can be treated as a black box with the appropriate abstraction. In the first case such an abstraction serves to insulate us from a sub-par implementation.

This is a subject to which I could write much more but feel that my point has been made so will leave it with some closing thoughts.

1. Abstractions are of vital importance to us and our way of life. Embrace them and learn how to apply them to your self-discovery and learning.
2. I would advocate a bottom-up approach to learning a tough subject. This is taught to us in mathematics but is often ignored for very similar types of learning.
3. When designing a system, I would go with a top-down approach. This allows you to quickly list the necessary modules for a "complete" solution.
