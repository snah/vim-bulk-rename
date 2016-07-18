# Bulk file renaming in Vim

Bulk renaming files can be annoying and time consuming.
This simple tool allows you to use vim's powerful editing commands to make this task easier.

## Requirements

Any POSIX operating system with vim and bash should work.

## Installation

Simply put the file `vr` somewhere in your path and make sure it is executable.

## Usage

Usage: vr [FOLDER]

Open a list of filenames from FOLDER in vim for mass renaming.
When FOLDER is not given the current directory is used.

Upon exiting vim the files will be renamed as needed.
Files can also be removed by replacing the filename with and empty line.
Exit vim without saving or save an empty file to cancel.

WARNING: DO NOT reorder the filenames or remove lines, as the algorithm depends
on the line number to identify the original file. To aid the user the 'dd'
command is remapped to clear the current line, which results in the file being
deleted.

## Collaboration

While fully operational this is just a very basic version of what is possible
using this concept. Feel free to create a pull request or request a feature.
