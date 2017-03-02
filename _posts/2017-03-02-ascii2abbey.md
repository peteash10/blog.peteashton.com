---
layout: post
title:  "ASCII to Abbey"
date:   2017-03-02 15:00:00 +0000
category: "Art"
---

Continuing my experiments with [pix2pix](https://github.com/phillipi/pix2pix), I've been training it on exclusively colour photos taken from the [Trailblazers](http://www.stanscafe.co.uk/trailblazers.html) project. This is an archive of [11,000 pics](https://www.flickr.com/photos/bhamtrailblazers/albums) (plus anther 2,000 documentation photos) taken by 14 year old students around Birmingham over the winter of 2015/16 which I've been wanting to push through machine learning every since. 

Using the same process as [Pictures from Dorian Gray](http://blog.peteashton.com/art/2017/02/24/pictures_dorian_gray/) I cropped and ASCII-ified them to create training pairs. 

![](images/00112.jpg)![](images/00285.jpg)![](images/00498.jpg);

Because training on 13,000 images will take days, if not weeks, I started with a more reasonable 500. My test was an ASCII-art version of the Beatle's Abbey Road picture. 

![](images/abbey3-a.jpg)

The training process tries to understand the relationship between the left and right pairs and then uses this knowledge to create the right image from the left, learning from the success or otherwise of each attempt. Each complete pass over the images is called an "epoch" and there are 200 epochs in a standard training session. 

Here's the test image recreated after 10, 130 and 200 epochs. 

![](images/abbey3-early.jpg)![](images/abbey3-mid.jpg)
![](images/abbey3-final.jpg)

I'm now training on all 13,000 images. While it's doing that I'm going to look into creating prose from the images, using something like Ross Goodwin's [NeuralSnap](https://github.com/rossgoodwin/neuralsnap), trained on the transcriptions of interviews with the kids, which can then be turned back into images. 

And then the itterative loops can begin! 