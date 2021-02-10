#### morpheus monitor-alerts add

```
Usage: morpheus monitor-alerts add [name]
        --name STRING                Alert name
        --min-severity VALUE         Min. Severity. Trigger when severity level is reached. Default is critical
        --min-duration MINUTES       Min. Duration. Trigger after a number of minutes. Default is 0 (immediate)
        --all-checks [on|off]        Toggle trigger for all checks.
        --checks LIST                Checks, comma separated list of names or IDs.
        --all-groups [on|off]        Toggle trigger for all check groups.
        --groups LIST                Check Groups, comma separated list of names or IDs.
        --all-apps [on|off]          Toggle trigger for all check groups.
        --apps LIST                  Monitor Apps, comma separated list of names or IDs.
        --contacts LIST              Contacts, comma separated list of Contact names or IDs. Additional recipient settings can be passed like Contact ID:method:notifyOnClose:notifyOnChange.
    -O, --option OPTION              Option in the format -O field="value"
        --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
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

Create a monitoring alert rule.
[name] is required. This is the name of the new alert rule.
```
