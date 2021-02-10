#### morpheus tasks add

```
Usage: morpheus tasks add [name] -t TASK_TYPE
    -t, --type TASK_TYPE             Task Type
        --name NAME                  Task Name
        --code CODE                  Task Code
        --source VALUE               Source Type. local, repository, url. Only applies to script task types.
        --content TEXT               Contents of the task script. This implies source is local.
        --file FILE                  File containing the task script. This can be used instead of --content
        --url VALUE                  URL, for use when source is url
        --content-path VALUE         Content Path, for use when source is repository or url
        --content-ref VALUE          Content Ref (Version Ref), for use when source is repository
        --result-type VALUE          Result Type
        --execute-target VALUE       Execute Target
        --target-host VALUE          Target Host
        --target-port VALUE          Target Port
        --target-username VALUE      Target Username
        --target-password VALUE      Target Password
        --git-repo VALUE             Git Repo ID
        --git-ref VALUE              Git Ref
        --retryable [on|off]         Retryable
        --retry-count COUNT          Retry Count
        --retry-delay SECONDS        Retry Delay Seconds
        --allow-custom-config [on|off]
                                     Allow Custom Config
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
```
