#### morpheus apps add

```
Usage: morpheus apps add [name] [options]
    -b, --blueprint BLUEPRINT        Blueprint Name or ID. The default value is 'existing' which means no blueprint, for creating a blank app and adding existing instances.
    -g, --group GROUP                Group Name or ID
    -c, --cloud CLOUD                Default Cloud Name or ID.
        --name VALUE                 Name
        --description VALUE          Description
    -e, --environment VALUE          Environment Name
        --validate                   Validate Only. Validates the configuration and skips creating it.
        --refresh [SECONDS]          Refresh until status is running,failed. Default interval is 30 seconds.
    -O, --option OPTION              Option in the format -O field="value"
    -P, --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
    -y, --yaml                       YAML Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Create a new app.
[name] is required. This is the name of the new app. It may also be passed as --name or inside your config.
```
