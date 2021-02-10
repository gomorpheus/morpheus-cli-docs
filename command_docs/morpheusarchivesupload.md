#### morpheus archives upload

```
Usage: morpheus archives upload [local-file] [bucket:/path]
    -R, --recursive                  Upload a directory and all of its files. This must be passed if [local-file] is a directory.
        --ignore-files PATTERN       Pattern of files to be ignored when uploading a directory.
    -y, --yes                        Auto Confirm
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

Upload a local file or folder to an archive bucket. 
The first argument [local-file] should be the path of a local file or directory.
The second argument [bucket:/path] should contain the bucket name.
The [:/path] component is optional and can be used to specify the destination of the uploaded file or folder.
The default destination is the same name as the [local-file], under the root bucket directory '/'. 
This will overwrite any existing remote files that match the destination /path.
```
