#### morpheus resource-pools add

```
Usage: morpheus resource-pools add [cloud] [pool] [options]
    -c, --cloud CLOUD                Cloud Name or ID
        --name VALUE                 Name
        --group-access-all [on|off]  Toggle Access for all groups.
        --group-access LIST          Group Access, comma separated list of group IDs.
        --group-defaults LIST        Group Default Selection, comma separated list of group IDs
        --plan-access-all [on|off]   Toggle Access for all plans.
        --plan-access LIST           Plan Access, comma separated list of plan IDs.
        --plan-defaults LIST         Plan Default Selection, comma separated list of plan IDs
        --tenants LIST               Tenant Access, comma separated list of account IDs
        --visibility [private|public]
                                     Visibility
        --active [on|off]            Can be used to disable a resource pool
        --default-pool [on|off]      Set resource pool as the default
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

Update a resource pool.
[cloud] is required. This is the name or id of the cloud.
```
