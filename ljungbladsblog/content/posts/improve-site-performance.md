---
title: "Measure and Improve Site Performance"
date: 2021-12-22T14:10:15+01:00
draft: false
defaultTheme: light
categories: [web, performance]
tags: [performance, images]
ShowToc: true
---

### Improve site performance 
To find out how your site perform, use [Google Page Speed Insight](https://pagespeed.web.dev/).  

The result will give you many hints on what to do to improve performance. But this post 
will only talk about how to improve page speed by compressing images, since this is a common issue. Other things could be to cache .js files and stylesheets.  

This is the result of the first page of this blog, it's 100% :). But it's only one small image, go ahead and try other pages, and you will probably find a lot of improvements that can be applied.
![Google Page Speed Insight Example](/images/google_performance.png)

### How do I know if an image is too big?
Well it's all about preferences, but most of the time it's possible to compress the images a lot without loosing any visual (for the eye) quality.  

So I would suggest to check out these two tools, and compress your images, and then 
decide if it's worth using the compressed image and get a faster site, or if you like to stick with the larger file. 

 - To compress png, jpg use: https://tinyjpg.com/
 - To compress SVG, use chrome plugin: svgomg

Here is an example where I compressed an image 72%, but using `tinyjpg`  
(It's the screenshot of Google Page Insight further down.)
![Tinyjpg example](/images/google-performance-tinyjbp-ex.png)

### View the result 
Change to the compressed images and redo the measuring using the [Google Page Speed Insight](https://pagespeed.web.dev/). 
My blog was a pretty bad example, since it already had 100% though :). 













