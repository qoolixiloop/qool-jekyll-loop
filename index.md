---
layout: default_
title: Home
---
#{{ "Hello World!" | downcase }}

##{{ "Solution of the official step by step tutorial on Jekylls website"}}

###I added five features
- The Theme {{site.theme}}
- Make navigation links look like buttons
- A nicely rendered tutorial summary 
- A new author: Qool ixi Loop
- Some infos about me, and a donate button


###Steps to make the theme {{site.theme}} work</h3> 
 In order to make the theme work I added to `_config.yml` the line `theme: jekyll-theme-hacker` and changed the name of our `_layouts/default.html` file to `_layouts/default_.html`. To the front matter of the file `_layouts/default_.html` I added  `layout: default`, which is the template file in the gem `jekyll-theme-hacker`.

If you are wondering, how the theme's css gets loaded please read on. The entry in `_config.yml` is just a `key:value` pair, which is used in a file `assets/css/style.scss` to import the theme's css with  `@import "{{site.theme}}";` If we rename the file e.g. to `assets/css/style_.scss`, we can remove the import because then the theme-gem's file `assets/css/style.scss` is loaded, which has the same import in it. But the `assets/css/style.scss` file is loaded in the first place, because the gem's `_layouts/default.html` and our `_layouts/default_.html` contain the following line `&ltlink rel="stylesheet" href="/assets/css/style.css"&gt`


###Code to make navigation links look like buttons
I added css classes to file `_sass/main.scss` and used them in `_includes/navigation.html`

###Please visit the nicely rendered tutorial summary
It is available by clicking the navigation button `blogs`

<p align="center">
<a href="https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=ZJSNJNBGL8MVE&source=url" target="_blank">
  <img src="https://www.paypalobjects.com/en_US/CH/i/btn/btn_donateCC_LG.gif"/>
</a>  
</p>

------------------------   
qoolixiloop, 24. Jan. 2019 






