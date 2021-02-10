#### morpheus library-layouts update

```
Usage: morpheus library-layouts update [layout] [options]
        --name VALUE                 Name for this layout
        --version VALUE              Version
        --description VALUE          Description
        --creatable [on|off]         Creatable
        --technology CODE            Technology
        --min-memory VALUE           Minimum Memory (MB)
        --auto-scale [on|off]        Enable Scaling (Horizontal)
        --convert-to-managed [on|off]
                                     Supports Convert To Managed
        --workflow ID                Workflow
        --option-types [x,y,z]       List of Option Type IDs
        --node-types [x,y,z]         List of Node Type IDs
        --spec-templates [x,y,z]     List of Spec Templates to include in this layout, comma separated list of names or IDs.
        --group-access-all [on|off]  Toggle Access for all groups.
        --group-access LIST          Group Access, comma separated list of group IDs.
    -O, --option OPTION              Option in the format -O field="value"
        --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
    -q, --quiet                      No Output, do not print to stdout
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

Update a layout.
[layout] is required. This is the name or id of a layout.
```