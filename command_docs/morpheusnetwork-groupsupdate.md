#### morpheus network-groups update

```
Usage: morpheus network-groups update [network-group] [options]
        --name VALUE                 Name for this network group
        --description VALUE          Description of network group
        --networks LIST              Networks in the group, comma separated list of network IDs
        --subnets LIST               Subnets, comma separated list of names or IDs.
        --group-access-all [on|off]  Toggle Access for all groups.
        --group-access LIST          Group Access, comma separated list of group IDs.
        --group-defaults LIST        Group Default Selection, comma separated list of group IDs
        --tenants LIST               Tenant Access, comma separated list of account IDs
        --accounts LIST              alias for --tenants
        --visibility [private|public]
                                     Visibility
        --active [on|off]            Can be used to disable a network group
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
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Update a network group.
[network-group] is required. This is the id of a network group.
```
