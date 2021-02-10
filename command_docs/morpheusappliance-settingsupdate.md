#### morpheus appliance-settings update

```
Usage: morpheus appliance-settings update
        --appliance-url STRING       Appliance URL
        --internal-appliance-url STRING
                                     Internal appliance URL (PXE)
        --api-allowed-origins STRING API allowed origins
        --registration-enabled [on|off]
                                     Tenant registration enabled
        --default-tenant-role ROLE   Default tenant role authority or ID
        --default-user-role ROLE     Default user role authority or ID
        --docker-privileged-mode [on|off]
                                     Docker privileged mode
        --expire-pwd-days NUMBER     Expire password after specified days. Set to 0 to disable this feature
        --disable-after-attempts NUMBER
                                     Disable user after attempts. Set to 0 to disable this feature
        --disable-after-days-inactive NUMBER
                                     Disable user if inactive for specified days. Set to 0 to disable this feature
        --warn-user-days-before NUMBER
                                     Send warning email before deactivating. Set to 0 to disable this feature
        --smtp-from-email STRING     From email address
        --smtp-server STRING         SMTP server / host
        --smtp-port NUMBER           SMTP port
        --smtp-ssl [on|off]          Use SSL for SMTP connections
        --smtp-tls [on|off]          Use TLS for SMTP connections
        --smtp-user STRING           SMTP user
        --smtp-password STRING       SMTP password
        --proxy-host STRING          Proxy host
        --proxy-port NUMBER          Proxy port
        --proxy-user STRING          Proxy user
        --proxy-password STRING      Proxy password
        --proxy-domain STRING        Proxy domain
        --proxy-workstation STRING   Proxy workstation
        --currency-provider STRING   Currency provider
        --currency-key STRING        Currency provider API key
        --enable-all-clouds          Set all cloud types enabled status on, can be used in conjunction with --disable-clouds
        --enable-clouds LIST         List of cloud types to set enabled status on, each item can be either name or ID
        --disable-clouds LIST        List of cloud types to set enabled status off, each item can be either name or ID
        --disable-all-clouds         Set all cloud types enabled status off, can be used in conjunction with --enable-clouds options
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
