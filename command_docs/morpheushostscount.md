#### morpheus hosts count

```
Usage: morpheus hosts count [options]
        --tenant TENANT              Tenant Name or ID
    -g, --group GROUP                Group Name or ID
    -c, --cloud CLOUD                Cloud Name or ID
    -M, --managed                    Show only Managed Servers
        --unmanaged                  Show only Unmanaged Servers
    -t, --type TYPE                  Show only Certain Server Types
    -p, --power STATE                Filter by Power Status
    -i, --ip IPADDRESS               Filter by IP Address
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
        --details                    Display more details: memory and storage usage used / max values.
    -s, --search PHRASE              Search Phrase
    -Q, --query PARAMS               Query parameters. PARAMS format is 'foo=bar&category=web'
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
    -U, --username USERNAME          Username for authentication.
    -P, --password PASSWORD          Password for authentication.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Get the number of hosts.
```
