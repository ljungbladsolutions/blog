---
title: "Working with hugo"
date: 2021-11-25T08:09:22+02:00
draft: false
categories: [development]
tags: [blogging,hugo]
ShowToc: true
---

## Setup Hugo blog 
This post will give an intro how to get started editing a Hugo Site.  
If you have not already Hugo setup, go to my previous post found [here](/posts/hosting-hugo-blog)

### Run Hugo locally
Go to your blog directory, where the content is and run:  
`hugo server`

### Add content (a new post)
To add a new post, run:  
`hugo new posts/intro-to-java-17.md`

This will create a file `intro-to-java-17.md` in your post directory, having a menu.  

```
---
title: "Intro to java 17"
date: 2021-11-25T08:09:22+02:00
draft: true
defaultTheme: light   
ShowToc: true
---
```

Here I also added:  
`defaultTheme: light`   //will show this page in light theme
`ShowToc: true`         //will show a Table of content (every headline will be added in the Toc)



### Add a menu
I choose to manually add the menu in the config.yml file something like this:
```
menu:
  main:
    - identifier: about
      name: About
      title: About me
      url: /about/
      weight: -100
    - identifier: archives
      name: Archive
      title: blog section
      url: /archives/
      weight: -300
    - identifier: Categories
      name: Categories
      title: Categories
      url: /categories/
      weight: -200
```
There are many ways you can add a menu, read more about it [here](https://gohugo.io/templates/menu-templates/#site-config-menus)

###  Adding a categories and labels to your posts
In Hugo this is the chapter about `taxanomies`, in other words `how to group and order your content`.  
[Read more on hugo site about taxanomies.](https://gohugo.io/content-management/taxonomies/)

#### 1. How to add taxanomies (categories and tags)
There are two `taxanomies` that Hugo will automatically create for you, namely `categories` and `tags`.
So there is no need to add these in the `config.yml`. I did it anyway, just to show that these are my `taxanomies`  
and to make it easier to add others later, so in my `config.yml` I added:
```
taxonomies:
  category: categories
  tag: tags
```

#### 2. How to add category and tags to a post
For example, this post has the `category=development` and two `tags`, `blogging and hugo`. This was added like this:   
```
---
title: "Working with hugo"
date: 2021-11-25T08:09:22+02:00
draft: false
categories: [development]
tags: [blogging,hugo]
ShowToc: true
---
```

This will show up in the `/categories`. Which was also added to the menu.

### Config file setup example
This is an example of the `config.yml`, this one is pretty much copied from the PaperMod example and modified to fit my page:  

```
baseURL: https://ljungbladsolutions.github.io/posts
languageCode: en-us
title: Ljungblad Solutions
theme: PaperMod5
defaultTheme: light

menu:
  main:
    - identifier: about
      name: About
      title: About me
      url: /about/
      weight: -100
    - identifier: archives
      name: Archive
      title: blog section
      url: /archives/
      weight: -300
    - identifier: Categories
      name: Categories
      title: Categories
      url: /categories/
      weight: -200

params:
  env: production # to enable google analytics, opengraph, twitter-cards and schema.
  description: "A blog about Software development, architecture and other things."
  author: Christopher Ljungblad
  defaultTheme: auto
  # disableThemeToggle: true
  ShowShareButtons: true
  ShowReadingTime: true
  # disableSpecial1stPost: true
  displayFullLangName: true
  ShowPostNavLinks: true
  ShowBreadCrumbs: true
  ShowCodeCopyButtons: true
  ShowToc: true #Show table of content
  # comments: false
  images: ["papermod-cover.png"]

  profileMode:
    enabled: true
    title: Christopher Ljungblad
    imageUrl: "/images/christopher.png"
    imageTitle: my image
    # imageWidth: 120
    # imageHeight: 120
    buttons:
      - name: Archive
        url: archives
      - name: Categories
        url: categories

  homeInfoParams:
    Title: "Christopher Ljungblad"
    Content:
  socialIcons:
    - name: github
      url: "https://github.com/ljungbladsolutions/"
    - name: LinkedIn
      url: "https://www.linkedin.com/in/ljungblad/"

taxonomies:
  tag: "tags"
  category: "categories"
```




### Add raw html to your post
Sometimes it's necessary to use html. This can be done using the `{{</* rawhtml */>}}`, for example:
```
{{</* rawhtml */>}}
<strong>This is my html</strong>
{{</* /rawhtml */>}}
```

For this to work, there has to be a file:  
`layouts/shortcodes/rawhtml.html` containing:  
```
<!-- raw html -->  
{{ .Inner }}
```


###  Example page for this theme
[Here is an example for this theme, find inspiration here on gitHub.](https://github.com/adityatelange/hugo-PaperMod/tree/exampleSite)

References:  
[https://gohugo.io/templates/homepage/](https://gohugo.io/templates/homepage/)  
[https://guides.github.com/features/mastering-markdown/](https://gohugo.io/templates/homepage/)  
[https://gohugo.io/getting-started/configuration/](https://gohugo.io/getting-started/configuration/)  