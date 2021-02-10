#### morpheus deployments update-version

```
Usage: morpheus deployments update-version [deployment] [version] [options]
        --userVersion VALUE          Version (optional) - This is the deployment version identifier (userVersion)
        --deployType VALUE           Deploy Type (optional) - This is the deployment version identifier (userVersion)
        --fetchUrl VALUE             Fetch URL (optional) - The URL to fetch the deployment file(s) from.
        --gitUrl VALUE               Git URL (optional) - The URL to fetch the deployment file(s) from.
        --gitRef VALUE               Git Ref (optional) - The Git Reference to use, this the branch or tag name, defaults to master.
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

Update a deployment version.
[deployment] is required. This is the name or id of a deployment.
[version] is required. This is the deployment version identifier
```
