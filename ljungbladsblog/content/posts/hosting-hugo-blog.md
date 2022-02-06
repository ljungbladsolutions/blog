---
title: "Create and host a blog using Hugo"
date: 2021-11-08T08:09:22+02:00
draft: false
defaultTheme: light
categories: [development]
tags: [blogging,hugo]
ShowToc: true
---

Prerequisites: Some knowledge about GitHub is good. 

Since this is my first post in this blog, it will be about how to create and host a blog using Hugo and GitHub.

I decided to use [Hugo](https://gohugo.io/about/what-is-hugo/) which is a static site generator that makes it easy to generate new pages/blog posts.
Hugo can be cloned from GitHub and easily run at your local machine to start with.

To have your site deployed on a static hosting service like [Netlify](https://www.netlify.com/) or [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages). 
I decided to go for GitHub pages. Let's do this:

### Install hugo
Can be done in many ways as explained [here](https://gohugo.io/getting-started/installing/), I did it with brew, like this:  
```
brew install hugo
```

### Part 1. Create a github repository for the blog

Create a repository called `blog` (for example) and make it public.

Next we'll create the hugo site, so clone your repository to you local machine. 
```
git clone https://github.com/ljungbladsolutions/blog.git
```

### Part 2. Create new Hugo site
Inside `blog` directory, create a new Hugo site by typing:
```
hugo new site ljungbladsblog -f yml
```
The `-f yml` is to use .yml files instead of .toml for the configuration.

### Part 3. Add a theme
Go into project  folder (ljungbladsblog) and clone a theme you like.
[I choose this one](https://github.com/adityatelange/hugo-PaperMod/wiki/Installation).

Either clone the theme:
```
git clone https://github.com/adityatelange/hugo-PaperMod themes/PaperMod --depth=1
```

Or download the theme and unpack it here. I did that, so now I can modify it myself. I used PaperMod v.5.0.
https://github.com/adityatelange/hugo-PaperMod/archive/v5.0.zip.  
Unpacked this in `theme` folder and named it to PaperMod5.

### Part 4. Configure site to use theme and setup the baseURL

In the config.yml add:

```
baseURL: https://github.com/ljungbladsolutions/ljungbladsolutions.github.io.git
languageCode: en-us
title: Christopher's Blog
theme: PaperMod5
``` 

### Part 5. Preview the newly created site locally
Preview blog locally, go to project folder (cljungblad) and write:
```
hugo server
```
View blog at: 
http://localhost:1313

![Blog no content](/images/blog-empty.png)

Not very exciting, since there is no content. Let's add a new post.

### Part 6. Add a new post
Inside blog/ljungbladsblog type:
```
hugo new posts/myfirstpost.md
```
### Part 7. Edit a post
To be able to make nice posts, you need to master github markdowns, to make headers, links, insert images etc.  
[Here is a guide for github markdowns](https://guides.github.com/features/mastering-markdown/)

Open the `post/myfirstpost.md` file to start editing, using your favorite editor. I'm using pretty much IntelliJ for everything.  
Change the file content to be:

```
---
title: "My first post"
date: 2021-10-25T09:02:53+02:00
draft: false
---

### My first post!

```java
public static void main(String[] args) {
    System.out.println("Hello world!");
}
```

To view the newly added post (not being a draft):  
[http://localhost:1313/posts/](http://localhost:1313/posts/)  

![Blog with one post](/images/blog-one-post.png)

To open the content of the post: 
[http://localhost:1313/posts/my-first-post/](http://localhost:1313/posts/my-first-post/)

![Blog with post content](/images/blog-post-content.png)

 
### Part 8. Push content to blog repository
```
>git add .
>git branch -m master main
>git commit -m "initial commit"
>git push origin main
``` 
We also changed the master branch to be main here.

### Part 9. Create a github.io hosting service repository
Now it's time to create the github.io hosting repository where your blog content will be hosted.  

Create a new repository on GitHub, that will be used for hosting the blog.      
It has to be named `<username>.github.io` for example `ljungbladsolutions.github.io`.  
Make it public unless you want to pay for it. 

Go to the parent directory of the `blog and clone the io project, this is where the static content will stay:
```
git clone https://github.com/ljungbladsolutions/ljungbladsolutions.github.io.git
```

Make sure the default branch is main, not master.
```
git branch -m master main
```

Add something to the github.io directory (it cannot be empty):
```
>cd ljungbladsolutions.github.io
>touch README.md
>git add .
>git commit -m “adding readme file”
>git push origin main 
```

### Part 9. Add the created blog content to the github.io hosting service repository
So now we have two repositories.
1. `blog` used for the blog code
2. `ljungbladsolutions` is used for hosting the static assets 

By adding the `ljungbladsolutions.github.io.git` repository as a submodule and add the `public` folder.   

Go to `blog/ljungbladsolutions` directory and type:
```
git submodule add -b main https://github.com/ljungbladsolutions/ljungbladsolutions.github.io.git public
```
The static files that are generated will now be available from the public folder automatically.

### Part 10. Build content to public folder
Generate content to the public folder (build the code).  
Go to `blog/ljungbladblog` and type:
```
hugo -t PaperMod
```
And all this generated code will go into the public directory. This is your static assets that you want to push.  

If you do a git remote -v inside the public folder, you can see that that it points to:
https://github.com/ljungbladsolutions/ljungbladsolutions.github.io.git

### Part 11. Push the changes to the public folder
To push the changes in the public folder after building hugo, go to the `public` folder:
```
> git status (will show all uncommitted files)
> git add .  (add everything)
> git commit -m “initial commit”
> git push origin main
```
### Part 12. View the published site at github.io
Now your site should have been published. Enter your github.io repository and go to Settings, find the Pages settings.
https://github.com/ljungbladsolutions/ljungbladsolutions.github.io/settings/pages    
https://github.com/<username>/<username>.github.io/settings/pages  

This is where my this blog is found.  
[https://ljungbladsolutions.github.io/](https://ljungbladsolutions.github.io)


### Happy blogging, go on and make your blog a bit nicer!  
And now when it's up and running let's go on and add some content like, more, posts, table of contents, a menu, search page, etc.  
Find my post about Hugo editing [here](/posts/editing-hugo-blog)





 



