# jacques
The AWK JSON Processor

Jacques aims to address some concerns with JSON
* Lack of comment support - jacques supports comments
* Executable Code - jacques files are in no way executable

## Jacques is ever so slightly inspired by EBCDIC

Jacque uses the EBCDIC `#` character converted to ASCII `{` as a comment.

example.jacques
```
{ Start Schema Definition
¯\_(ツ)¯\_
{ This is a comment
"event": "puppetconf",
"inspired_by": ["#beerops","#Canada"],
{ End Schema Definition
_/¯(ツ)_/¯
```

# Implementation
Jacques is written in AWK.

Currently only the jacques encoder function is implemented
