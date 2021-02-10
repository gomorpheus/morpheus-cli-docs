#### morpheus prices update

```
Usage: morpheus prices update [price]
        --name NAME                  Price name
        --type [TYPE]                Price type
        --unit [UNIT]                Price unit
        --platform [PLATFORM]        Price platform [linux|windows]. Required for platform price type
        --software [TEXT]            Price software. Required for software price type
        --volume [TYPE]              Volume type ID or name. Required for storage price type
        --datastore [DATASTORE]      Datastore ID or name. Required for datastore price type
        --cross-apply [on|off]       Apply price across clouds. Applicable for datastore price type only
        --incur [WHEN]               Incur charges [running|stopped|always]
        --currency [CURRENCY]        Price currency
        --cost [AMOUNT]              Price cost
        --fixed-markup [AMOUNT]      Add fixed price adjustment
        --percent-markup [PERCENT]   Add percent price adjustment
        --custom-price [AMOUNT]      Set customer price directly. Can be used to override price calculation based on cost and markup
        --restart-usage [on|off]     Apply price changes to usage. Default is on
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

Update price
[price] is required. Price ID, name or code
```
