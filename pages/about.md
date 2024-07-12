# About this site

I wanted a simple site to showcase what I've done, mainly for myself to remember in the future.

## How it's built

All the hard work was done by Bradley Taunt and his website generator [barf](https://barf.btxx.org).

This website is hosted on GitHub pages using an [actions workflow](https://github.com/vlad-sharpie/website/blob/main/.github/workflows/ci.yml). It's very simple, but means in the future I can just write a blog post in one file, push it to the repo, and the changes will be live in under a minute, let's hope I start making some posts!

I made it switch between a dark and light theme based on your OS choice, though my GNOME theme doesn't seem to respect it, so that's great. If you're using the dark theme, then the link colours are plucked from GitHub's palette. Also the markdown interpreter, [lowdown](https://github.com/kristapsdz/lowdown), has been changed to allow inline HTML to passthrough:
<marquee>so I can do fun stuff like this</marquee>