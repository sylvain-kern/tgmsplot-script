readme.md

# tgms-plot-script

`tgmsplot-script` is a script for Origin software to automate data treatment and plot for mass spectrometry and thermogravimetry experiences using the Netzsch equipment.

Origin's website: https://www.originlab.com

This file describes how to install and use it. For more details on in-depth use, see the documentation in the following folder:

```
procedure/procedure.pdf
```

## Installation

Run `setup.exe` in the setup folder. When it asks for the installation folder, please check that your Origin files folder is the same (it may change with your version of Origin or the way it is installed on your computer). In most of the cases the default folder should work though.

To install manually, just put the `tgmsplot-script` folder in the Origin files folder:
```
C:\Program Files\OriginLab\Origin2016
```

Again, the very folder may change depending on your version of Origin, so be careful.

## Usage

The scripts will process the exported files from Netzsch Aëolos and Proteus Dispsav software in `.asc` or `.txt` format. Make sure you have exported all files for the MS, TG and BL before starting the program. See the documentation for more details.

Open Origin and run the files via the Command window: on the right of the top toolbar or by pressing `Alt+"`. Then run the desired files with:
```
run.file(<the file path>)
```

What do the files do ?

`import-ms` : imports MS data in a worksheet and smooths the columns.

`import-tg` : imports TG data in a worksheet, imports baseline, does the substraction, smooths the mass loss and puts it in the MS worksheet. It also fits the temperature growth on a linear model and puts temperature points in the MS worksheet.

`plot-vs-temp` : asks the user what to plot and plots it versus the temperature. All curves are on a new layer of the same graph.

`plot-vs-time` : asks the user what to plot and plots it versus the time. All curves are on a new layer of the same graph.


### Button groups

You can put custom button groups in the Origin toolbar to execute the scripts without opening the Command window. More information about that here:

https://www.originlab.com/doc/Origin-Help/UserDef-Custom-Toobar-Button

## Issues

Segment management is not on point.

The graphs still need a bit of manual formatting.