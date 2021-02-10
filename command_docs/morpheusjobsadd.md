#### morpheus jobs add

```
Usage: morpheus jobs add [name]
        --name NAME                  Updates job name
    -a, --active [on|off]            Can be used to enable / disable the job. Default is on
    -t, --task [TASK]                Task ID or code, assigns task to job. Incompatible with --workflow option.
    -w, --workflow [WORKFLOW]        Workflow ID or code, assigns workflow to job. Incompatible with --task option.
        --context-type [TYPE]        Context type (instance|server|none). Default is none
        --instances [LIST]           Context instances(s), comma separated list of instance IDs. Incompatible with --servers
        --servers [LIST]             Context server(s), comma separated list of server IDs. Incompatible with --instances
    -S, --schedule [SCHEDULE]        Job execution schedule type name or ID
        --config [TEXT]              Custom config
    -R, --run [on|off]               Can be used to run the job now.
        --date-time DATETIME         Can be used to run schedule at a specific date and time. Use UTC time in the format 2020-02-15T05:00:00Z. This sets scheduleMode to 'dateTime'.
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

Create job.
```
