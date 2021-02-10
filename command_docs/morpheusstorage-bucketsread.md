#### morpheus storage-buckets read

```
Usage: morpheus storage-buckets read [provider:/path]
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Print the contents of a storage file.
[provider:/path] is required. This is the name or id of the provider and /path the file or folder to be downloaded.
This confirmation can be skipped with the -y option.
```
