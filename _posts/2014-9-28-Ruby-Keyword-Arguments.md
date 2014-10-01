---
layout: post
title: Ruby Keyword Arguments. Improve your code readibility
---

I know, I know. I'm late to the party. Keyword Arguments is an old feature in Ruby. It's available since Ruby 2.0 and required keyword arguments is a feature supported since Ruby 2.1. At the time of this post the stable ruby version is Ruby 2.1.3. So yeah, this is ancient history. 

Nevertheless, given that I was very happy when I found it, I wanted to write about it. There are probably some people that like me don't know about them and I want to help them leave that dark place they are living in.

### What is this Keyword Arguments thing?

Keyword arguments is nothing more than **named parameters**. Meaning that we have to pass the name of each parameter within the method call.

So our method defined and called like this

{% highlight ruby %}
def cool_method(magic_number, magic_type)
  ### some beautiful code that outputs rainbows and unicorns
end

cool_method(10, "black magic")
{% endhighlight %}

Can be defined and called like this

{% highlight ruby %}
def cool_method(magic_number: 1, magic_type:)
  ### some beautiful code that outputs rainbows and unicorns
end

cool_method(magic_number: 10, magic_type "black magic")
{% endhighlight %}

*Note: default arguments are set in the method signature after the ":". If the parameter is required just create the argument with trailing colon as "magic_type:". Ruby will raise an **ArgumentError** if that argument is not passed within the call.*

### Why I should I use it?

You probably noticed how keyword arguments add more characters to our code. And this is just a small example, on a large codebase the amount of keystrokes are going to be considerably augmented by using keywords arguments. How can this be a good thing?

Well your code is also exponentially more readable. When reading method calls, specially in large projects that are being mantained by a team rather and an individual, you can forget (I do it everytime) signature of the method. Yeah I can see the method being called like this

{% highlight ruby %}
cool_method(10, "black magic")
{% endhighlight %}

but I have to trace back the method definition to know that 10 is supposed to be *magic_number* and black_magic is supposed to be *magic_type*. On the other hand when I see this

{% highlight ruby %}
cool_method(magic_number: 10, magic_type "black magic")
{% endhighlight %}

I don't need anything else.

Now, let's say you know well that we are working with numbers and magic type, what else could our *cool_method* receive as arguments, right? You would think that keyword arguments are unnecesarry for you. Think again. Another advantage of using Keyword Arguments is that you don't need to remember the position of the arguments.

I mean anything could happen if you call the method like this.

{% highlight ruby %}
cool_method("voldemort magic", 20)
{% endhighlight %}

I don't think the result of that method will be rainbows and unicorns anymore.

## Umm, wait a second there ...

You currently use **option hash** you say? I used to do it like that too. But Keyword Arguments are better, there's a lot of boilerplate code that goes into extracting the variables from the hash and more code means more opportunity for bugs and also have the drawback that we actually have to read the method body in order to find out the name of the arguments.

## Conclusion

It's easy to see that Keyword Arguments advantages far outweights it's disavantages. I have heard some Rubyist stating that they will only use this feature in methods that have more than 2 or 3 arguments,  I am one that will use them on every method from now on. The time I save looking up for the definition or going back because the test failed because the position of the arguments were wrong is going to be well spent elsewhere.

#### Feel free to comment or point out any error on this article. I will apreciate it.
