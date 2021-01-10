# Usage

## Basic Usage

```
snekdown 0.30.5

USAGE:
    snekdown <SUBCOMMAND>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

SUBCOMMANDS:
    clear-cache    Clears the cache directory
    help           Prints this message or the help of the given subcommand(s)
    render         Parse and render the document
    watch          Watch the document and its imports and render on change
```


## Rendering

```

USAGE:
    snekdown render [OPTIONS] <input> <output>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
    -f, --format <format>    the output format [default: html]

ARGS:
    <input>     Path to the input file
    <output>    Path for the output file
```


## Watching

```
USAGE:
    snekdown watch [OPTIONS] <input> <output>

FLAGS:
    -h, --help       Prints help information
    -V, --version    Prints version information

OPTIONS:
        --debounce <debounce>    The amount of time in milliseconds to wait after changes
                                 before rendering [default: 500]
    -f, --format <format>        the output format [default: html]

ARGS:
    <input>     Path to the input file
    <output>    Path for the output file
```

