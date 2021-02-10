#### morpheus workflows update

```
Usage: morpheus workflows update [name] --tasks taskId:phase,taskId2:phase,taskId3:phase
        --name NAME                  New name for workflow
        --description DESCRIPTION    Description of workflow
        --tasks [x,y,z]              List of tasks to run in order, in the format <Task ID>:<Task Phase> Task Phase is optional. Default is the same workflow type: 'provision' or 'operation'.
        --option-types [x,y,z]       List of option type name or IDs. For use with operational workflows to add configuration during execution.
        --platform [PLATFORM]        Platform, eg. linux, windows or osx
        --allow-custom-config [on|off]
                                     Allow Custom Config
        --visibility VISIBILITY      Visibility, eg. private or public
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
```
