#### morpheus remote view

```
Usage: morpheus remote view [name]
        --path PATH                  Specify a path to load. eg '/logs'
        --no-auth PATH               Do not attempt to login with access token.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

View remote appliance in a web browser.
[name] is optional. This is the name of a remote.  Default is the current remote.
This will automatically login with the current access token.
```
