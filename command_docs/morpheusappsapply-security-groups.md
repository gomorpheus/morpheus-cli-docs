#### morpheus apps apply-security-groups

```
Usage: morpheus apps apply-security-groups [app] [--clear] [-s]
    -c, --clear                      Clear all security groups
    -s, --secgroups SECGROUPS        Apply the specified comma separated security group ids
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help
```
