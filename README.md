# KiCAD Library Generator
A KiCAD Library Generator tool to simplify library maintenance

![Work in progress](https://img.shields.io/badge/Status-Work%20in%20progress-important)

**This script is heavily work in progress! It can be used only for experimental purposes.**

## Motivation

Have you ever wondered what would it be to have a KiCAD library based on an Excel workbook (similar to [Altium Database Libraries](https://www.altium.com/documentation/altium-designer/working-with-database-libraries-ad))? Or to avoid any duplicated work to draw the same schematic symbols over and over? Now, the solution is here!

**Draw once, use unlimited times!**

## Features

The KiCAD Library Generator reads the given Excel workbook and creates one library from each sheets.

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

The different sheets contain the different libraries. In the [example](example.xlsx) two sheets are present: 'capacitors' and 'resistors'. This means that two schematic symbol libraries will be created to the output folder, defined in the [script](kicad-library-generator.py).

The first row shall be the header. The next rows contain the different components. The script reads over the data (line-by-line), checks for the schematic symbol in the file, defined in the [script](kicad-library-generator.py) and create the component.

The parameters will be injected into the schematic symbol in the following way.
* Modify the header to UPPERCASE
* Substitute the ' ' characters with '-'
* Place '%%' to the beginning and to the end of the string

E.g. the data in the `'Parameter seconday'` column will be injected to the schematic symbol `'%%PARAMETER-SECONDARY%%'` value.

![Symbol Parameters](https://github.com/tamasfederer/kicad-library-generator/blob/main/doc/symbol-parameter.PNG?raw=true)

Have a look on the example, make some trials and feel free to add more components and/or sheets.

## Features to implement

The following features planned to be implemented in the near future.

* GUI to easier setup
* Different file format support (e.g. CSV)
* GUI to preview the components

## License
[GNU GPLv3](https://choosealicense.com/licenses/gpl-3.0/)