# Haste-Client

This is a rewritten Haste-Client in Go which is meant to be a little utility that uploads code via command line from pipe or by providing names of files to upload.

# Usage

Examples:

`echo Sample Text | haste`  

`haste veryLongScript.js | xsel`

`echo "Hello World" | haste message.txt - main.cpp`
> *uploads (separetly): contents of message.txt file, standard input from echo command, contents of main.cpp file
 This can be combined with `pbcopy`, like:

* mac osx: `cat file | haste | pbcopy`
* linux: `cat file | haste | xsel`

<br>

## Arguments

`-h`

Shows Help and exits

`-v`

Shows Program version and exits

`-d string`

Changes upload destination, can be a URL another haste server (default: https://cetus.sh/paste).  

`-r`

Returns a link to raw paste (text only) instead

# Installing Linux


```bash
git clone https://github.com/ydap1/haste-client/ 
cd haste-client
make
sudo cp haste /usr/local/bin/
```

Or just clone GitHub repository and build with `make`.
