#### morpheus hosts list

```
Usage: morpheus hosts list
    -g, --group GROUP                Group Name or ID
    -c, --cloud CLOUD                Cloud Name or ID
    -M, --managed                    Show only Managed Servers
        --unmanaged                  Show only Unmanaged Servers
    -t, --type TYPE                  Show only Certain Server Types
    -p, --power STATE                Filter by Power Status
    -i, --ip IPADDRESS               Filter by IP Address
        --cluster CLUSTER            Filter by Cluster Name or ID
        --plan NAME                  Filter by Plan name(s)
        --plan-id ID                 Filter by Plan id(s)
        --plan-code CODE             Filter by Plan code(s)
        --vm
                                     Show only virtual machines
        --hypervisor
                                     Show only VM Hypervisors
        --container
                                     Show only Container Hypervisors
        --baremetal
                                     Show only Baremetal Servers
        --status STATUS
                                     Filter by Status
        --agent
                                     Show only Servers with the agent installed
        --noagent
                                     Show only Servers with No agent
        --created-by USER            Created By User Username or ID
        --tenant TENANT              Tenant Name or ID
        --tags Name=Value            Filter by tags.
        --tag-compliant              Displays only servers that are valid according to applied tag policies. Does not show servers that do not have tag policies.
        --non-tag-compliant          Displays only servers with tag compliance warnings.
        --stats                      Display values for memory and storage usage used / max values.
    -a, --details                    Display all details: hostname, private ip, plan, stats, etc.
    -m, --max MAX                    Max Results
    -o, --offset OFFSET              Offset Results
    -s, --search PHRASE              Search Phrase
    -S, --sort ORDER                 Sort Order. DIRECTION may be included as "ORDER [asc|desc]".
    -D, --desc                       Reverse Sort Order
    -Q, --query PARAMS               Query parameters. PARAMS format is 'foo=bar&category=web'
    -j, --json                       JSON Output
    -y, --yaml                       YAML Output
        --csv                        CSV Output
        --csv-delim CHAR             Delimiter for CSV Output values. Default: ','
        --csv-newline [CHAR]         Delimiter for CSV Output rows. Default: '\n'
        --csv-quotes                 Wrap CSV values with ". Default: false
        --csv-no-header              Exclude header for CSV Output.
    -f, --fields x,y,z               Filter Output to a limited set of fields. Default is all fields for json,csv,yaml.
        --all-fields                 Show all fields present in the data.
        --wrap                       Wrap table columns instead hiding them when terminal is not wide enough.
    -q, --quiet                      No Output, do not print to stdout
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

List hosts.
```
