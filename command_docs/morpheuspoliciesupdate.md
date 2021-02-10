#### morpheus policies update

```
Usage: morpheus policies update [policy] [options]
        --name VALUE                 Name for this policy
        --description VALUE          Description of policy
        --accounts LIST              Tenant accounts, comma separated list of account IDs
        --each-user [on|off]         Apply individually to each user in role, for use with policy scoped by role.
        --enabled [on|off]           Can be used to disable a policy
        --config JSON                Policy Config JSON
        --config-yaml YAML           Policy Config YAML
        --config-file FILE           Policy Config from a local JSON or YAML file
    -O, --option OPTION              Option in the format -O field="value"
        --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
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

Update a policy.
[policy] is required. This is the id of a policy.
```
