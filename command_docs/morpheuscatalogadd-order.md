#### morpheus catalog add-order

```
Usage: morpheus catalog add-order [type] [options]
    -t, --type TYPE                  Catalog Item Type Name or ID
        --validate                   Validate Only. Validates the configuration and skips creating the order.
    -a, --details                    Display all details: item configuration.
        --context [instance|server]  Context Type for operational workflow types
        --target ID                  Target Resource (Instance or Server) for operational workflow types
        --sigdig DIGITS              Significant digits to display for prices (currency). Default is 4.
    -O, --option OPTION              Option in the format -O field="value"
        --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
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

Place an order for new inventory.
This allows creating a new order without using the cart.
The order must contain one or more items, each with a valid type and configuration.
By default the order is placed right away.
Use the --validate option to validate and review the order without actually placing it.
```
