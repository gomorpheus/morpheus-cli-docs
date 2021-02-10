#### morpheus roles update-persona-access

```
Usage: morpheus roles update-persona-access [role] [persona] [access]
        --persona CODE               Persona Code
        --all                        Update all personas at once.
        --access VALUE               Access value [full|none]
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

Update role access for a persona or all personas.
[role] is required. This is the name or id of a role.
--persona or --all is required. This is the code of a persona. Service Catalog or Standard
--access is required. This is the new access value. full and none
```
