# 3d-braille
A system for creating and exporting braille as a 3D-printable object

## Overview
Braille is a system of raised dots—in the past as seen on paper—to represent letters for the blind. Now, with the advent of the 3D printer, I've made it easy to print braille messages.

![screen shot 2018-07-03 at 5 22 55 pm](https://user-images.githubusercontent.com/15971213/42252232-83627488-7ef0-11e8-9d94-65818884e688.png)

## Instructions
This is a command line interface (CLI) which accepts some arguments such as the text to be turned into a braille message. The CLI produces a standard STL (mesh) file as an output which is suitable for opening in a slicer program such as Cura. This final process then will create a GCODE file for your printer.

## Installation

```
mkdir ~/sites && cd ~/sites
git clone https://github.com/OutsourcedGuru/3d-braille.git
cd 3d-braille
npm install
chmod a+x 3d-braille
# Create a symlink somewhere in your path so that it can be found
sudo ln -s ~/sites/3d-braille/3d-braille /usr/local/bin/3d-braille
```

## Usage
The interface is simple enough but note that the input string should come as the first argument before any flags to adjust the platform size. The width argument should come before the height.

You should invoke the executable from a folder in which you have the rights to create the file `output.stl`.

```
3d-braille -v
3d-braille --version
3d-braille "this is some text"                         # Platform of 100mm x 100mm
3d-braille "abcdefghijkl" --w=100 --h=25               # Platform of 100mm x 25mm, a single line of text 
3d-braille "abcdefghijklmnopqrstuvwx" --w=100 --h=35   # Two lines of text 
```

|Description|Version|Author|Last Update|
|:---|:---|:---|:---|
|3d-braille|v1.0.2|OutsourcedGuru|June 10, 2019|

|Donate||Cryptocurrency|
|:-----:|---|:--------:|
| ![eth-receive](https://user-images.githubusercontent.com/15971213/40564950-932d4d10-601f-11e8-90f0-459f8b32f01c.png) || ![btc-receive](https://user-images.githubusercontent.com/15971213/40564971-a2826002-601f-11e8-8d5e-eeb35ab53300.png) |
|Ethereum||Bitcoin|
