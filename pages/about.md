# About this site

I wanted a simple site to showcase what I've done, mainly for myself to remember in the future.

## How it's built

All the hard work was done by Bradley Taunt and his website generator [barf](https://barf.btxx.org).

This website is hosted on GitHub pages using an [actions workflow](https://github.com/vlad-sharpie/website/blob/main/.github/workflows/ci.yml). It's very simple but means in the future I can just write a blog post in one file, push it to the repo and the changes will be live in under a minute.

I also got it to switch between a dark and light theme based on your OS choice, though my firefox doesn't seem to respect it, so that's great.

```
<meta name="color-scheme" content="dark light">
<style>
    body {
        transition: background-color 0.3s, color 0.3s;
    }
    /* Default to light mode */
    body {
        background-color: white;
        color: black;
    }
    /* Dark mode */
    @media (prefers-color-scheme: dark) {
        body {
            background-color: black;
            color: white;
        }
    }
</style>
```