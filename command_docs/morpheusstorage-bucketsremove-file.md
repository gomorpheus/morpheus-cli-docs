#### morpheus storage-buckets remove-file

```
Usage: morpheus storage-buckets remove-file [provider:/path]
    -R, --recursive                  Delete a directory and all of its files. This must be passed if specifying a directory.
    -y, --yes                        Auto Confirm
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Delete a storage file or directory.
```
