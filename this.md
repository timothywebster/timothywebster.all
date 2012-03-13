---
layout: default
title: this website
---
#This Site
A long time ago I needed to pick a web content management system for a client, and I picked drupal. I don't think there is a one-size-fits-all CMS that everybody can use for everything, and the client already had a few php guys on board, so drupal seemed like a pretty good fit. One nice thing about drupal is that it has a big enough community that if your client wants to learn how to administer or customize the site, she can go to the store and buy a book, or find a consultant on the internet, or whatever. When I am buying services, I do not like vendor lock-in, and I don't try to force my clients to come to me for changes. 

It turns out there were more people nearby who needed drupal stuff, and I am the kind of agreeable freelancer who goes where the work is. So I built some more even drupal sites, and with so many instances around it was handy to use it my own stuff in drupal.

I am not going to trash talk drupal here. It's good for a lot of use cases, but also requires a lot of plumbing for features that I will not use. All of my pages are visible to the public, I don't have users who sign in and post their own content, etc. So I thought about what I really wanted to do:

- write content in markdown
- wrap that content up in some kind of template
- create static exports, so that I could build phonegap applications (or offline html5, or whatever)
- do my workflow with my own source control, rather than using some kind of baked-in, tool-unfriendly proprietary system

So, I googled on *markdown, template, export* and *git,* and found [Jeckyll](https://github.com/mojombo/jekyll), which is exactly[^foot]  what I thought I would write myself if I were starting from scratch. I knew I was on to something when I saw that there was already a community of very smart folks using it. The Internet is good like that. 

[^foot]: I don't think I would have done it in ruby, but that's hardly a dealbreaker. 

Anyway, [here's the source](https://github.com/timothywebster/timothywebster.all) if you're interested.
