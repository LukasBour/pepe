# pepe

![alt text](https://ichef.bbci.co.uk/ace/standard/976/cpsprodpb/16620/production/_91408619_55df76d5-2245-41c1-8031-07a4da3f313f.jpg.webp "Real fun meme lolxd")

pepe is a simple programm replacing the boring pip calls with way more interesting pepe calls. Instead of typing 
```
pip install ...
```
simply type 
```
pepe install ...
```
Cool right? Now you're still depressed because you have to use Python but at least you're having fun while doing so (i guess).

## Requirements

- CMake

## Installation

### Windows

First choose the latest release of pepe and download it (or just clone the repo). Then build the project using CMake by creating a folder "build" at the root of the repository. Then open a Terminal inside the "build" folder and execute
```
cmake ..
```
and after that
```
cmake --build .
```

Don't procrastinate yet, we're almost finished. Only thing left to do is to add the path to the executable to your PATH environment variable and you're done.

### MacOS / Linux

Should work almost similar but idk, I use Windows. Will update this part when I have time to do some research. In the meantime, you can ask ChatGPT on how to make the executable available as a shell command on your system.

## Console support

pepe prints an ASCII-Art image of pepe in the console. To make sure that the image is displayed correctly, your console window has to support UTF-8 encoding and must be configured to use it, too. In addition to that, the currently used font of your console has to support braille characters. Else the image will just be displayed as some random characters. Maybe in a future version I will change the image to enable better font / console support. 

To set the encoding of powershell to UTF-8, you have to edit your "settings.json" file. The file can be accessed by opening the Terminal-App (Win-11) and clicking on the field in the bottom left corner. The contents of the file should loke something like this
```JSON
{
    "$help": "https://aka.ms/terminal-documentation",
    "$schema": "https://aka.ms/terminal-profiles-schema",
    "profiles": 
    {
        "list": 
        [
          {
            "commandline": "Path/to/powershell",
            "guid": "ID",
            "hidden": false,
            "name": "Windows PowerShell"
          }
        ]
    },
    "schemes": [],
    "themes": []
}
```

In this file you have to replace the `"commandline"` line with the following
```JSON
 "commandline": "powershell.exe -NoExit -Command \"[Console]::OutputEncoding = [System.Text.Encoding]::UTF8\"",
```
Restart your terminal and then you should be good to go.
