donow
=====

donow is a tool that gives you convinient access to functions in a shell script.

The idea is to provide `Dofiles` and the `donow` command to automate recurring tasks that do not fit the usecase of a build system.

## Installation

from source:

```
git clone git@github.com:turbinenreiter/donow.git
cd donow
install donow.py ~/bin/donow
```

or with pip:

```
pip install donow --user
```

## Usage

Put a `Dofile` in you working directory. `Dofiles` are shell scripts which follow the naming convention `do-<name>` and are structured like this:

```sh
#!/usr/bin/env bash

test() {
    echo test
}

"$@"
```

Running `donow` in the same direcotry will find the `Dofile` and make it's functions avaliable as commands.

`donow test` will return test.

Additionally there are the `help` and `list` commands built in:
* help: print help message
* list: list all do's of the Dofile
