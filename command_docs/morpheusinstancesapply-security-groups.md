#### morpheus instances apply-security-groups

```
Usage: morpheus instances apply-security-groups [instance] [-S] [-c]
    -S, --secgroups SECGROUPS        Apply the specified comma separated security group ids
    -c, --clear                      Clear all security groups
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
```