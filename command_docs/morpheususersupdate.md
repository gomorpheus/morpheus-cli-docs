#### morpheus users update

```
Usage: morpheus users update [user] [options]
    -g, --global                     Global (All Tenants). Find users across all tenants. Default is your own tenant only.
        --firstName VALUE            First Name (optional)
        --lastName VALUE             Last Name (optional)
        --username VALUE             Username (optional)
        --email VALUE                Email (optional)
        --password VALUE             Password (optional)
        --passwordConfirmation VALUE Confirm Password (optional)
        --roles VALUE                Roles (optional) - Role authorities or IDs (comma separated)
        --receiveNotifications [on|off]
                                     Receive Notifications? (optional)
        --linuxUsername VALUE        Linux Username (optional)
        --linuxPassword VALUE        Linux Password (optional)
        --linuxKeyPairId VALUE       SSH Key (optional)
        --windowsUsername VALUE      Windows Username (optional)
        --windowsPassword VALUE      Windows Password (optional)
        --tenant TENANT              Tenant (Account) Name or ID
    -O, --option OPTION              Option in the format -O field="value"
    -P, --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help
```
