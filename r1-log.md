# #100DaysOfCode Log - Round 1 - Dan Yeaw

The log of my #100DaysOfCode challenge. Started on January 13, Sunday, 2019.

## Log

### Day 1: Jan 13 Sunday

**Today's Progress:** Completed PyBites Code Challenge 1 -
Word Values Part I

**Thoughts:** PyBites uses unittest, I'm going to convert everything to
pytest to learn that more. For my initial solutions, I manually summed
and found the max using for loops, so I learned that sum() and max() can
simplify my code. I read Trey Hunner's new post on
[pathlib](https://treyhunner.com/2018/12/why-you-should-be-using-pathlib/),
which was really good, but I ended up just using a simple `with open()`.

**Link to work:** [PyBites 1](https://github.com/danyeaw/pybites-challenges/commit/3c08c17676ff9fc4aa3d6d7c5ed4d6ee9ddc79f8)

### Day 2: Jan 14 Monday

**Today's Progress**: Completed PyBites Code Challenge 2 -
Word Values Part II - A Simple Game

**Thoughts:**: Great practice for working with lists and sets including
appending, removing, and removing values. I learned about the `yield from`
keyword as well when using itertools. 

**Link to work:** [PyBites 2](https://github.com/danyeaw/pybites-challenges/blob/master/02/game.py)

### Day 3: Jan 15 Tuesday

**Today's Progress**: Completed PyBites Code Challenge 3 -
PyBites Blog Tag Analysis

**Thoughts:**: This is my first use of itertools product and difflib
SequenceMatcher. It took me a while to figure out I needed to read() from
the xml file instead of trying to open it line by line. It also stumped
me that the tests were putting the tag pairs in to a set, and I needed to
sort the tuples so that I didn't get duplicates. I got through the challenge
today but I am hoping over the next few weeks I can speed up my coding some.
I also started to use the REPL with `help()` more, to explore the different
python libraries while reducing my reliance on looking up things on the
internet.

**Link to work:** 
[Commit 1](https://github.com/danyeaw/pybites-challenges/commit/45d5552c82df35338289da414bc9c0fb201033c5)
[Commit 2](https://github.com/danyeaw/pybites-challenges/commit/aa7f37fdf5d3a57d629afc1ea467285ae7b94fbc)

### Day 4: Jan 16 Wednesday

**Today's Progress**:

- Completed a HankerRank challenge with basic numpy shape and reshape
- Completed PyBites Code Challenge 4 - Twitter data analysis Part 1
- Almost completed PyBites Code Challenge 5 - Similar Tweeters

**Thoughts:**: I had done the PyBites Challenge 4 before, so that one was
a refresher. Challenge 5 was really tough, and I had to use some of the
review hints to make progress. This was my first dive in to natural
language processing. I am getting an error with gensim Dictionary.doc2bow
expecting an array of unicode tokens on input, not a single string. I'm
not sure why I am getting this error, but I will troubleshoot more tomorrow.

**Link to work:** 
[Commit 1](https://github.com/danyeaw/pybites-challenges/commit/0203532d094b37a5a85a93ec42038ba9ccbd3512)
[Commit 2](https://github.com/danyeaw/pybites-challenges/commit/77125b3e93f2ac98f61240a800535b715e5e8adb)

### Day 5: Jan 17 Thursday

**Today's Progress**:

- Completed PyBites Code Challenge 5 - Similar Tweeters
- Started my first Rails app

**Thoughts**: Resolved the issues with challenge 5 I was having yesterday.
I want to start getting in to building some full stack apps to expand my
knowledge in that area.

**Link to work:** 
[Commit 1](https://github.com/danyeaw/pybites-challenges/commit/bbecc2bef9d203d5f09fe36b230ec8312ddaf2ed)

### Day 6: Jan 18 Friday

**Today's Progress**:

- Started working on upgrading Batavia to support NodeJS 10.x LTS

**Thoughts**: My goal is to get Django working again as a Toga backend.
Before doing that I need to give Batavia some Javascript attention.

### Day 7: Jan 19 Saturday

**Today's Progress**:

- Updated the Batavia dependencies to fix security vulnerabilites
- Fixed file not found errors in the Batavia test server
- Started testing Batavia against multiple versions of Python3 and Node

**Thoughts**: After running some tests, it appears that Batavia works great
with Python 3.5.6, Node 6.16.0 and 10.15.0, and django 1.11.18. This is
good because we can have users start to use a modern version of Node. 
It also breaks with Python 3.7.2 and django 2.1. This will be my next step
to figure out why django doesn't work, and then fix the Batavia bytecode
translation problems with the latest Python.

### Day 8: Jan 20 Sunday

**Today's Progress**:

More work on Batavia today:
Updates Django to version 2.1.5, including:
- Fix errors caused by pyc payloads not properly decoded
- Replace `MIDDLEWARE_CLASSES` since now deprecated
- Upgrade urlparsers from url to the new path syntax

Since the version of CodeMirror being packaged was very old, moved it to be npm installed:

- Added it to the webpack to create a codemirror.js and codemirror.css that is placed in the static site for just the 3 files out of CodeMirror needed for this project.

Update Babel configurations and package.json to fix issues caused by the upgrade to Babel 7

Enabled source map creation in webpack

**Thoughts**: Gained some good experience working with Django, Webpack,
and npm today. Did troubleshooting and added breakpoints using the
Firefox developer console. I also learned about source mapping for minified
JS. I also realized that the errors I thought I fixed yesterday, were
actually a mistake I made, I wasn't running the testserver from the correct
directory.

[Commit 1](https://github.com/pybee/batavia/pull/770/commits/27febe2458ad81d8b4af37932a43e2fcef7146fe)
[Commit 2](https://github.com/pybee/batavia/pull/770/commits/1c588819861958bc94fd70b8f102cc7862e43202)
[Commit 3](https://github.com/pybee/batavia/pull/770/commits/96ae4a135f842d2f03d317c2cac3aa4d88ee436f)

### Day 9: Jan 21 Monday

**Today's Progress**:

More work on Batavia today to add to the PR I started yesterday:
- Builds for Batavia were failing in the CI. Webpack 4 has an issue with
building for universal targets: webpack/webpack#6525. I made use of the
workaround to create a globalObject in the webpack config.
- For dependencies and building I updated it to include a production and
development modes.

I also added the new magic verison numbers for Python 3.7 and 3.8-dev, and
added all of the current op codes to the project. This is a start to get
Python 3.7 working.

**Thoughts**: Doing complex setups with webpack's configs is not easy.
This is one of my first times looking through Python's C code. Using
Python's built in py_compile, decode, and ord is much easier than trying
to look up ascii tables.

[Commit 1](https://github.com/pybee/batavia/pull/770/commits/c6a1372dbd6b3f7bc595bffb0ac7426865f46c3f)

### Day 10: Jan 22 Tuesday

**Today's Progress**: Completed 2x HackerRank challenges in Python.

- Cleaned up more Batavia opcodes to support Python 3.7.

**Thoughts**: Currently I am getting an unknown type code of 16, I'll have
to look at that more tomorrow.

### Day 11: Jan 23 Wednesday

**Today's Progress**: Completed 2x HackerRank challenges in Python.

- Add support for PEP 552 which uses 4 32-bit words in the pyc header in Python 3.7 and up
- Update the docs to have users use Python 3.5 and 3.6, and Node 10.x LTR
- Started replacing an ugly .bat script and a few Java .properties files
with one written in Python with a toml config
- Explored the basics of creating a GUI with Gooey

**Thoughts**: Feeling great about figuring out the 4 32-bit pyc header
which solved the type errors I was getting.

### Day 12: Jan 24 Thursday

**Today's Progress**: 

- Merged by PR for days 7, 8, and 9
- Started troubleshooting issue with the version number checks in Batavia
not working
- Started creating a Gitter bot using ChatterBot, Django, and Heruku for thePyBee channel

**Thoughts**: It is awesome to have one of my PRs merged! Hopefully I can
get the other one merged tomorrow.

### Day 13: Jan 25 Friday

**Today's Progress**: 

- Built a script that replaced two .bat files and two .properties
configurations with python using Click, toml, pathlib, and 
python-jproperties
- Worked on completing support for Python 3.7 and 3.8

**Thoughts**: Python makes creating simple programs sooo easy ;-)

### Day 14: Jan 26 Saturday

**Today's Progress**: 

- Completed a tutorial on Postman for web API development
- Got about half way through the Ruby on Rails tutorial to build a blog
- Worked on completing support for Python 3.7 and 3.8

**Thoughts**: I would like to learn some Rails and Vue, so I made some
progress towards that today. I have also been thinking about trying to
get some small freelance gigs on the side to start to build up a portfolio
for getting a developer job or doing freelance full time.

### Day 15: Jan 27 Sunday

**Today's Progress**: 

- Fix the Gaphor main window so that it is resizable
- Begin to replace the Gaphor Toolbox's custom wrapbox with the Gtk
ToolPalette widget that provides similar functionality

**Thoughts**: Got back in to working on Gaphor today which is great, I
really want to push through getting a working version done. The ToolPalette
drag and drop isn't currently working.

### Day 16: Jan 28 Monday

**Today's Progress**: 

- Got a working version of the script I started on Friday working. It
is now called MagicDraw AutoBot, since it is a MagicDraw Product Line
Engineering Transformer and Report Generator.

**Thoughts**: Making a CLI tool with Python has been really fun and
rewarding.

### Day 17: Jan 29 Tuesday

**Today's Progress**: 

- MagicDraw AutoBot now uses click's built in password mechanism and
the getpass module to get the username automatically. Removed storing
the password from the config files. Also switched to using a secure
temp file and added a README.
- Got drag and drop working in Gaphor with the new ToolPalette.

**Thoughts**: Really happy I got drag and drop working since it is
a little tricky with Gtk. The new ToolPalette is a big improvement. 

### Day 18: Jan 30 Wednesday

**Today's Progress**: 

- Completed an Athlete Sort challenge on Hackerrank
- Apply default position to layout the Gtk Paned on the main window
of Gaphor

**Thoughts**: On a role making updates to Gaphor, the main window is
starting to come together. My wife says it looks like Win98, so some more
work there eventually to spruce up Gtk+ in the app.

### Day 19: Jan 31 Thursday

**Today's Progress**: 

- Fixed hand drawn diagrams in Gaphor, they are now working again from
the option on the Diagrams menu.

**Thoughts**: I am still getting the hang of using Zope for creating
different components that can be called across the app. I get the value
in easily being able to call things across the app, but it does add a lot
of complexity to easily reason about how the app is working.

### Day 20: Feb 01 Friday through Day 22: Feb 03 Sunday

**Today's Progress**: 

- Learned about the Zope Component Architecture, read multiple tutorials
- Figured out how to use the getUtility method from ZCA to get the current
Gaphor diagram.

**Thoughts**: This took a lot of work to learn about Zope. Being able to
get the current Gaphor diagram is one of the last remaining items to get
a fully functional app, so this was really good.

### Day 23: Feb 04 Monday

**Today's Progress**: 

- Reviewed Arjan's Pull Requests for Gaphor.

**Thoughts**: I wasn't feeling very good when I got home from work. I
stayed home from work on Tuesday as well.

### Day 24: Feb 06 Wednesday

**Today's Progress**: 

- Completed HackerRank challenge: The Minion Game
- Added gif showing an issue with a Gaphor PR.

**Thoughts**: I am still recovering from being sick. Hopefully tomorrow
I can get back to the full swing of things.

