#### morpheus image-builder update

```
Usage: morpheus image-builder update [image-build] [options]
    -t, --type TYPE                  Image Build Type
        --name VALUE                 New Name
        --description VALUE          Description
    -g, --group GROUP                Group Name or ID
    -c, --cloud CLOUD                Cloud Name or ID
        --config JSON                Instance Config JSON
        --config-yaml YAML           Instance Config YAML
        --config-file FILE           Instance Config from a local JSON or YAML file
        --bootScript VALUE           Boot Script ID
        --bootCommand VALUE          Boot Command. This can be used in place of a bootScript
        --preseedScript VALUE        Preseed Script ID
        --scripts LIST               Additional Scripts (comma separated names or ids)
        --sshUsername VALUE          SSH Username
        --sshPassword VALUE          SSH Password
        --storageProvider VALUE      Storage Provider ID
        --isCloudInit [on|off]       Cloud Init?
        --buildOutputName VALUE      Build Output Name
        --conversionFormats VALUE    Conversion Formats ie. ovf, qcow2, vhd
        --keepResults VALUE          Keep only the most recent builds. Older executions will be deleted along with their associated Virtual Images. The value 0 disables this functionality.
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
```
