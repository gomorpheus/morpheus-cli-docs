#### morpheus power-schedules add

```
Usage: morpheus power-schedules add [name]
        --name VALUE                 Name
        --description VALUE          Description
        --type [power|power off]     Type of Schedule. Default is 'power'
        --timezone CODE              The timezone. Default is UTC.
        --sundayOn [0-24]            Sunday start hour. Default is 0.
        --sundayOff [0-24]           Sunday end hour. Default is 24.
        --mondayOn [0-24]            Monday start hour. Default is 0.
        --mondayOff [0-24]           Monday end hour. Default is 24.
        --tuesdayOn [0-24]           Tuesday start hour. Default is 0.
        --tuesdayOff [0-24]          Tuesday end hour. Default is 24.
        --wednesdayOn [0-24]         Wednesday start hour. Default is 0.
        --wednesdayOff [0-24]        Wednesday end hour. Default is 24.
        --thursdayOn [0-24]          Thursday start hour. Default is 0.
        --thursdayOff [0-24]         Thursday end hour. Default is 24.
        --fridayOn [0-24]            Friday start hour. Default is 0.
        --fridayOff [0-24]           Friday end hour. Default is 24.
        --saturdayOn [0-24]          Saturday start hour. Default is 0.
        --saturdayOff [0-24]         Saturday end hour. Default is 24.
        --enabled [on|off]           Can be used to disable it
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

Create a new power schedule.
[name] is required and can be passed as --name instead.
```
