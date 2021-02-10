#### morpheus apps remove

```
Usage: morpheus apps remove [app]
        --remove-instances [on|off]  Remove instances. Default is off.
        --preserve-volumes [on|off]  Preserve Volumes. Default is off. Applies to certain types only.
        --keep-backups               Preserve copy of backups
        --releaseEIPs [on|off]       Release EIPs. Default is on. Applies to Amazon only.
    -f, --force                      Force Delete
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -q, --quiet                      No Output, do not print to stdout
    -y, --yes                        Auto Confirm
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Delete an app.
[app] is required. This is the name or id of an app.
```
