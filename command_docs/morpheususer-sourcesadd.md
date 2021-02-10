#### morpheus user-sources add

```
Usage: morpheus user-sources add [account] [name]
        --tenant TENANT              Tenant Name or ID the user source will belong to, default is your own.
        --type CODE                  User Source Type
        --name VALUE                 Name for this user source
        --description VALUE          Description
        --allow-custom-mappings [on|off]
                                     Allow Custom Mappings, Enable Role Mapping Permissions
                                     Allow Custom Mappings, Enable Role Mapping Permissions
        --role-mappings MAPPINGS     Role Mappings FQN in the format id1:FQN1,id2:FQN2
        --role-mapping-names MAPPINGS
                                     Role Mapping Names in the format id1:Name1,id2:Name2
        --default-role ID            Default Role ID
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

Create a new user source.
[account] is required. This is the name or id of an account.
```
