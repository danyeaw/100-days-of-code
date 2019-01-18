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
