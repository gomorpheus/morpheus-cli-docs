### morpheus forgot

```
Usage: morpheus forgot [username]
    -U, --username USERNAME          Username of the user to be emailed.
        --email [USERNAME]           Email only. Only send an email, skip the reset password.
        --reset [TOKEN]              Reset only. Only reset password, skip sending an email.
    -T, --token TOKEN                Token, the secret token that was emailed to the user. Only reset password, skip sending an email.
        --password PASSWORD          New Password, the new password for the user.
    -O, --option OPTION              Option in the format -O field="value"
    -P, --prompt                     Always prompts. Use passed options as the default value.
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
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Send a forgot password email and reset your password.
[username] is required. This is the username to be notified.
By default this command prompts to perform two actions. 
First it sends a forgot password email to the specified user.
Then it attempts to reset the password with the secret token and a new password.
Use the --email and --token options to only perform one of these actions, instead of prompting to do both.
That is, only send the email or only reset the password.

```
