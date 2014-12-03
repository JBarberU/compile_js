# battery-term

compile_js is a commandline utility for traversing and merging javascript files 
used with UIAutomation for iOS. It's useful if you mainly use instruments 
through the commandline and use a lot of libraries, but also want an easy way to 
use the Instruments.app for debugging/recording. The main reason this utility 
exists is the clunky way Instruments.app handles file includes...

compile_js traverses the selected files and resolves the non-standard #imports 
to recurse through all the dependencies.

## Usage

```bash
-i The input files to compile (directory or javascript file)
-o The name of the output file (the given file will be overwritten)
-h This help page
```


## Examples

```bash
$ compile -i js/helpers -o instr.js
$ compile -i js/helpers -i /js/lang-ext -o instr.js
$ compile -i js/helpers -i /js/lang-ext/string.js -o instr.js
```

## License

See [LICENSE](LICENSE.md)

