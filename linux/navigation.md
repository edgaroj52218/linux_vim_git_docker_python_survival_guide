# Linux Navigation and Help

## Purpose

Find your location, move between directories, and discover how commands work.

## Prerequisites

Use a Linux Bash terminal with `pwd`, `mkdir`, and `ls` available. Choose a new directory name if `linux-navigation-practice` already exists.

## Steps and examples

```bash
mkdir linux-navigation-practice
cd linux-navigation-practice
mkdir notes
pwd
ls
cd notes
pwd
cd ..
ls -la
```

The first `pwd` ends in `/linux-navigation-practice`. The first `ls` lists `notes`. After entering `notes`, `pwd` ends in `/linux-navigation-practice/notes`. `cd ..` returns to the parent; `ls -la` also shows hidden entries such as `.` and `..`.

An absolute path starts at `/`, such as `/tmp`. A relative path starts from your current directory, such as `notes`. `~` represents your home directory.

```bash
cd ~
pwd
cd -
pwd
```

`cd ~` goes home. `cd -` returns to the previous directory and prints its path. The last `pwd` should again end in `/linux-navigation-practice`.

## Find help

```bash
ls --help
help cd
man ls
```

`--help` prints a command summary. `help cd` explains Bash's built-in `cd` command. `man ls` opens the installed manual; use the arrow keys and press `q` to leave. Some minimal systems do not install manual pages.

## Troubleshooting

| Problem | Fix |
| --- | --- |
| `mkdir`: File exists | Use a different practice directory name. |
| `cd`: No such file or directory | Run `ls` and check the name and capitalization. |
| `cd`: Not a directory | The target is a file; inspect it instead of entering it. |
| `man`: command not found | Use `ls --help` or the online manual. |

## References

- [GNU Coreutils: directory listing](https://www.gnu.org/software/coreutils/manual/html_node/Directory-listing.html)
- [Bash directory built-ins](https://www.gnu.org/software/bash/manual/html_node/Bourne-Shell-Builtins.html)

[Back to the Linux index](README.md)
