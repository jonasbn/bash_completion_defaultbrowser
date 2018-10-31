# defaultbrowser Bash Completion

Bash completion for the [`defaultbrowser`](https://github.com/kerma/defaultbrowser) tool for MacOS

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Introduction

The completion implementation requires `defaultbrowser` to be installed (of course), Tt uses the `defaultbrowser` built-in feature of listing all available browsers by not providing as$ argument.

```bash
$ defaultbrowser
  iterm2
* chrome
  firefoxdeveloperedition
  safari
  vlc
  evernote
  netnewswire
```

## Usage

```bash
$ defaultbrowser <tab><tab>
chrome                   iterm2                   vlc
evernote                 netnewswire
firefoxdeveloperedition  safari
```

## Download

```bash
$ curl https://raw.githubusercontent.com/jonasbn/bash_completion_defaultbrowser/master/defaultbrowser > defaultbrowser
```

## Installation

When downloaded you have to install the completion implementation. Where your completions are located might vary.

### Personal

If you want to install them for your personal use, do the following.

Create the file: `~/.bash_completion`, containing the code below:

```bash
for bcfile in ~/.bash_completion.d/* ; do
  . $bcfile
done
```

Ref: [ServerFault.com: _Standard place for user defined bash_completion.d scripts?_](https://serverfault.com/questions/506612/standard-place-for-user-defined-bash-completion-d-scripts)

Create a directory for your completions:

```bash
$ mkdir ~/.bash_completion.d
```

Copy your completions into the newly created directory:

```bash
$ cp defaultbrowser ~/.bash_completion.d/
```

Start a new shell and you should be good to go.

### System-wide example from Debian

Based on [an introduction](https://debian-administration.org/article/316/An_introduction_to_bash_completion_part_1) to `bash` completions on Debian.

```bash
$ sudo cp defaultbrowser /etc/bash_completion.d/
```

### System-wide example from OSX

This assumes you are using **Homebrew**

Do note that paths vary based on whether you are using `bash` 3 or 4

#### `bash` 3

Formula: `bash-completions`.

```bash
$ cp defaultbrowser /usr/local/etc/bash_completion.d/
```

And to activate right away:

```bash
$ source  /usr/local/etc/bash_completion.d/defaultbrowser
```

#### `bash` 4

Formula: `bash-completions2`.

```bash
$ cp defaultbrowser /usr/local/share/bash-completion/completions/
```

And to activate right away:

```bash
$ source /usr/local/share/bash-completion/completions/defaultbrowser
```

## Motivation

I just discovered `defaultbrowser` [today](http://jonasbn.github.io/til/osx/change_default_browser_from_cli.html), since I needed a tool, which does exactly THAT - with this tab completion, it is even easier to use.

## History

- 1.0.0
  - Initial version working with `defaultbrowser`.

## See Also

A more elaborate piece of documentation on `bash` completions is available from **The Linux Documentation Project** in the [Advanced Bash-Scripting Guide](http://tldp.org/LDP/abs/html/tabexpansion.html).

From the [GNU Documentation](https://www.gnu.org/software/bash/manual/html_node/Programmable-Completion.html).

Good two-part article, "An Introduction to Bash Completion": [Part 1](https://debian-administration.org/article/316/An_introduction_to_bash_completion_part_1) and [Part 2](https://debian-administration.org/article/317/An_introduction_to_bash_completion_part_2).

Please note that this experimental implementation has only been tested with `bash` version 3 (see version 1.0.0).

Versions after version 1.0.0 have been tested with `bash` version 4.

The most comprehensive collection of `bash` completions I have come across is [the one](https://github.com/scop/bash-completion) from the **Debian Linux distribution**. It is also the one offered for OSX via **Homebrew**.

## References

- [GitHub: kerma/defaultbrowser](https://github.com/kerma/defaultbrowser)
- [Today I Learned: Change Default Browser From the Command Line](http://jonasbn.github.io/til/osx/change_default_browser_from_cli.html)

## License

This is made available under the MIT license, see separate license file.

## Copyright

:copyright: jonasbn 2018

:copyright: [defaultbrowser](https://github.com/kerma/defaultbrowser) Margus Kerma, MIT License
