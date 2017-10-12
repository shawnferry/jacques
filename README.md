# jacques
The AWKward JSON Processor

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

# Usage
jacques attempts to naively detect the type of file based on the file extension.

```
./jacques -- -h
   Default behavior attempts to naively detect the type of file
  -e encode
  -d decode
  -h this help
```


./jacques sample/simple.json
```
¯\_(ツ)¯\_
    "id": 1,
    "name": "A green door",
    "price": 12.50,
    "tags": ["home", "green"]
_/¯(ツ)_/¯
```

# Jacques Is Flexible
Any use of the patterns `¯\_([^\x00-\x7F])¯\_` and `_/¯([^\x00-\x7F])_/¯` will be correspondingly
replaced with `{` and '}'. That is you can choose any single non-ascii character in the schema start/end tokens.

Non-exhaustive examples:
* `ϖ` as  `¯\_(ϖ)¯\_` and `_/¯(ϖ)_/¯`
* `𝛑` as  `¯\_(𝛑)¯\_` and `_/¯(𝛑)_/¯`

You can even mix and match your non-ascii characters in the same file!!!

# Reviews

Jacques is exactly as useless and half as entertaining as one might expect. -- Shawn Ferry
