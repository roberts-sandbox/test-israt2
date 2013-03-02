---
layout: post
title: "Setting up Octopress and Github for blogging."
date: 23 August 2012
comments: false
categories: Blogging
---

Finally I setup my octopress blog. I had some pain initially but once after I solved the issues, I found it's pretty simple and stable. Mind it, it's hackers way of blogging. You won't have the luxury of what blogger and wordpress offers but this has got highest amount of flexibility on your content.

All the following instructions are detailed well in the [Octopress Documentation Page][5]. This is kind of excerpt/fundamental setup I went through to setup the blog.

### I am no Ruby Developer ###
This was the hectic part. As usual I started with Windows, and realized that it's really painful. I tried installing Rails Installer and Ruby Installer. It was so painful to setup the rbenv and gem installer mentioned in the Octopress setup page. Even using Cygwin could not help me to move further. So I went ahead with Linux VM installed locally in my Windows machine

### Ubuntu Linux - The choice ###
It's really heaven. I was able to work well with the instructions mentioned in the Octopress setup. Also I realized not to call myself as a hacker without a linux box.

### The setup ###
Github allows you to setup your own homepage by creating a respository with your username. `github.com/username/username.github.com` (replace username with your username). 

Also you can setup as a project page with any of the projects you create with GitHub. What I am explaining here is setting up GitHub homepage as a blog.

### Installing Ruby ###

 1. Check your ruby version first with `ruby -v` if the version is less than 1.9.3, [then follow the instructions to update the ruby version][2]

 2. Clone the Octopress source from GitHub. `git clone git://github.com/imathis/octopress.git octopress`

 3. Move to octopress folder `cd octopress`

 4. Execute the following commands

`
    gem install bundler
    rbenv rehash    # If you use rbenv, rehash to be able to run the bundle     command
    bundle install
`

 5. Now you're done with the default theme. Follow [the instructions mentioned in the setup page][3]

`rake setup_github_pages`

This is for username.github.com repository. For a other normal the setup is different and mentioned in the same page mentioned above.

 6. This is the most important step which we should understand

`
rake generate
rake deploy
`

Octopress is the repository cloned from a different user. Now this is your fundamental setup. The scripts and Jekyll frame work help you to generate the pages and push to your own repository. on rake deploy command, it will ask for the repository to push the generated files. All the actions are automated. You really don't need to bother about git commands just give the URL and the necessary changes will be made within the repository and the generated changes will be pushed. All you need to specify the git repository when prompted. The format will be mentioned in the prompt itself.

### The source branch ###

The previous help you deploy the static pages, now you want your original framework and posts you created like a database backup. Hence add all the files

`
git add .
git commit -a -m 'first commit'
git push origin source
`

This will push your original data to a source branch in repository. i.e the master contains the pages you generated and source branch is your template to generate them.

### configuring the blog ###

[See the configuration instruction here.][4]

The most important thing you've to notice is that, while adding twitter handler or Google analytics tracking code, please leave a space after ':' otherwise the page generation will fail.

### Basics of blogging ###
[The blogging basics are shared in detail at Octopres pages][5]

Note that whatever the file you add using rake new_post["title"] must be added separately to your archive and pushed to source for backing up. using rake gen_deploy will regenerate the pages and pushes to the archive.


  [1]: http://octopress.org/docs/
  [2]: http://octopress.org/docs/setup/rbenv/
  [3]: http://octopress.org/docs/deploying/github/
  [4]: http://octopress.org/docs/blogging/
  [5]: http://octopress.org/docs/blogging/
