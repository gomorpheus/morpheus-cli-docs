#### morpheus budgets add

```
Usage: morpheus budgets add [name] [options]
        --name VALUE                 Name
        --description VALUE          Description (optional)
        --scope VALUE                Scope. Default: account
        --tenant VALUE               Tenant
        --user VALUE                 User
        --group VALUE                Group
        --cloud VALUE                Cloud
        --year VALUE                 Period - The period (year) the budget applies to. Default is the current year.. Default: 2020
        --interval VALUE             Interval. Default: year
        --cost [amount]              Budget cost amount, for use with default year interval.
        --q1 [amount]                Q1 cost amount, use with quarter interval.
        --q2 [amount]                Q2 cost amount, use with quarter interval.
        --q3 [amount]                Q3 cost amount, use with quarter interval.
        --q4 [amount]                Q4 cost amount, use with quarter interval.
        --january [amount]           January cost amount, use with month interval.
        --february [amount]          February cost amount, use with month interval.
        --march [amount]             March cost amount, use with month interval.
        --april [amount]             April cost amount, use with month interval.
        --may [amount]               May cost amount, use with month interval.
        --june [amount]              June cost amount, use with month interval.
        --july [amount]              July cost amount, use with month interval.
        --august [amount]            August cost amount, use with month interval.
        --september [amount]         September cost amount, use with month interval.
        --october [amount]           October cost amount, use with month interval.
        --november [amount]          November cost amount, use with month interval.
        --december [amount]          December cost amount, use with month interval.
        --enabled [on|off]           Can be used to disable a policy
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
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

Create budget.
```
