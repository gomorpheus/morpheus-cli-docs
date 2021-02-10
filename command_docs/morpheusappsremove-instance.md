#### morpheus apps remove-instance

```
Usage: morpheus apps remove-instance [app] [instance]
    -O, --option OPTION              Option in the format -O field="value"
    -P, --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Remove an instance from an app.
[app] is required. This is the name or id of an app.
[instance] is required. This is the name or id of an instance.
```
