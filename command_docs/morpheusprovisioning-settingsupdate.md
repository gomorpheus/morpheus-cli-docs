#### morpheus provisioning-settings update

```
Usage: morpheus provisioning-settings update
        --allow-cloud [on|off]       Allow cloud selection. Default is on
        --allow-host [on|off]        Allow host selection. Default is on
        --require-env [on|off]       Require environment selection. Default is on
        --show-pricing [on|off]      Show pricing. Default is on
        --ds-hide-stats [on|off]     Hide datastore stats on selection. Default is on
        --x-tenant-naming [on|off]   Cross-tenant naming policies. Default is on
        --reuse-name-seq [on|off]    Reuse naming sequence numbers. Default is on
        --deploy-bucket BUCKET       Deployment archive storage provider ID or name
        --cloud-username STRING      Cloud-init username
        --cloud-pwd STRING           Cloud-init password
        --cloud-keypair KEYPAIR      Cloud-init key pair ID or name
        --windows-pwd STRING         Windows administrator password
        --pxe-pwd STRING             PXE Boot default root password
        --blueprint-type TYPE        Default blueprint type ID, name or code
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
```
