### morpheus login

```
Usage: morpheus login [username] [password]
    -u, --username USERNAME          Username. Sub-tenant users must format their username with a prefix like {subdomain}\{username}
    -p, --password PASSWORD          Password
    -t, --test                       Test credentials only, does not update stored credentials for the appliance.
        --client-id CLIENT           Used to test authentication with a client_id other than morph-cli. Currently behaves like --test, credentials are not stored.
    -T, --token ACCESS_TOKEN         Use an existing access token to login instead of authenticating with a username and password.
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Login to a remote appliance with a username and password or using an access token.
Logging in with username and password will make an authentication api request to obtain an access token.
[username] is required, this is the username of the Morpheus User
[password] is required, this is the password of the Morpheus User
Sub-tenant users will need to pass their tenant subdomain prefix. ie. {subdomain}\{username}
By default, the subdomain is the tenant account ID. Example: 2\neo
The --token option can be used to login with a valid access token instead of username and password.
The specified token will be verified by making a whoami api request
If successful, the access token will be saved with the active session for the remote appliance.
This command will first logout any active session before attempting authentication.
The --test option can be used to test credentials without updating the stored credentials for the appliance, neither logging you in or out.
```
