#### morpheus deployments remove-file

```
Usage: morpheus deployments remove-file [deployment] [version] [file] [options]
    -R, --recursive                  Delete a directory and all of its files. This must be passed if specifying a directory.
    -f, --force                      Force delete, this will do a recursive delete of directories.
    -y, --yes                        Auto Confirm
    -Q, --query PARAMS               Query parameters. PARAMS format is 'foo=bar&category=web'
    -j, --json                       JSON Output
    -q, --quiet                      No Output, do not print to stdout
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

Delete a deployment file.
[deployment] is required. This is the name or id of a deployment.
[version] is required. This is the version identifier of a deployment version.
[file] is required. This is the name of the file to be deleted.
```
