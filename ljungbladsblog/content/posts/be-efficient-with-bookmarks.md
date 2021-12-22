---
title: "Be Efficient With Chrome Bookmarks"
date: 2021-12-12T08:11:40+02:00
draft: false
defaultTheme: light
categories: [productivity]
tags: [bookmarks]
ShowToc: true
---

How often do open Chrome and search for something to find an already known site. Usually you add a bookmark to 
frequently visited pages. But there is more to having bookmarks, and using bookmarks effectively.  

Here are some tips on how you can increase your productivity using your chrome bookmarks more effectively.

### 1. Categorise, prioritise and visualise bookmarks in Chrome  
- Use folders to categorise your bookmarks in. For example, have your `playing guitar` links in one folder and your `Recipies` in another.
- Do this by opening the Chrome `Chrome Bookmark Manager`.
- Put the folders in prioritisation order, the most used folder first.
- Also make sure to have a `tmp` folder where temporary bookmarks can be stored.
- In Chrome select `View -> Always Show Bookmarks Bar`
- Now you will have a menu in Chrome with all your bookmarks categorised in a prioritised order.

### 2. Make your bookmarks searchable from the address bar
1. Open the Chrome SearchEngines: [chrome://settings/searchEngines](chrome://settings/searchEngines)
2. Add a new `Search Engine` by clicking the `Add` button and fill in following:
```
- Search Engine Name: Chrome Bookmarks
- Keyword: b
- URL: chrome://bookmarks/?q=%s
```
3. Go back to address bar in Chrome and try it out by entering a `b` followed by a space, and then the `search keywords`.  
4. For example: `b lasagna` to find your favorite lasagna bookmark.

### 3. Use aliases for your bookmarks
1. Go to chrome://settings/searchEngines
2. Find the `Add` button
3. Enter `Search engine` which is just a description of that `url`, then the `keywork` (the alias), and then the `url`.
4. There is also a feature where it's possible to add `in parameters` for the url.  
For example: `http://supermaps?search=%s` Then if the `keyword`is `map`, you would use `map stockholm` to get `http://supermaps?search=stockholm  `

In Chrome press `⌘ + L` mac, (`Ctrl + L` windows) to focus on the address bar.

#### Prepare to be able to add new alias quickly
Add the `chrome://settings/searchEngines` url as a keyword. 
*For example:* 
- Search engine: Add a new alias as a searchEngine
- Keword: `na`  (for new alias)
- Query url: chrome://settings/searchEngines
- Now the only thing you need to do is to write `na` in the `omnibox` (address bar) to open Chrome SearchEngine and add a new alias to the url you just probably just copied.


#### How to quickly add a new alias
1. In Chrome press `⌘ + L` mac, (`Ctrl + L` windows) to focus on the address bar.  
2. Copy link in omnibox (the link you like to have an alias for)
3. Write `na` in omnibox and press Enter
4. `SearchEngine` will open up, and you can press `Add` button, paste the link and add your alias for that link, and you are done.

### Some examples where I use aliases
1. Github
2. JIRA
3. Confluence
4. Google maps
5. Bookmarks
6. Pricerunner  

For example, now I only have to print this in the search box to quickly get my result:  
 
```
jira ticket-123  (will 
maps stockholm  
price bicycle
```