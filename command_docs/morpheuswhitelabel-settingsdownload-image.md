#### morpheus whitelabel-settings download-image

```
Usage: morpheus whitelabel-settings download-image [image-type] [local-file]
        --tenant TENANT              Tenant Name or ID
    -f, --force                      Overwrite existing [local-file] if it exists.
    -p, --mkdir                      Create missing directories for [local-file] if they do not exist.
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

Download an image file.
[image-type] is required. This is the whitelabel image type (header-logo|footer-logo|login-logo|favicon) to be downloaded.
[local-file] is required. This is the full local filepath for the downloaded file.
```
