#### morpheus virtual-images add-file

```
Usage: morpheus virtual-images add-file [name] [filepath]
        --filename FILENAME          Filename for uploaded file. Derived from [filepath] by default.
        --url URL                    Image File URL. This can be used instead of [filepath]
        --gzip                       Compress uploaded file
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -q, --quiet                      No Output, do not print to stdout
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
    -U, --username USERNAME          Username for authentication.
    -P, --password PASSWORD          Password for authentication.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Upload a virtual image file.
[name] is required. This is the name or id of a virtual image.
[filepath] or --url is required. This is location of the virtual image file.
```
