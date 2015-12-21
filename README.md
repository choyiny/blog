blog.choyin
==========

### Introduction
This repo serves as a host for my blog at [pages.choy.in](https://pages.choy.in) This blog is made for a task in Google Code-in 2015 for FOSSASIA.


### Credits
[Hugo](http://gohugo.io/), a fast and modern static website engine

[Hyde](https://github.com/spf13/hyde), the best Hugo theme imo

### Tutorial

#### Download and install Hugo
This is a relatively easy task if you have a mac and [Homebrew](http://brew.sh/), which you can install with a single command in terminal. After installing homebrew, type this command into terminal:

```
brew install hugo
```

Wait for a few seconds and you've done it! Alternatively you can download the software packages of Hugo for other platforms such as Windows (not as pro) or Linux [here](https://github.com/spf13/hugo/releases).

#### Creating a repository on Github
I created an empty repository on github named "blog". This will ensure your blog will be acccessible at http://[username].github.io/blog. Alternatively you can create a new repo (if you don't have one) named [username].github.io, then, your blog will be directly accessible at http://[username].github.io. My repository can be viewed [here](https://github.com/hkminegod/blog), and website [here](https://pages.choy.in/blog).

#### Preparing the workspace
Make a new file in the blog directory called 'config.yml' with the following plain-text using a text editor such as textedit or brackets: (make sure there are no tabs)

```
---
baseurl: "http://[username].github.io/blog"
title: "my blog"
permalinks:
  post: /:year/:month/:title/
params:
  Subtitle: "Tu etais formidable"
  description: "this is my blog"
  AuthorName: "choyin"
  GitHubUser: "hkminegod"
  SidebarRecentLimit: 5
---
```

Edit parameteres to your own likings, save and exit the file. Next, create two folders. One inside the root folder named `content`, and one inside `content` named `posts`. All your blog posts will be put in the folder `posts`.

#### Blogging with a theme
Now, let's choose a theme for your blog! Hugo itself does not have any capability to create a website from nothing, so choose a nice looking theme from their official [Theme Showcase](http://themes.gohugo.io/) For me, I downloaded [HYDE](http://themes.gohugo.io/hyde/) to work with, because I thought it was great.

Make a new folder `themes` and put the whole theme folder there.

#### Your first post
Hugo makes it very easy to create a blogpost. Just make a markdown file named anything, and put it under `root/content/posts`. I like to make the file name the date, like so: `20151221.md` For the contents on the file, paste in this and adjust to your likings:

```
---
title: "Hello world!"
date: "2015-12-21"
description: "I am a description"
categories:
    - "tutorial"
    - "hugo"
---
This will house the contents of your post, formattable in markdown.
```

#### Deploy Hugo on Github
Using terminal, navigate to your blog root directory. For beginners that is not familiar with terminal, here is an example:

`$ cd workspace/blog`

Basically what this does is point terminal to the folder `workspace` and then `workspace/blog`. After that, type in terminal

`$ hugo server --watch`

It will output a bunch of stuff, along with a line like this.

```
Web Server is available at http://127.0.0.1:1313/blog/
```

Using any browser of your choice, navigate to that link and you will be able to see if your blog works! If you like it, type this last command in terminal (replace hyde with your installed theme):

`$ hugo -t hyde`

Using commandline or [Github Desktop](https://desktop.github.com/), push the `public` folder to the blog's `gh-pages` branch. I personally find Github Desktop less confusing for beginners, but using the command line has multiple advantages as well.

You're done! Your site will be live momentarily at http://[username].github.io/blog! Congratulations, that was easy!

#### Extras
If you have a custom domain like me, you can point your repository to your own domain using a CNAME. Create a new file called `CNAME` in your repository's root folder, and put your domain name in the file. For me, it is `pages.choy.in`. Modify the CNAME in your domain's DNS records and make sure that domain points to `[uesrname].github.io`
