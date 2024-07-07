# barf

**barf is an extremely minimal blog generator.**

The entire build script is >170 lines of shell.

It could almost be called "suckless", but probably isn't. It was created for those focused on writing, not tinkering.

You can learn more by reading the [official README](https://git.btxx.org/barf/about).

**barf** = blogs are really fun

---

### Get setup in 2 minutes

**Install dependencies:**

For Linux (Alpine example):

    sudo apk add rsync lowdown coreutils

For macOS:

    brew install rsync lowdown coreutils gnu-sed

For OpenBSD:

    doas pkg_add lowdown coreutils gsed cmake gcc

**Clone barf:** 

    git clone https://git.btxx.org/barf

1. Open project, change the `domain` variable at the top of the core barf file
2. Run: `make build`
3. Upload the contents of `build` to your server! 
4. Profit?

---

### Articles
