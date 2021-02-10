#### morpheus projects update

```
Usage: morpheus projects update [project] [options]
        --name NAME                  Project Name
        --description NAME           Project Description
        --tags [TAGS]                Project Tags in the format 'name:value, name:value'. This replaces all project tags.
        --add-tags TAGS              Add Project Tags in the format 'name:value, name:value'. This will add/update project tags.
        --remove-tags TAGS           Remove Project Tags in the format 'name, name:value'. This removes project tags, the :value component is optional and must match if passed.
        --instances [LIST]           Instances, comma separated list of instance names or IDs.
        --add-instances LIST         Add Instances, comma separated list of instance names or IDs to add.
        --remove-instances LIST      Remove Instances, comma separated list of instance names or IDs to remove.
        --servers [LIST]             Servers, comma separated list of server (host) names or IDs.
        --add-servers LIST           Add Servers, comma separated list of server names or IDs to add.
        --remove-servers LIST        Remove Servers, comma separated list of server names or IDs to remove.
        --clouds [LIST]              Clouds, comma separated list of cloud names or IDs.
        --add-clouds LIST            Add Clouds, comma separated list of cloud names or IDs to add.
        --remove-clouds LIST         Remove Clouds, comma separated list of cloud names or IDs to remove.
        --resources [LIST]           Resources, comma separated list of resource names or IDs.
        --add-resources LIST         Add Resources, comma separated list of resource names or IDs to add.
        --remove-resources LIST      Remove Resources, comma separated list of resource names or IDs to remove.
        --find-by-name               Always treat the identifier argument as a name, never an ID. Useful for specifying names that look like numbers. eg. '1234'
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

Update a project.
[project] is required. This is the name or id of a project.
```
