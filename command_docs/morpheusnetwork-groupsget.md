#### morpheus network-groups get

```
Usage: morpheus network-groups get [network-group]
    -j, --json                       JSON Output
    -y, --yaml                       YAML Output
        --csv                        CSV Output
        --csv-delim CHAR             Delimiter for CSV Output values. Default: ','
        --csv-newline [CHAR]         Delimiter for CSV Output rows. Default: '\n'
        --csv-quotes                 Wrap CSV values with ". Default: false
        --csv-no-header              Exclude header for CSV Output.
    -f, --fields x,y,z               Filter Output to a limited set of fields. Default is all fields for json,csv,yaml.
        --all-fields                 Show all fields present in the data.
        --wrap                       Wrap table columns instead hiding them when terminal is not wide enough.
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

Get details about a network group.
[network-group] is required. This is the name or id of a network group.
```
