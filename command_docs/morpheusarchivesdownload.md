#### morpheus archives download

```
Usage: morpheus archives download [bucket:/path] [local-file]
    -f, --force                      Overwrite existing [local-file] if it exists.
        --mkdir                      Create missing directories for [local-file] if they do not exist.
    -p, --public                     Use Public Download URL instead of Private. The file must be in a public archives.
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

Download an archive file or directory.
[bucket:/path] is required. This is the name of the bucket and /path the file or folder to be downloaded.
[local-file] is required. This is the full local filepath for the downloaded file.
Directories will be downloaded as a .zip file, so you'll want to specify a [local-file] with a .zip extension.
```
