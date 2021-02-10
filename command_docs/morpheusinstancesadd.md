#### morpheus instances add

```
Usage: morpheus instances add [name] -c CLOUD -t TYPE
    -g, --group GROUP                Group Name or ID
    -c, --cloud CLOUD                Cloud Name or ID
    -t, --type CODE                  Instance Type
        --name NAME                  Instance Name
        --description [TEXT]         Description
        --environment ENV            Environment code
        --tags LIST                  Metadata tags in the format 'ping=pong,flash=bang'
        --labels LIST                Labels (keywords) in the format 'foo, bar'
        --copies NUMBER              Number of copies to provision
        --layout-size NUMBER         Apply a multiply factor of containers/vms within the instance
    -l, --layout LAYOUT              Layout ID
    -p, --plan PLAN                  Service plan ID
        --resource-pool ID           Resource pool ID
        --workflow ID                Automation: Workflow ID
        --ports ARRAY                Exposed Ports, JSON formatted list of objects containing name and port
        --create-user on|off         User Config: Create Your User. Default is on
        --user-group USERGROUP       User Config: User Group
        --shutdown-days DAYS         Automation: Shutdown Days
        --expire-days DAYS           Automation: Expiration Days
        --create-backup [on|off]     Automation: Create Backups.
        --security-groups LIST       Security Groups, comma sepearated list of security group IDs
        --refresh [SECONDS]          Refresh until status is running,failed. Default interval is 30 seconds.
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

Create a new instance.
[name] is required. This is the new instance name.
The available options vary by --type.
```
