---
layout: page
title: Setting up an Academic Website
permalink: /resources/academic-website/
---

When I first set out to build my website, I set out and built it from scratch using html and bootstrap. 
This process became quite cumbersome to make updates and everytime I added a new page I had to update every pages navigation bar. 
It quickly became unscalable! I decided to scrap the idea after only four months and I fell back on an old favorite: Jekyll. 
I now can make updates quite quickly and use my favorite markup language markdown!

Rather than start from scratch I did a brief "literature survey" and found the following 
[page](http://svmiller.com/blog/2015/08/create-your-website-in-jekyll/#advantages) describing how to make an academic 
site with jekyll. I forked his github repo and modified it to fit the lovely UMass branding. I plan to add some modifications for the publications 
and cv sections of the site but for now the two templates are virtually identical. Feel free to refer to that page for additional hints and assitance. 
You can also ask me any questions! 

Now to the fun part! Below I give a brief and slightly disorganized rundown of how to copy the template, modify it, and then 
a little background on how the process works.



# Deploying the website for yourself.

## Make a copy for your own repo. [Source](https://help.github.com/articles/duplicating-a-repository/)

1. Create the github repo you wish to use for your website. For our examples we will use `mrlucasch.github.io`
2. Clone the github template repo.

```
git clone --bare git@github.com:mrlucasch/umass-website-template.git
```

3. Mirror-push to the new repo (your repo):

```
cd umass-website-template.git
git push --mirror git@github.com:mrlucasch/mrlucasch.github.io
```

## Customizing your website.

### Modify \_config.yml to control sitewide data
This file holds most of the generic site_wide settings for your jekyll site. It controls the domain name as well as some generic data.

1. Modify the title. This is the title that will appear at the top of your page.

```
title: Lucas Chaufournier
```

2. Add your email.

```
email: lucasch@cs.umass.edu
```

3. Edit the description. This appears at the bottom of the webpage on every page. You can include some basic info about yourself or 
pretend to be witty/cultured and include a famous quote.

```
description: > # this means to ignore newlines until "baseurl:"
  "It is one of life's bitterest truths that bedtime so often arrives just when things are really getting interesting." -- Lemony Snicket
```

4. For `url` place the domain name for your website. For github pages this will be `mrlucasch.github.io`:

```
url: "http://mrlucasch.github.io"
```

5. Add your twitter_username if you feel so inclined:

```
twitter_username: lucasch
```

6. Add your github_username if you wish:

```
github_username:  mrlucasch
```

7. Feel free to modify your job title:

```
job.title: "Graduate Student"
```

That is it for the ```_config.yml``` file.

### Modify \_data/menu.yml to add Navigation links to the top.
This file contains the site layout for your webpage. It determines the links that appear in the main navigation bar.
Links are in the order that they will appear. Feel free to add more as you wish and remove others. Be mindful of spacing as yaml can be quite particular.

`href` is used to point to the markdown file for that link. The content for about would be located in about.md in the root directory. The content for item-1 is located in item-1.md in the folder resources.

If you want to have submenus, then you can follow the example of the resources page. To creates subfolders, just make a subfolder in the root directory with the parent link and add pages as necessary.


## Changing site content.
To change the content of each page you need to edit the corresponding markdown files. I break down the different pages below:

### index.html
This file contains the information you see on the main page when people navigate to your site. It is good to put a brief overview of yourself, your research, and 
selected publications. Also include an image of yourself so people know who you are!

To replace the default octocat, place your image in your /images/ folder and then modify the following line with the correct file name:


{% include image.html url="/images/image_code.png" caption="Image Embed Code." align="center" %}


FYI: This site does not accept markdown unlike every other page we will work with.



### about.md
This file contains more detailed information about you and your history. It is not as detailed as your full family tree but maybe include where you went to undergrad and 
some of your non-cs related hobbies. Feel free to find a happy medium between the start of time and just putting "I'm at umass". 
Don't be afraid to let your personality shine through!

You should also replace the octocat on this page. You can use the same boring picture that you do on your front page or you can spice things up with a 
picture of you skydiving or looking over some broad landscape. I don't know, you do you! This is just what I've seen more "seasoned" academics do.

### blog.md
This represents your blog and should not be altered much. Feel free to alter the Title at the top of the page to something more fun than "Blog". 
Also you can edit the tagline from:

```
Tell us about your blog. Hopefully it's cool.
```

to something more interesting. Leave the awful code there.

You may be wondering where the blog posts come from? Great Question! 
They are automatically pulled from the \_posts folder. We will go over that once we are done customizing the website.

### research.md
This is where you should really let your passion shine through. Go crazy and talk all about your research interests. 
Discuss what you are working on currently, where your passion for it comes from, and where you hope to push your research in the future. 
Really motivate the problems you are working on.

This is also a good place to put your full publications. If you are a superstar student and have boatloads of papers already 
then you may wish to break it off into its own page or subpage. See the menu.html section to figure out how.

### paper1.md
This page can be used to display your papers in a more presentable way. It includes a section for your abstract, as well as embedding your paper and containing the bibtex for your page.


### cv.md
I am a little torn on my feelings toward this page. Currently it just embeds a pdf from dropbox and allows you to download said pdf.
 I would rather it be an html version of your cv with a link to download the pdf version. 
 I am working on a way to do this but styles in css are painful so for now we are stuck with this version. 
 I will send an update when it is up and working.

You may be wondering how to get the pdf part working. Simply upload your cv to dropbox and then create a shared link of the form 
`https://www.dropbox.com/s/ALPHANUMERICSTRING/fname.pdf` Then replace mine in the template. Easy as pie.

### resources.md and its subpages
This is for any misc information you wish to provide. I usually have 1 or 2 tutorial pages on how to use a technology that I need to reference all the time.
 You can see on my page I have reference guides for tmux, kvm, lxc, etc.

This is also a good place to keep pages about advice for others or links to good papers on how do things. 
This is totally up to you. If you don't feel like sharing with the world then simply remove it and edit the menu.yml page above.

## How do I add blog pages?
To write a blog post you simply need to create a new file in the \_posts folder. The filename should be of the form YYYY-MM-DD-post-title.markdown.
The file should start with the following header information:
<pre><code>
---
layout: post
title:  "Welcome to Jekyll!"
date:   2015-08-16 15:36:27
categories: post1 mptcp
---
</code></pre>


Make sure the layout says post. The Title should be the title of your blog post. The date should be the current date. Feel free to add any categories you wish. 
Then add your blog post content after the ```---```. Your post can consist of any markdown syntax. Feel free to check out the sample posts or the posts on my webpage.

## Activate Github pages for your repo

1. Navigate to your websites github repo
2. Click on settings.
3. Scroll down to `GitHub Pages`
4. Under source, select the `master branch` and then hit save.
5. Access your website from GITHUBUSERNAME.github.io


## Redirect from UMass CSCF Page 
You may find that you want to redirect your official CS page from umass to your github repo. This is a very easy process.

1. First log into loki.cs.umass.edu with your cs account
2. Navigate to your public_html folder.
3. Create a file titled .htaccess and place the following content into it:

    
    <pre><code>
    RewriteEngine on  
    RewriteBase /  
    RewriteRule ^(.*)$ http://mrlucasch.github.io/$1 [L,R=301,NC]  
    </code></pre>

    *Be sure to replace the `mrlucasch.github.io` with your github page address. Make sure to leave `/$1`*

4.  Change the permissions on the .htaccess file:

```
chown CS_USERNAME .htaccess
chmod 644 .htaccess
```

*Replace `CS_USERNAME` with your cs id.*

# Displaying your research papers on your website.

If you have perused my website you may have noticed I have a unique way of displaying my research papers. 
I like to provide an easy way to view my research and have everything in one place (including slides, bibtex, pdfs,datasets, etc.)
You can see an example [here.](http://itsalgorithmic.com/research/containers-vms/)

If you are interested in doing something similar, reach out to me and I can fill you in on how to structure and create something similar for your research.

To include your papers in a similar fashion you can do the following:

1. Open `/_includes/embedpaper.html` and replace the `GITHUB-URL` with your github page url.
2. Navigate to `/research/`. This directory will hold all of your papers. 
3. The initial repo has a template for how papers and pdfs should be structured. For each of your 
papers, you should create a directory inside of `/research/` that holds the pdf copies of your paper and slides. In the repo
this is the paper1 directory. You should then create a markdown file for the paper, a sample is provided named paper1.md.
4. Inside of `paper1.md` you should do the following:

Replace all references to GITHUB-URL with your github url. You should also modify those url's with the 
directory for your paper and the name of your pdfs. So in this case the url refers to the paper1 directory and the slides.pdf and paper.pdf files. 

At the top of the page you should repalce `TITLE OF PAPER` with the title of your paper.

Under Abstract, place the abstract for your paper.

Modify
  ```
 code="paper1/paper.pdf"
  ```
  so that `paper1/paper.pdf` points to the directory you created and the pdf of the paper.

Modify 
```
code="paper1/slides.pdf"
```
so that `paper1/slides.pdf` points to the directory you created and the pdf of the slides.


Under Bibtex, place the bibtex for the paper between the `<pre><code>` and `</code></pre>` sections.

Now when you link to a copy of your paper, you can link to `/research/paper1` (note paper1 is the name of the markdown file not the directory) and nicely display your research.

---

# Maintaining an Open Research Notebook



I have recently added the optional ability to host an open research notebook. An example is [here](http://mrlucasch.github.io/notebook). This page functions similarly to the way the blog page works except it is more specialized.
To use the open notebook feature, open the `_data/menu.yml` file and uncomment the following:

```
  - title: "Research Notebook"
    href: "/notebook"

```

This will add a menu entry that points to the notebook page. The notebook page has the exact same functionality as the 
blog page except that it only displays pages with the `notebook` tag. To create a new entry, create a new file in the `_posts` directory
in the same manner you would a blog post. An example post is included already titled `2017-01-01-weekly-template.markdown`. To have the post appear
in the notebook, under categories just append the `notebook` category and it will automatically be included. It is up to you how you want to format it,
but I generally included tasks I have completed, any results, and how to's related to my research. Feel free to modify the template as you see fit. 

