# Quality of Life Improvements

2024-06-06

I haven't circled back to `barf` in quite a bit of time, so I'm happy to announce a small update mainly focused on quality of life improvements! I'll keep things brief and get right into the core changes:

**Automatic detection of your operating system (supports Linux, macOS and OpenBSD currently)**

* `barf` now checks your current OS and sets aliases accordingly
* this removes the need to hard-set your own aliases or run syslinks

**Added a semantically valid RSS feed**

* `barf` initially launched with Atom support only, now a separate RSS feed is generated at build time

**Removed hardcoded feed links from `header.html`**

* You now only need to set your main domain at the top of the core `barf` file.

**Swapped out `smu` for `lowdown`**

* The default Markdown parser is now set to `lowdown`. The original parser (`smu`) is great, but I wanted to make the project simpler by avoiding users to clone and build a separate package.

That's it really! I've also updated the original blog posts about setting up `barf` on macOS and OpenBSD to reflect these changes.

Cheers!
