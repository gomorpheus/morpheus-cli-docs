#### morpheus self-service add

```
Usage: morpheus self-service add [name] [options]
    -t, --type VALUE                 Type. Default: instance
        --name VALUE                 Name
        --description VALUE          Description (optional)
        --enabled [on|off]           Enabled (optional). Default: true
        --featured [on|off]          Featured (optional)
        --visibility VALUE           Visibility. Default: private
        --iconPath VALUE             Logo (optional)
        --config VALUE               Config - JSON or YAML
        --blueprint VALUE            Blueprint - Choose a blueprint to apply to the catalog item.
        --appSpec VALUE              App Spec - Enter a spec in the for the App, the Scribe YAML format
        --workflow VALUE             Workflow (optional) - Enter a spec in the for the App, the Scribe YAML format
        --context VALUE              Context Type (optional) - Context for operational workflow, determines target type. Default: Select
        --content VALUE              Content (optional) - Wiki Page Content describing the catalog item
        --config-file FILE           Config from a local JSON or YAML file
        --option-types [x,y,z]       List of Option Type IDs
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

Create a new catalog item type.
```
