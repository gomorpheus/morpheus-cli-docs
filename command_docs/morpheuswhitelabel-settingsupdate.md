#### morpheus whitelabel-settings update

```
Usage: morpheus whitelabel-settings update
        --tenant TENANT              Tenant Name or ID
        --active [on|off]            Can be used to enable / disable whitelabel feature
        --appliance-name NAME        Appliance name. Only available to master tenant
        --disable-support-menu [on|off]
                                     Can be used to disable support menu
        --reset-header-logo          Resets header logo to default header logo
        --reset-footer-logo          Resets footer logo to default footer logo
        --reset-login-logo           Resets login logo to default login logo
        --reset-favicon              Resets favicon default favicon
        --header-bg-color VALUE      Header background color
        --header-fg-color VALUE      Header foreground color
        --nav-bg-color VALUE         Nav background color
        --nav-fg-color VALUE         Nav foreground color
        --nav-hover-color VALUE      Nav hover color
        --primary-button-bg-color VALUE
                                     Primary button background color
        --primary-button-fg-color VALUE
                                     Primary button foreground color
        --primary-button-hover-bg-color VALUE
                                     Primary button hover background color
        --primary-button-hover-fg-color VALUE
                                     Primary button hover foreground color
        --footer-bg-color VALUE      Footer background color
        --footer-fg-color VALUE      Footer foreground color
        --login-bg-color VALUE       Login background color
        --copyright TEXT             Copyright String
        --css TEXT                   Override CSS
        --css-file FILE              Override CSS from local file
        --terms TEXT                 Terms of use content
        --terms-file FILE            Terms of use content from local file
        --privacy-policy TEXT        Privacy policy content
        --privacy-policy-file FILE   Privacy policy content from local file
        --support-menu-links JSON    Support menu links JSON
        --support-menu-links-list LIST
                                     Support menu links list. Comma delimited list of menu links. Each menu link is pipe delimited url1|label1|code1,url2|label2|code2
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
