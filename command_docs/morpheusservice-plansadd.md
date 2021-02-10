#### morpheus service-plans add

```
Usage: morpheus service-plans add
        --name NAME                  Service plan name
        --code CODE                  Service plan code, unique identifier
    -t, --provision-type [TYPE]      Provision type ID or code
        --description [TEXT]         Description
        --active [on|off]            Can be used to enable / disable the plan. Default is on
        --editable [on|off]          Can be used to enable / disable the editability of the service plan. Default is on
        --storage [AMOUNT]           Storage size is required. Assumes GB unless optional modifier specified, ex: 512MB
        --memory [AMOUNT]            Memory size is required. Assumes MB unless optional modifier specified, ex: 1GB
        --cores [NUMBER]             Core count. Default is 1
        --disks [NUMBER]             Max disks allowed
        --custom-cores [on|off]      Can be used to enable / disable customizable cores. Default is on
        --custom-storage [on|off]    Can be used to enable / disable customizable storage. Default is on
        --custom-volumes [on|off]    Can be used to enable / disable customizable extra volumes. Default is on
        --custom-memory [on|off]     Can be used to enable / disable customizable memory. Default is on
        --add-volumes [on|off]       Can be used to enable / disable ability to add volumes. Default is on
        --sort-order NUMBER          Sort order
        --price-sets [LIST]          Price set(s), comma separated list of price set IDs
        --min-storage NUMBER         Min storage. Assumes GB unless optional modifier specified, ex: 512MB
        --max-storage NUMBER         Max storage. Assumes GB unless optional modifier specified, ex: 512MB
        --min-memory NUMBER          Min memory. Assumes MB unless optional modifier specified, ex: 1GB
        --max-memory NUMBER          Max memory. Assumes MB unless optional modifier specified, ex: 1GB
        --min-cores NUMBER           Min cores
        --max-cores NUMBER           Max cores
        --group-access-all [on|off]  Toggle Access for all groups.
        --group-access LIST          Group Access, comma separated list of group IDs.
        --visibility VISIBILITY      Visibility [private|public]
        --tenants LIST               Tenant Access, comma separated list of account IDs
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

Create service plan
```
