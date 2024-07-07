barf
----

barf is an extremely minimal blog generator.

The entire build script is >170 lines of shell.

It could *almost* be called "suckless", but probably isn't.

(barf is a modified/forked version of Karl Bartel's fantastic [blog.sh](https://github.com/karlb/karl.berlin). Be sure to check it out since 
my version does things slightly different.)

You can see a [live demo here](https://barf.btxx.org)

why 'barf'?
-----------

> **barf**
>
> blogs are really fun


core features
-------------

- Extremely portable
- Automatic, **valid** RSS generation
- Handles both blog posts and normal pages
- No front matter or templating, just create markdown files

requirements
------------

`barf` was originally built on and for Linux, but has since been 
updated to include support for both OpenBSD and MacOS out-of-the-box.

linux
-----

- rsync
- lowdown
- entr (optonal)
- standard UNIX tools

Example on Alpine:

    sudo apk add rsync lowdown

openbsd
-------

Please refer to the main tutorial on setting up barf on OpenBSD: 
https://barf.btxx.org/openbsd

- coreutils
- gcc
- cmake
- lowdown
- gsed
- entr (optional)

Example:

    doas pkg_add coreutils gcc cmake lowdown gsed

macOS
-----

Please refer to the main tutorial on setting up barf on MacOS: 
https://barf.btxx.org/macos

- coreutils
- gnu-sed
- rsync
- lowdown
- entr (optional)

Example:

    brew install coreutils gnu-sed rsync lowdown

basic setup
-----------

Clone this repo and navigate inside it. Edit the "header.html" 
and "footer.html" files with your own information, navigation, etc. 

Be sure to edit the **domain** variable inside `barf` or else your feed won't validate!

Then build:

    make build

Your blog content will be in the `build` directory.

Now you can delete the dummy posts/pages and start making your own!

Media (such as images, videos) are placed in the "public" folder and 
carried over to the "build" folder via rsync. You can easily remove 
this altogether inside the main `barf` script if you plan to store 
media elsewhere (or not use any at all).

post structure
--------------

The first line of any markdown file inside your `posts` directory 
should start with a h1 heading, then a line break, then the date 
in `YYYY-MM-DD` format.

Like so:


    # This is the Post Title

    2023-01-05


Changing this structure or date format will break things or require 
you to edit the `barf` script accordingly.

projects goals
--------------

- The core focus should be to **reduce** the code of this project, 
  not increase it. Overall scope needs to remain small.
- Major tweaks/add-ons should be run by individuals via forks/patches, 
  not put into the barf base

submitting patches
------------------

Please send me patches via git email: barf@patches.btxx.org

Thanks!


FAQs
----

## How do I test locally?

Inside your project directory run:

```sh
make watch
cd build && python3 -m http.server 3003
```

## Do you plan to add "X"? Can *I* add "X"?

Most likely not. I'm happy with how things are currently. If you 
want to add something - great! The point of this project is to give 
others the ability to fork it, tweak it, patch it, and share it as 
much as they'd like. The core of barf will remain minimal for this reason.

Of course, any patches that can help *reduce* the project's footprint 
or even speed things up are more than welcome!

## Can I use other Markdown parsers?

Of course! Simply edit the main `barf` script and swap out `lowdown` with 
something else. I wouldn't advise doing this if you already have pre-existing 
content based-off `lowdown`, since this could break some of your pages.

But give `lowdown` a try - it is very lightweight and fast!


MORE FAQs TO COME...

