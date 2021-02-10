#### morpheus library-instance-types update

```
Usage: morpheus library-instance-types update [name] [options]
        --name VALUE                 Name
        --code VALUE                 Code - Useful shortcode for provisioning naming schemes and export reference.
        --description VALUE          Description (optional)
        --category VALUE             Category
        --visibility VALUE           Visibility (optional). Default: private
        --environmentPrefix VALUE    Environment Prefix (optional) - Used for exportable environment variables when tying instance types together in app contexts. If not specified a name will be generated.
        --hasSettings [on|off]       Enable Settings (optional)
        --hasAutoScale [on|off]      Enable Scaling (Horizontal) (optional)
        --hasDeployment [on|off]     Supports Deployments (optional) - Requires a data volume be configured on each version. Files will be copied into this location.
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
        --option-types [x,y,z]       List of Option Type IDs

Update an instance type.
[name] is required. This is the name or id of a instance type.
```
