#### morpheus library-cluster-layouts add

```
Usage: morpheus library-cluster-layouts add [name] [options]
    -n, --name VALUE                 Name for this cluster layout
    -D, --description VALUE          Description
    -v, --version VALUE              Version
    -c, --creatable [on|off]         Can be used to enable / disable creatable layout. Default is on
    -g, --cluster-type CODE          Cluster type. This is the cluster type code.
    -t, --technology CODE            Technology. This is the provision type code.
    -m, --min-memory NUMBER          Min memory. Assumes MB unless optional modifier specified, ex: 1GB
    -w, --workflow ID                Workflow
    -s, --auto-scale [on|off]        Can be used to enable / disable horizontal scaling. Default is on
        --evars-json JSON            Environment variables JSON: {"name":"Foo", "value":"Bar", "masked":true, "export":true}
    -e, --evars LIST                 Environment variables list. Comma delimited list of name=value pairs
    -o, --option-types LIST          Option types, comma separated list of option type IDs
        --masters LIST               List of master. Comma separated container types IDs in format id[/count/priority], ex: 100,101/3/0
        --workers LIST               List of workers. Comma separated container types IDs in format id[/count/priority], ex: 100,101/3/1
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

Create a cluster layout.
```
