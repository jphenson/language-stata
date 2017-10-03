# Stata language support in Visual Studio Code
[![GitHub stars](https://img.shields.io/github/stars/kylebarron/language-stata.svg?style=social&label=Star)](https://github.com/kylebarron/language-stata)
[![GitHub forks](https://img.shields.io/github/forks/kylebarron/language-stata.svg?style=social&label=Fork)](https://github.com/kylebarron/language-stata)

#### Stata syntax highlighting in Visual Studio Code, built from the ground up.
Also [available for Atom](https://github.com/kylebarron/language-stata).

![stata](./img/stata-vscode.png)
Code snippet from [Gtools](https://github.com/mcaceresb/stata-gtools), a faster implementation of Stata's collapse and egen using C plugins. Shown with the [Material](https://marketplace.visualstudio.com/items?itemName=Equinusocio.vsc-material-theme) theme. 


## Features

This package highlights:
- System commands, functions, and function arguments
- Macros, both global and local
    - Accurately colors nested macros and escaped macros in strings when you want the inner macro to evaluate at runtime
- Regular expressions
    - Colors both the limited syntax provided through the `regexr()` and `regexm()` functions, as well as the vastly expanded regex syntax provided in Stata 14 and 15 through the `ustrregexm()`, `ustrregexrf()`, and `ustrregexra()` functions.

Other nice features:
- Alerts you if your variable name is illegal, i.e. if your variable name is more than 32 chars, starts with a number, or is a reserved name.
- Alerts you if you have any text other than } on a line ending a foreach/forvalues/if/else command
- Local macro back tick autocompletion. When you write a `, Visual Studio Code automatically fills in a ' after your cursor
- Makes it easy to spot incorrect nesting of compound quotes
- Support for programming ligatures for all valid Stata syntax for fonts that support them, like the [Fira Code](https://github.com/tonsky/FiraCode) font.

#### Note
Some themes may not color all parts of the syntax.

## Installation
Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.
```
ext install stata-enhanced
```

## Running Code

This package doesn't have the capabilities to run your code in Stata. If you're using Linux, you can use my [scripts](https://github.com/kylebarron/stata-autokey) with the [Autokey](https://github.com/autokey-py3/autokey) automation utility to quickly run selections of your files in a graphical session of Stata.

You might also be interested in trying to port Atom's `script` or `stata-exec` packages.