# KiCAD Library Generator
![Work in progress](https://img.shields.io/badge/Status-Work%20in%20progress-important)

A KiCAD Library Generator tool to simplyfy library maintenance.

## Motivation

Have you ever wondered what would it be to have a KiCAD library based on an Excel workbook? Or to avoid any duplicated work to draw the same schematic symbols over and over? Now, the solution is here!

**Draw once, use unlimited times!**

## Features

The KiCAD Library Generator reads the given Excel workbook to read the sheets and create a library for all sheets in it.

## Installation

Download the [script](kicad-library-generator.py) and run!

### Pre-requisites

* [Python 3](https://www.python.org/)
* [xlrd](https://pypi.org/project/xlrd/)

### Configuration

In the [script](kicad-library-generator.py), you can set up three parameters:
1. `lib_name` This contains the name of the excel sheet, i.e. 'example.xlsx'
2. `symbols_name` This contains the name of the symbol library, i.e. './symbol/symbols.lib'
3. `output_folder` This contains the name of the output folder, i.e. './schematic'

## Usage

This chapter is planned to be updated in the near future.

Have a look on the [example](example.xlsx). Feel free to add more components and/or sheets.

## Features to implement

The following features planned to be implemented in the near future.

* GUI to easier setup
* Different file format support (e.g. CSV)
* GUI to preview the components

## License
[GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/)