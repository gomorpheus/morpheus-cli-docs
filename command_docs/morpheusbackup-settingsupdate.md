#### morpheus backup-settings update

```
Usage: morpheus backup-settings update
    -a, --active [on|off]            Can be used to enable / disable the scheduled backups. Default is on
        --create-backups [on|off]    Can be used to enable / disable create backups. Default is on
        --backup-appliance [on|off]  Can be use to enable / disable backup appliance. Default is on
    -b, --bucket BUCKET              Default storage bucket name or ID
        --clear-bucket               Use this flag to clear default backup bucket
    -u, --update-existing            Use this flag to update existing backups with new settings
    -s, --backup-schedule ID         Backup schedule type ID
        --clear-schedule             Use this flag to clear default backup schedule
    -R, --retention NUMBER           Maximum number of successful backups to retain
    -j, --json                       JSON Output
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
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

Update your backup settings.
```
