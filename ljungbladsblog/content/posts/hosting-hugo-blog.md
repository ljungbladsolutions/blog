---
title: "Create and host a blog using Hugo"
date: 2021-10-20T08:09:22+02:00
draft: true
---

#Hosting a blog using Hugo and GitHub

Prerequisites: Some knowledge about GitHub is good. 

Since this is my first post in this blog, it will be about how to create and host a blog using Hugo and GitHub.

I decided to use [Hugo](https://gohugo.io/about/what-is-hugo/) which is a static site generator that makes it easy to generate new pages/blog posts.
Hugo can be cloned from GitHub and easily run at your local machine to start with.

To have your site deployed on a static hosting service like [Netlify](https://www.netlify.com/) or [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages). 
I decided to go for GitHub pages. Let's do this:

###Part 1. Create necessary repositories in GitHub

Create a new repository on GitHub. It has to be named `<username>.github.io`.
Make it public unless you want to pay for it. In my case the name would be:
`ljungbladsolutions.github.io

Create another repository called `blog` (for example) make it public.

Clone your repository. 
```
git clone https://github.com/ljungbladsolutions/blog.git
```

###Part 2. Create new Hugo site
Create a new Hugo Site! Inside blog directory, create a new Hugo site by typing:
```
hugo new site ljungbladsblog -f yml
```
The `-f yml` is to use .yml instead of .toml

###Part 3. Add a theme
Go into project  folder (ljungbladsblog) and clone a theme you like.
[I choose this one](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation)

Either clone the theme:
```
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

Or download the theme and unpack it here. I did that, so now I can modify it myself. I used PaperMod v.5.0.
https://github.com/adityatelange/hugo-PaperMod/archive/v5.0.zip
Unpacked this in theme folder and named it to PaperMod5.

###Part 4. Configure site to use theme and setup the baseURL

In the config.yml add:

```
baseURL: https://github.com/ljungbladsolutions/ljungbladsolutions.github.io.git
languageCode: en-us
title: Christopher's Blog
theme: PaperMod5
``` 

###Part 5. Preview the newly created site locally
Preview blog locally, go to project folder (cljungblad) and write:
```
hugo server
```
View blog at: 
http://localhost:1313

Not very exciting, since there is no content. Let's add a new post.

###Part 6. Add a new post
Inside blog/ljungbladsblog type:
```
hugo new posts/myfirstpost.md
```



```java
public static void main(String[] args) {
    System.out.println("test");
}
```

