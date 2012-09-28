---
layout: post
title: "GitHub blogging made easy with Windows"
date: 2012-09-28 13:35
comments: true
categories: Blogging
---

I rethought about after the previous post I made about blogging fundamentals with github. I am lazy and tackled it better now! I learned the art of copying and make it happen rather than taking up all the pain to generate someone else created (using [Octopress](http://octopress.org/))

In the previous [post](http://sarat.in/Blogging/2012/08/23/setting-up-new-octpress-with-github-for-blogging.html), I explained about setting up a github blog with Octopress. Octopress is an excellent framework over github Pages ([Jekyll](https://github.com/mojombo/jekyll)).

But setting up ruby, gems, rakes etc are not so easy with Windows. It's not really impossible but as you know the open source world and 

### I am no Ruby Developer ###
I am reinforcing this point. I am no ruby developer and not big understanding on the frameworks and the tools coming with Ruby. I am in the process of learning it.

### Ubuntu Linux - The tough choice ###
It's really heaven for programmers, I mentioned in the previous post! Whatever you need simply works there, just matter of few commands. Not really painful like windows to set it up. I am not a full time Linux desktop user. So it's expensive to spawn a Linux Virtual machine whenever I need to make a post. So I wanted to throw away my own itch!

### The setup ###
*This is fundamental, GitHub allows you create your own blog based on a github repository*. Plus they provides, a custom domain mapping to your blow as well. github pages implemented using Jekyll, a blog aware static site generator tool created by the founder of github, [Tom Preston-Werner](http://tom.preston-werner.com/)

Your own homepage can be created with your username[there are other variations as well, like pages for the projects but let's focus on personal blog). `github.com/username/username.github.com` (replace username with your username). 

### The windows way to work with Jekyll ###
You're no more hacker, just blindly do this!

### Pre Requisites ###
 - [RubyInstaller for Windows](http://rubyinstaller.org/)
 - Ruby [Installer DevKit](http://rubyinstaller.org/) (go to the end of the the page you can find a 7-Zip self extracting archive
	
### Setup ###

 - Install both the per-requisites. Better opt for `C:\DevKit` for the installation. Or choose a place where you can easily remember

 - Open command prompt and navigate to the toolkit installation location (mostly `C:\DevKit` ) and execute the following commands

    	ruby dk.rb init
    	ruby dk.rb install

Now execute the following commands as well to install Jekyll

	gem install jekyll
	gem install RedCloth
	gem install rdiscount	

NOTE: If you're accessing Internet via the proxy, please set `HTTP_PROXY` variable as follows

`set HTTP_PROXY=http://proxy:port/`

### Now Steal the code ###

You can use github for windows to easily clone the repository to your local machine.

You can fork the code from [mojombo.github.com](https://github.com/mojombo/mojombo.github.com). Check the copyright information before using.

Alternatively, there's a clean version of Tom Preston's theme which can act as the [bare minimum template](https://github.com/xpaulbettsx/blogstrap) for your github blog


### Setup repository on github ###
Go ahead and create your repository on `github.com` with the name `username.github.com`

Now copy the forked blog code to your local archive and I am really shame on you if you don't delete the whole posts created by the users who made the original blog. You can navigate to the _post folder and delete the old posts. 

### Basics of blogging ###
I prefer hand written posts with some simple text editor. Navigate to _post folder and create a .md file with the following format as file name

`YYYY-MM-DD-Post-title.md`

e.g
`2012-09-28-Easy-Way-to-setup-blog-with-github-on-windows.md`

[The whole goodness of Jekyll based blogging you can learn here](https://github.com/mojombo/jekyll)

Happy blogging!

### Thanks ###
Finally thanks a million to [Zach Holman](https://twitter.com/holman) for the interesting conversation happened over twitter. [Paul Betts](https://twitter.com/xpaulbettsx) helped to lead to the bare minimum setup he made from [mojombo.github.com](http://mojombo.github.com)
