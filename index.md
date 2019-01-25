---
layout: idefault
title: Home
---
# {{ "Hello World!" | downcase }}

## Enhanced solution of the official step by step tutorial on Jekylls website

### I added five features
- The Theme {{site.theme}}
- Make navigation links look like buttons
- A nicely rendered tutorial summary 
- A new author: Qool ixi Loop
- Some infos about me, and a donate button


### Steps to make the theme {{site.theme}} work 
1. **Copy the default file and do some renaming:** I renamed *_layouts/default.html* to *_layouts/idefault.html* and copied/pasted the *_layouts/default.html* from the {{site.theme}} in it. Then I changed the front matter of all files, which required *layout:default* to *layout:idefault*. I tried to keep 
2. **Add css for navigation and do some renaming:** I renamed the file *assets/css/style.scss* to *assets/css/main.scss* and the file *_scss/main.scss* to *_scss/navi.scss* in order to make clear that the *_sass* folder holds the snippets, which are imported into *assets/css/main.scss*. The latter will be included into the head-tags of the compiled html files.
3. **Make all links relativ:** In order to work on github project pages and not only on localhost and on github user pages, relative link variables or filters have to be included everywhere. For ankers like so: `<a href="{{ site.baseurl }}{{ author.url }}">` and for the css file added to the header like so: `<link rel="stylesheet" href="{{'/assets/css/main.css'| relative_url}}">`. I also output all link variables to the pages, because all these frameworks are very smart in defining rules to split up the files. But if you are not familiar with the magic that's used to put them together during compilation, you probably want to see in an example what's stored in the variables.  
4. **Change value of key-variable baseurl:** In *config.yml* we had `baseurl:""` when we worked on localhost or when we pushed to github's user pages. But if we use github's project pages we need to change the key:value pair to `baseurl: "</repository_name>"`.
5. **Starting server locally:** With all those changes the server starts at *http://127.0.0.1:4000/{{site.baseurl}}/*. To work on github project pages *gh-pages branch*, no changes are needed. The localhost is automatically replaced with *https://qoolixiloop.github.io*.

<br>
  
<p align="center">
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZJSNJNBGL8MVE&source=url" target="_blank">
  <img src="https://www.paypalobjects.com/en_US/CH/i/btn/btn_donateCC_LG.gif"/>
</a>  
</p>

------------------------   
qoolixiloop, 24. Jan. 2019 

