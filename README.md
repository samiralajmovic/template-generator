# Template Generator

[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)

A simple bash script used to manage boilerplates.

![example usage of template-generator](media/output.gif)

## Prerequisite

- Bash 4.2 >

## Install

1. Put the file [tp](tp) in an executable path.
2. Create a directory named boilerplates in your home folder and fill it with boilerplates.

Furthermore, if you want bash-autocompletion:

3. [Install boilerplates-completion](https://github.com/scop/bash-completion).
4. Source [tp-completion.sh](tp-completion.sh) from `~/.bash_completion`.

## Usage

```
template-generator - Template generator CLI

Usage: tp [command] [arguments]

Options:
  -h, --help                       Print this help
  -v, --version                    Print script version
  -L, --level                      Max display depth of the directory tree
  -b, --boilerplate-path <path>    Specify boilerplate path
  -f, --format <tree|line>         List format [default: tree]

Commands:
  list|ls|l [subdirectory]         List boilerplates.
  generate|g [boilerplate] [dest]  Generate boilerplate.
  preview|p [boilerplate]          Preview boilerplate.
  edit|e [boilerplate]             Edit boilerplate in editor.
  remove|rm|r [boilerplate]        Remove a boilerplate.
  new|n [file] [dest]              Add a new boilerplate.

Examples:
  # Show first depth level of boilerplates path.
  $ tp ls -L 1

  # Copy boilerplate file.txt to current directory with filename new-file.txt
  $ tp generate files/file.txt new-file.txt

Boilerplate Path:

  The order of precedence (highest to lowest) is:
    1. Path specified in options
    2. Environment variable BOILERPLATES_PATH
    3. $PWD/.boilerplates/
    4. $PWD/boilerplates/
    5. ~/.boilerplates/
    6. ~/boilerplates/

```
