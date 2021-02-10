### morpheus update

```
Usage: morpheus update
    -f, --force                      Force Update, executes update even if latest version is already installed.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

This will update the morpheus command line interface to the latest version.
This is done by executing the system command: `gem update morpheus-cli`
```
