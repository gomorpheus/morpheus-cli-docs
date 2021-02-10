#### morpheus instances scaling-update

```
Usage: morpheus instances scaling-update [instance]
        --autoUp [on|off]            Auto Upscale - Enable auto upscaling
        --autoDown [on|off]          Auto Downscale - Enable auto downscaling
        --zoneId ID                  Cloud (optional) - Choose a cloud to scale into.
        --minCount NUMBER            Min Count (optional) - Minimum number of nodes
        --maxCount NUMBER            Max Count (optional) - Maximum number of nodes
        --memoryEnabled [on|off]     Enable Memory Threshold - Scale when memory thresholds are met.
        --minMemory PERCENT          Min Memory (optional) - Minimum memory percent (0-100)
        --maxMemory PERCENT          Max Memory (optional) - Maximum memory percent (0-100)
        --diskEnabled [on|off]       Enable Disk Threshold - Scale when disk thresholds are met.
        --minDisk PERCENT            Min Disk (optional) - Minimum storage percent (0-100)
        --maxDisk PERCENT            Max Disk (optional) - Maximum storage percent (0-100)
        --cpuEnabled [on|off]        Enable CPU Threshold - Scale when cpu thresholds are met.
        --minCpu PERCENT             Min CPU (optional) - Minimum CPU percent (0-100)
        --maxCpu PERCENT             Max CPU (optional) - Maximum CPU percent (0-100)
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

Update scaling threshold information for an instance.
```
