#### morpheus invoices list-line-items

```
Usage: morpheus invoices list-line-items
    -a, --all                        Display all details, costs and prices.
        --prices                     Display prices: Total, Compute, Storage, Network, Extra
        --invoice-id ID              Filter by Invoice ID
        --external-id ID             Filter by External ID
    -t, --type TYPE                  Filter by Ref Type eg. ComputeSite (Group), ComputeZone (Cloud), ComputeServer (Host), Instance, Container, User
        --id ID                      Filter by Ref ID
        --group ID                   Filter by Group
    -c, --cloud CLOUD                Filter by Cloud
        --instance ID                Filter by Instance
        --container ID               Filter by Container
        --server ID                  Filter by Server (Host)
        --user ID                    Filter by User
        --project PROJECT            View invoices for a project.
        --start DATE                 Start date in the format YYYY-MM-DD.
        --end DATE                   End date in the format YYYY-MM-DD. Default is now.
        --period PERIOD              Period in the format YYYYMM. This can be used instead of start/end.
        --active [true|false]        Filter by active.
        --estimate [true|false]      Filter by estimate.
        --tenant ID                  View invoice line items for a tenant. Default is your own account.
        --tags Name=Value            Filter by tags.
        --raw-data                   Display Raw Data, the cost data from the cloud provider's API.
        --totals                     View total costs and prices for all the invoices found.
        --totals-only                View totals only
        --sigdig DIGITS              Significant digits when rounding cost values for display as currency. Default is 2. eg. $3.50
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

List invoice line items.
```
