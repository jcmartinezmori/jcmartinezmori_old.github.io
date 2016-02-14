#Read Me

I thought Balzac was a wizard's name. So when I forked and tweaked [Cole Townsend's](@twnsndco) Balzac for Jekyll theme I named it Fairytale. It's a theme which is heavy on typography. I did little modification to the home page. But I took my liberty with the rest. Fairytale is my first theme for jekyll. I didn't change the layout more than was necessary since I intend the theme to reflect Balzac in functionaliy. 


## Features
- A few typographical eye candy
- MathJax
- Plus all inherited features from Balzac


### Features: derived
- flexible, uses max-width for responsive goodness
- responsive drop down menu
- retina images using @2x
- post loop in the footer showing 3 latest posts
- custom portfolio page for case studies

## Basic Setup

1. [Install Jekyll](http://jekyllrb.com) if you haven't already.
2. Download this bad boy.
3.  Fork the [Fairytale repo](http://github.com/username/fairytale-theme)
4. Twerk it out so it's just for you.
5.  ???
6.  Profit

## [Preview this Theme](http://espresso-math.github.io)
 
``` bash 
Fairytale-Theme/
├── _includes
|    ├── footer.html  //site footer
|    ├── head.html  //site head
|    ├── head-dark.html  //dark site head for light pages
|  ├── mathjax.html //mathjax configuration
|    └── typefix.html //a few typographical tricks
├── _layouts
|    ├── 404.html   //Edit the 404 file
|    ├── home.html  //homepage layout
|    ├── page.html  //page layout
|    ├── post-index.html  //post listing layout
|    └── post.html  //post layout
|    ├── post-no-feature.html  //feature image-less post layout
├── _posts
├── _sass
|    ├── _grid.scss 
|    ├── _mixins.scss
|    ├── _normalize.scss
|    ├── _styles.scss //This make the looks
|    ├── _type.scss
|    ├── _variables.scss //Fonts, Colors etc...
├── _site
|    ├── //Leave well enough alone
├── assets
|    ├── css  //preprocessed less styles. good idea to minify
|    ├── img  //images and graphics used in css and js
|    ├── js
|    ├── ├── main.js  //jQuery plugins and settings
|    ├   └── vendor  //all 3rd party scripts
|    └── sass 
|    └── mathjax //the mathjax files.
├── images  //images for posts and pages
└── 404.md //File not found page.
├── about.md  //about page
├── articles.md  //lists all posts from latest to oldest
└── index.md  //homepage. lists 5 most recent posts

```

## Customization

## _config.yml

Most of the variables found here are used in the .html files found in `_includes` if you need to add or remove anything. A good place to start would be to change the title, tagline, description, and url of your site. When working locally comment out `url` or else you will get a bunch of broken links because they are absolute and prefixed with `{{ site.url }}` in the various `_includes` and `_layouts`. Just remember to uncomment `url` when building for deployment or pushing to **gh-pages**...

### Owner/Author Information

Change your name, bio, Twitter url, email, Dribbble URL, etc.


### Top Navigation Links

Edit page/post titles and URLs to include in the site's navigation. For external links add `external: true`.

``` yaml
# sample top navigation links
links:
  - title: About Page
    url: /about
  - title: Other Page
    url: /other-page
  - title: External Page
    url: http://example.org
    external: true
```

##The **New** in Fairyland

### Post

You can enlarge the initial letter by emphasizing it like this,
``` html
*"W*hen, where, wtf?"
```

###Note on Typography

The body text is in `Stempel Schneidler Light Medium`. The question mark `?` is upside down. Just fix this by replacing each ? with `<span class = "question-mark">?</span>`.

Most people don't realize this, but <span style = "font-style:italic;">this text</span> is not in italic but in oblique type. There's a big difference. Oblique text is rendered by the browser by slanting the original font. But italic is an entirely different typeface. If you want <span class = "nice-italic">italic</span> instead of oblique use `<span class = "nice-italic"></span>`. Fairytale use `Palatino Linotype` for italic.

The post heading and other sans text is in `Alte Haas Grotesk` ( separate typeface for normal and bold text ). On smaller screens the enormous post heading in `100pt` text might be too large and partly hidden. Although on smaller screens the fontsize automatically reduces to `50pt` you might want set `display_title` in you `post.md` file to a smaller, more readable title.

``` yaml
---
layout: post
title: Really long title
display_title: Bite Me
---
```

If you look at the lower right corner of the webpage you'll find a standalone quote there. You can set this in a post or page using `quote`,
``` yaml
---
layout: post
title: A really simple title
quote: "You must jump of a cliff before you can start living."
---
```
You can change the default quotation in the `_config.yml` file using the variable `quote`.

###Typefix

You can indent the first line of every paragraph by setting `indent: true` in the yaml frontmatter.
``` yaml
---
layout: post
typefix:
   indent: true
---
```

To make the text centered use `poetry: true` in the yaml frontmatter like this.
``` yaml
---
layout: post
typefix: 
   poetry: true
---
```

You can even combine both of them by,
``` yaml
---
layout: post
typefix:
   indent: true
   poetry: true
---
```

###Mathjax

Fairytale comes with support for mathjax, but only if you want it to. Add `mathjax: true` like this,
``` yaml
---
layout: post
mathjax: true
---
```


## Other Stuff

The rest is just your average Jekyll config settings. Nothing too crazy here...

### _includes

For the most part you can leave these as is since the author/owner details are pulled from `_config.yml`. That said you'll probably want to customize the copyright stuff in `footer.html` to your liking.

### Adding Posts and Pages

There are two main content layouts: `post.html` (for posts) and `page.html` (for pages). Both have large **feature images** that span the full-width of the screen, and both are meant for text heavy blog posts (or articles). 

### Feature Images

A good rule of thumb is to keep feature images nice and wide so you don't push the body text too far down. An image cropped around around 1024 x 256 pixels will keep file size down with an acceptable resolution for most devices. 

``` yaml
image:
# local image 
  feature: feature-image-filename.jpg
# link image
  feature: "http(s)://image.domain.com/feature-image-filename.jpg"
```

This makes the assumption that the feature image is in the *images* folder unless it has a link address. To add a feature image to a post or page just include the filename in the front matter like so.
You can "serve" images responsively with retina.js. All you need to do is have a file with @2x before the file type. That should be placed in the *images* folder. You literally don't have to do anything other than that. 2 copies. One is linked. That's it.
Ex:
`cool-photo@2x.jpg` 

**There is a default feature image that will show up for and posts. It isn't retina or anything. It's just there in case you want one but forget <3*

#### If you don't want a feature image
…just say so in the front-matter. Go to your-post-name.md and make sure it has this guy up top.
``` yaml
layout: post-no-feature
```

### Categories

In the sample `_posts` folder you may have noticed `category: articles` in the front matter. I like keeping all posts grouped in the same folder. If you decide to rename or add categories you will need to modify the permalink in `articles.md` along with the filename (if renaming).

For example. Say you want to group all your posts under `blog/` instead of `articles/`. In your post add `category: blog` to the front matter, rename or duplicate `articles.md` to `blog.md` and change the permalink in that file to `permalink: /blog/index.html`.

If done correctly `/blog` should be a page listing all the site's posts.


## License

This is free to use, fork, do whatever you want. 
