# Running `barf` on MacOS

2023-01-18

The `barf` project was built on Linux and was catered towards Linux users. The core of the project will remain focused on Linux/GNU tools, but that doesn't mean MacOS needs to be left out in the cold.

## Download Packages

This walkthrough assumes that you already have [homebrew](https://brew.sh/) installed on your machine.

You will need to install the GNU versions of both `date` and `sed` in order to avoid breaking things when `barf` tries to build.

    brew install coreutils
    brew install gnu-sed

Now everything should work as intended!
