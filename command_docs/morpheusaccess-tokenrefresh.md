#### morpheus access-token refresh

```
Usage: morpheus access-token refresh
    -T, --token TOKEN                Refresh Token to use. The saved credentials are used by default.
    -y, --yes                        Auto Confirm
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -j, --json                       JSON Output
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Use the refresh token in your saved credentials, or a provided token.
This will replace your current access and refresh tokens with a new values.
Your current access token will be invalidated
All other users or applications with access to your token will need to update to the new token.
```
