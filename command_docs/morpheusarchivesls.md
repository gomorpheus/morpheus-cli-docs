#### morpheus archives ls

```
Usage: morpheus archives ls [bucket/path]
    -a, --all                        Show all files, including subdirectories under the /path.
    -l, --long                       Lists files in the long format, which contains lots of useful information, e.g. the exact size of the file, the file type, and when it was last modified.
        --human                      Humanized file sizes. The default is just the number of bytes.
    -1, --oneline                    One file per line. The default delimiter is a single space.
    -m, --max MAX                    Max Results
    -o, --offset OFFSET              Offset Results
    -s, --search PHRASE              Search Phrase
    -S, --sort ORDER                 Sort Order. DIRECTION may be included as "ORDER [asc|desc]".
    -D, --desc                       Reverse Sort Order
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
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

Print filenames for a given archive location.
Pass archive location in the format bucket/path.
```
