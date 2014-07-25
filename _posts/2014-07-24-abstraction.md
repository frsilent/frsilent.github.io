---
title: "Abstraction"
categories: ['conceptual', 'misc']
layout: post
---

# Abstraction

I decided to write my first "real" blog post about a subject that may not seem all that interesting at first but one I am passionate about. Abstraction.

The concept of abstraction is of vital importance to technology and its evolution. By their design however, abstractions are to be ignored and taken for granted. Because of this we are able to peacefully go through life without convulsively having to know just exactly how every piece of technology is used. However, every now and then, I find it enormously useful to analyze these abstractions and traverse their different layers.

If you're not a software developer or engineer, the concept of an abstraction may seem foreign to you but are in fact something you deal with on a daily basis. There is far too much information for any one person to process. Abstractions insulate us, protect us, and allow us to progress towards a broader picture. You don't need to be a mechanic to drive a car, an electrician to operate a television, or a computer programmer to access a website.

What got me thinking about this recently, is that I just finished [Code](http://www.amazon.com/dp/0735611319) by [Charles Petzold](http://en.wikipedia.org/wiki/Charles_Petzold) and really enjoyed his bottom-up way of teaching. This bottom-up approach really exposes the reader to every level as it is taught and then abstracted.

While this ability to black-box things has been responsible for our technological growth, there are some consequences to its application. One thing I've seen time and time again in subjects of math, science, and engineering is a willful refusal to sometimes break abstractions and trying to understand things. I guess even outside those domains I see this as an issue sometimes. It blew my mind to save as much money as I did by learning some basic maintenance of a vehicle. With the incredible availability of information these days there's very little that you can't research and figure out yourself, given enough time.

On the other hand, ignoring abstractions can easily lead to poor engineering, over-complicating a problem, and headaches. I guess my point is that like all tools they need to be understood in the context of their applications. For a simple example, the code block below demonstrates complexity by utilizing different levels of abstraction and not performing a singular identifiable task.

{% highlight py linenos %}
def cylinder_area(radius, height):
    return 2 * 3.142 * radius * height + 2 * 3.142 * radius * radius
{% endhighlight %}

While this isn't too difficult, imagine seeing that single return evaluation in a couple-hundred lines of code. A better solution would be as follows:

{% highlight py linenos %}
def cylinder_area(radius, height):
    pi = 3.142
    border_area = 2 * pi * radius * height
    end_area = pi * radius * radius
    return end_area * 2 + border_area  # 2 endpoints
{% endhighlight %}

Admitedly this example is incredibly simple and not one I would implement myself (most languages have an established Math.Pi constant), it does illustrate my point of differing layers of abstraction. Imagine for a second that you had no clue what Pi approximates to or even the proper way of calculating the area of a cylinder. The first method is cryptic and assumes that the reader will understand the approximation of Pi. The second works at a single layer of abstraction by defining a constant before executing and consistently building the solution.

Both methods however return the same answer and as such can both be treated as a black box without worrying about the individual implementations.


