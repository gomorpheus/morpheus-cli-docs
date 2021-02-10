#### morpheus tasks execute

```
Usage: morpheus tasks execute [task] --instance [instance] [options]
        --instance INSTANCE          Instance name or id to execute the task on. This option can be passed more than once.
        --instances [LIST]           Instances, comma separated list of instance names or IDs.
        --host HOST                  Host name or id to execute the task on. This option can be passed more than once.
        --hosts [LIST]               Hosts, comma separated list of host names or IDs.
    -a, --appliance                  Execute on the appliance, the target is the appliance itself.
        --config [TEXT]              Custom config
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
```
