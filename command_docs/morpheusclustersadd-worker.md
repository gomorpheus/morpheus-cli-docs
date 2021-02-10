#### morpheus clusters add-worker

```
Usage: morpheus clusters add-worker [cluster] [options]
        --name NAME                  Name of the new worker
        --description [TEXT]         Description
    -c, --cloud CLOUD                Cloud Name or ID
        --resource-pool ID           ID of the Resource Pool for Amazon VPC and Azure Resource Group
    -p, --plan PLAN                  Service Plan
    -n, --worker-count VALUE         Worker / host count
        --max-memory VALUE           Maximum Memory (MB)
        --cpu-count VALUE            CPU Count
        --core-count VALUE           Core Count
        --cores-per-socket VALUE     Cores Per Socket
        --volumes JSON               Volumes Config JSON
        --volumes-file FILE          Volumes Config from a local JSON or YAML file
        --config-file FILE           Instance Config from a local JSON or YAML file
        --network-interfaces JSON    Network Interfaces Config JSON
        --network-interfaces-file FILE
                                     Network Interfaces Config from a local JSON or YAML file
        --security-groups LIST       Security Groups
        --create-user on|off         User Config: Create Your User. Default is off
        --user-group USERGROUP       User Config: User Group
        --domain VALUE               Network Domain ID
        --hostname VALUE             Hostname
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
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Add worker to a cluster.
[cluster] is required. This is the name or id of an existing cluster.
[name] is required. This is the name of the new worker.
```
