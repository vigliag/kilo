## Annotated Kilo

This is a version of Kilo with additional comments/annotations. It is aimed at making Kilo's source a good first introduction to real-world C code.
There's still a lot to improve in these annotations (this is pretty much an initial version), contributions are very welcome!

The additional comments are the single-line-styled ones `//`, original comments are the multiline-styled ones `/*`.

You can use [docco](https://jashkenas.github.io/docco/) to render an html version of the annotations

```bash
$ sudo npm install -g docco #installs docco (you'll need to install nodejs first)
$ docco kilo.c # it'll create a docs/html/ folder with the rendered documentation
```

There are a few bugs in the code (I'm using the uncorrected version of Kilo as it was originally published). These bugs are marked as such in the comments, but not corrected. Readers are incouraged to try building and running kilo themselves, and see if they can spot the bugs using debuggers and tools like valgrind or address-sanitizer.

You can read more about kilo in [antirez's blogpost](http://antirez.com/news/108)

## Original Readme

Kilo is a small text editor in less than 1K lines of code (counted with cloc).

A screencast is available here: https://asciinema.org/a/90r2i9bq8po03nazhqtsifksb

Usage: kilo `<filename>`

Keys:

    CTRL-S: Save
    CTRL-Q: Quit
    CTRL-F: Find string in file (ESC to exit search, arrows to navigate)

Kilo does not depend on any library (not even curses). It uses fairly standard
VT100 (and similar terminals) escape sequences. The project is in alpha
stage and was written in just a few hours taking code from my other two
projects, load81 and linenoise.

People are encouraged to use it as a starting point to write other editors
or command line interfaces that are more advanced than the usual REPL
style CLI.

Kilo was written by Salvatore Sanfilippo aka antirez and is released
under the BSD 2 clause license.
