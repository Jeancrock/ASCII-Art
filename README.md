
![Logo](https://github.com/Jeancrock/ASCII-Art/blob/main/template/yellogo.png?raw=true)


## Introduction

Ascii-art is a program that takes a string as an argument and returns a graphical representation of that string using ASCII characters in the terminal. The input string can contain numbers, letters, spaces, special characters, and supports newline characters: `\n`. If a second string is provided, it will define the ASCII art font.

```
Example: 

go run . "Hello\n\nThere" | cat -e
 _    _          _   _          $
| |  | |        | | | |         $
| |__| |   ___  | | | |   ___   $
|  __  |  / _ \ | | | |  / _ \  $
| |  | | |  __/ | | | | | (_) | $
|_|  |_|  \___| |_| |_|  \___/  $
                                $
                                $
$
 _______   _                           $
|__   __| | |                          $
   | |    | |__     ___   _ __    ___  $
   | |    |  _ \   / _ \ | '__|  / _ \ $
   | |    | | | | |  __/ | |    |  __/ $
   |_|    |_| |_|  \___| |_|     \___| $
                                       $
                                       $
```

****************************************************************************************************************************

## Fonts

The program includes 4 character libraries that serve as fonts for ASCII art: 

```
        standard.txt    : standard
        shadow.txt      : shadow
        thinkertoy.txt  : thinkertoy
        varsity.txt     : varsity
```
To use these fonts, specify the font name after the string you want to convert to ASCII art.

```
Example: 
go run . "hello" shadow | cat -e
                                 $
_|                _| _|          $
_|_|_|     _|_|   _| _|   _|_|   $
_|    _| _|_|_|_| _| _| _|    _| $
_|    _| _|       _| _| _|    _| $
_|    _|   _|_|_| _| _|   _|_|   $
                                 $
                                 $

go run . "hello" thinkertoy | cat -e
                 $
o        o o     $
|        | |     $
O--o o-o | | o-o $
|  | |-' | | | | $
o  o o-o o o o-o $
                 $
                 $
```

If the font name is incorrect in the command, the program will return an error.
If no font is specified, the default font will be `standard`.

****************************************************************************************************************************
## Options

### Output

By default, the program returns the ASCII graphic representation in the terminal, but the `--output=<fileName.txt>` option allows saving the string to a file with the specified name.
If the `--output=<fileName.txt>` option is used together with another option, the program will return an error.

```
Usage: 
go run . [OPTION] [STRING] [BANNER]

Example:
go run . --output=FileName.txt "hello" shadow

```

### Reverse

The `--reverse=<fileName.txt>` option allows converting an ASCII graphic representation back to text from a file.
Only the `--color` option can be used with the `--reverse=<fileName.txt>` option.
The file to be converted must be located in the `/fonctions/options/reverse/filesToReverse/` folder.

```
Usage: 
go run . [OPTION Reverse] [OPTION Color]

Example:
go run . --reverse=fileName.txt --color=red

```

### Color

The `--color="<color>"` option changes the color of the ASCII graphic representation or the result of the `--reverse` option. The `--color` option must be the last option entered.
## Authors

- [Jeancrock](https://github.com/Jeancrock)
- [Ne0Jiku](https://github.com/Ne0Jiku)
- [humanwonder](https://github.com/humanwonder)

