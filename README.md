
# git-export

Exports file differences in working tree.

## Usage

```bash
$ git export master
# Exports ./YYYYMMDDHHMMSS/*
$ git export -o ./my_exports develop master
# Exports ./my_exports/YYYYMMDDHHMMSS/*
$ git export -p my_prefix HEAD~2 HEAD~3
# Exports ./my_prefix/*
```

## Installation

Clone this repogitory on your local machine.

```bash
$ git clone https://github.com/toru-hamaguchi/git-export.git
$ cd git-export
```

`git-export` must be executable.

```bash
$ chmod +x git-export
```

And put `git-export` in your `$PATH`.

```bash
$ sudo ln -s "$(pwd)/git-export" /usr/local/bin/git-export
```

### On Windows

Copy `git-export` to `%YOUR_GIT_INSTALL_ROOT%/libexec/git-core/`.

## Change Log

### 2014/04/17 v1.1
* Change implementation from `git-diff + file copy` to `git-diff + git-archive + tar`.
* Add `-p` option.
* Add `-v` option.

### 2012/06/11 v1.0
* First release.
