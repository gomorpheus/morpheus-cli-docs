#### morpheus blueprints remove-instance-config

```
Usage: morpheus blueprints remove-instance-config [blueprint] [tier] [instance] -g GROUP -c CLOUD
    -g, --group GROUP                Group
    -c, --cloud CLOUD                Cloud
    -e, --env ENV                    Environment
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

Update a blueprint, removing a specified instance config.
[blueprint] is required. This is the name or id of a blueprint.
[tier] is required. This is the name of the tier.
[instance] is required. This is the instance identifier, which may be the type, the name, or the index starting with 0.
The config scope is specified with the -g GROUP, -c CLOUD and -e ENV. The -g and -c options are required.
```
