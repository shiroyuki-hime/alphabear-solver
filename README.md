# Alphabear Solver

A simple python script that is intended to be used to solve game boards on the mobile game 
[Alphabear](https://play.google.com/store/apps/details?id=com.spryfox.alphabear&hl=en) by Spry Fox.

Can also be used as a [Countdown](https://en.wikipedia.org/wiki/Countdown_(game_show)#Letters_round) with an arbitrary number of letters, not just 8 like in the game show.

Uses a dictionary, generated to `map.json`, from `dictionary.txt`. It's the "official" [SOWPODS](https://en.wikipedia.org/wiki/SOWPODS) dictionary.

## Usage

To use this script, you'll need Python 3 installed.

To read letters from game screenshots you need [Pillow](https://pypi.python.org/pypi/Pillow/2.2.1) and [pytesseract](https://pypi.python.org/pypi/pytesseract/0.1) installed.

1. Make sure you have a tone of words in `dictionary.txt`, one word per line. A wordlist is included here but you can modify it if you want.
2. Run `hashdict.py`
3. Run `solver.py`

Everytime you change/update the dictionary, you'll need to rerun `hashdict.py`

## Todo

* Read letters from game input.
* Weight letters so that ones with less moves remaining, worth more points etc. are preferred by the matching algorithm.
* Grab better dictionary, preferably the one used in the actual game.

## Dependencies

* Python 3

For reading images

* PyOCR
* Install an OCR:
  * tesseract-ocr from http://code.google.com/p/tesseract-ocr/
    ('tesseract-ocr' + 'tesseract-ocr-&lt;lang&gt;' in Debian).
    You must be able to invoke the tesseract command as "tesseract".
    Python-tesseract is tested with Tesseract >= 3.01 only.
  * or cuneiform
* Pillow

### References

* Dictionary (`dictionary.txt`) is taken from here: https://code.google.com/p/scrabblehelper/source/browse/trunk/ScrabbleHelper/src/dictionaries/sowpods.txt?r=20
* [The World's Fastest Scrabble Program](http://www.cs.cmu.edu/afs/cs/academic/class/15451-s06/www/lectures/scrabble.pdf) - 
Andrew W. Appel & Guy J. Jacobson (1988)
