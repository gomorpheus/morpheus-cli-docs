#### morpheus virtual-images add

```
Usage: morpheus virtual-images add [name] -t TYPE
    -t, --type TYPE                  Virtual Image Type
        --filename NAME              Image File Name. Specify a name for the uploaded file.
        --url URL                    Image File URL. This can be used instead of uploading local files.
    -c, --cloud CLOUD                Cloud to scope image to, certain types require a cloud to be selected, eg. Azure Reference
        --azure-offer OFFER          Azure Reference offer value, only applies to Azure Reference
        --azure-sku SKU              Azure SKU value, only applies to Azure Reference
        --azure-version VERSION      Azure Version value, only applies to Azure Reference
        --tenants LIST               Tenant Access, comma separated list of account IDs
        --tags LIST                  Metadata tags in the format 'name:value, name:value'
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

Create a virtual image.
```
