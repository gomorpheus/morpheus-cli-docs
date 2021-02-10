#### morpheus storage-buckets download

```
Usage: morpheus storage-buckets download [provider:/path] [local-file]
    -f, --force                      Overwrite existing [local-file] if it exists.
    -p, --mkdir                      Create missing directories for [local-file] if they do not exist.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Download a file or directory.
[provider:/path] is required. This is the name or id of the provider and /path the file or folder to be downloaded.
[local-file] is required. This is the full local filepath for the downloaded file.
Directories will be downloaded as a .zip file, so you'll want to specify a [local-file] with a .zip extension.
```
