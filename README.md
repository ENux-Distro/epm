# epm
epm is a minimal package manager written in C that uses its own minimal .epm package format.

## What is .epm package format

.epm package format is technically a tar archive that the .epm package manager extracts. The .epm package needs to have 2 important things:

### Control

Control, which needs to be executable, is the heart of the package manager. After extracting the .epm file, the package manager runs the Control file.

The control file must consits of where the package is going to be copied to, what happens after both install, warnings and etc.

### The program itself

The program itself, is going to be inside of a directory like /usr/bin, which the epm package manager will log the program's place onto /var/epm/installed/[package]

## epm options

| option  | usage           |
|-------|-------------------|
| install   | Downloads & installs the package   |
| purge  | Removes the package          |
| sync    | Pings the avaible mirros at /etc/epm/mirror.list|
| clean  | Removes logs and cache |


