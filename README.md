Simple but effective OCR implementation using pyTesseract
To install:
  pip install pytesseract
  change the location of tesseract.exe accordingly
  import WorkingOCR
Useful functions:
find_all(target) - finds all word matches and returns the array of boxes
find_word(target) - returns first word match
box_under_word(target, offset, x_offset=0) - returns the position given an offset of a box near a word
tripple_try(target) - Attempts 3 times to find a match for the word (useful when waiting for a loading screen)

Note all functions account for partial matches untill the last 3 characters. 
Example:
find_word("dogma") will first look for "dogma", then "dogm", then "dog" (in case the first attempts are not found)
