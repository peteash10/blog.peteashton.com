---
layout: posts
title:  "Pictures from Dorian Gray"
date:   2017-02-24 15:00:00 +0000
category: "Art"
---

![](/images/Pictures_From_Dorian_Gray_6.jpg)

I've been exploring the potential of the [pix2pix](https://github.com/phillipi/pix2pix) system for generating photos from abstract representations of objects. A popular version of this currently buzzing around the internet is [edges2cats](http://affinelayer.com/pixsrv/index.html), because cats, and more interesting work is being done by [Mario Klingemann](http://mario-klingemann.tumblr.com).

The basic principle is fairly simple. You create a pair of images. One is the original image and the other is an abstraction, usually an outline. You then train a neural network to try to generate the original from the abstraction. This is analogous to teaching a child to recognise dogs. You show it lots of pictures of different dogs labelled "dog" and eventually the child will correctly identify a dog even if it's never seen that specific dog before.

[![](/images/pix2pixexamples.jpg)](https://github.com/phillipi/pix2pix)

Once you've trained the system, you can then give it abstractions and ask it to figure out the "original". In theory it produces something that looks real, which is the goal of these systems. In practice it's very easy to produce something that looks weird and interesting, which is why artists have latched on to this stuff. 

As well as the joy of producing weird images, I'm interested in exploring what's actually happening in these systems by poking them with sticks. I was drawn to [Mario's use of blurred abstractions](http://mario-klingemann.tumblr.com/post/157270869090/yhancik-mario-klingemann-trained-pix2pix-with) to create an oil-paint effect and wondered what other sorts of abstractions could be used. Since some of my work has involved transforming between mediums ([image to sound](http://art.peteashton.com/live-sonification-photography/), etc) I thought I'd give [ASCII Art](https://en.wikipedia.org/wiki/ASCII_art) a try. 

I used a collection of "classic photography" I'd found a while back as my training data and produced ASCII versions of each picture using the process included in Apple's Automator app. Here's an example. 

![](/images/training-1-photo-0003.jpg)

The ASCII here is quite fine and uses all the possible characters, which wasn't giving me the abstraction I needed, so I went with [jp2a](https://csl.name/jp2a/) which gave me a lot more control. Specifically I could up the font size and chose which characters it used. By limiting it to lower-case a-z and select punctuation I was able to generate this:

![](/images/training-2-photo-0003.jpg)

Now the abstraction looks closer to real text, the sort you might get in a book that makes sense. This is what I was after. 

With the training underway I started to prepare my input for the final piece. I needed a body of text and settled on the Gutenberg edition of Oscar Wilde's [The Picture of Dorian Gray](http://www.gutenberg.org/ebooks/4078) because one should always go for the pun, but any text would do. I removed all paragraphs and extraneous spacing and exported it into squares which resembled the generated ASCII art. Here's the first page. 

![](/images/dorian_sq_01.jpg)

Once the training had finished processing overnight (it's a long process, though my electricity usage plug says it only cost 24p for 12 hours, which isn't bad) I asked it to generate photos from all 91 pages. Here's that first page again. 

![](/images/dorian_sq_01-after.jpg)

And here's all the pages in a [video](https://vimeo.com/205563393):

<iframe src="https://player.vimeo.com/video/205563393?loop=1&title=0&byline=0&portrait=0" width="640" height="640" frameborder="0" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>

You can also [download it as a PDF](/images/Pictures_From_Dorian_Gray.pdf) if you like. 

Much more to be done, which is why this is a blog post and not on my [Art website](http://art.peteashton.com) yet. Onwards! 
