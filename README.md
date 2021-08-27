# Local Font Converter

This does only work for Ubuntu. Taken from this [article by Jan Küster](https://dev.to/jankapunkt/converting-my-otf-font-into-multiple-web-fonts-with-this-bash-script-m1l).

## Prerequisites
You need to have the following packages installed:

|package|command|description|
|---|---|---|
|`eot-utils`|`mkeot`|convert otf to eot|
|`eot2ttf`|`eot2ttf`|convert eot to ttf|
|`woff-tools`|`sfnt2woff`|convert otf to woff|
|`woff2`|`woff2_compress`|convert ttf to woff2|

you can install them with:
```bash
# install dependencies (packages)
sudo apt install eot-utils
sudo apt install eot2ttf
sudo apt install woff-tools
sudo apt install woff2
# check if commands exist
which mkeot
which eot2ttf
which sfnt2woff
which woff2_compress
```

# Usage
```bash
convertOtf input.otf /path/to/output/

# EXAMPLE
mkdir out
convertOtf myFont-otf out
```

# make script runnable and add to PATH
Inside the repo, run
```bash
# make runnable
sudo chmod +x ./convertOtf

# add current directory to your PATH
pwd # copy the directory and add to your PATH
```
