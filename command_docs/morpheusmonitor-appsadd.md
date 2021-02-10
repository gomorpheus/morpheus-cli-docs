#### morpheus monitor-apps add

```
Usage: morpheus monitor-apps add [name]
        --name VALUE                 Name
        --description VALUE          Description
        --minHappy VALUE             Min Checks. This specifies the minimum number of checks within the app that must be happy to keep the app from becoming unhealthy.
        --severity VALUE             Max Severity. Determines the maximum severity level this app can incur on an incident when failing. Default is critical
        --inUptime [on|off]          Affects Availability. Default is on.
        --muted [on|off]             Muted, Turns Affects Availability off.
        --checks LIST                Checks to include in this app, comma separated list of names or IDs.
        --groups LIST                Check Groups to include in this app, comma separated list of names or IDs.
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
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
    -U, --username USERNAME          Username for authentication.
    -P, --password PASSWORD          Password for authentication.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Create a new app of monitoring checks.
[name] is required and can be passed as --name instead.
```
