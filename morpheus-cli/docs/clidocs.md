# NAME

    morpheus - the command line interface for interacting with the Morpheus Data appliance

## SYNOPSIS

    morpheus [command] [<args>]

## DESCRIPTION

    Morpheus CLI

    This is a command line interface for managing a Morpheus Appliance.
    All communication with the remote appliance is done via the Morpheus API.

    To setup a new appliance, see the `remote add` and `remote setup` commands.

    To get started, visit https://github.com/gomorpheus/morpheus-cli/wiki/Getting-Started

    To learn more about the Morpheus Appliance, visit https://www.morpheusdata.com/features

    To learn more about the Morpheus API, visit http://bertramdev.github.io/morpheus-apidoc/

## GLOBAL OPTIONS

    Morpheus supports a few global options.

    -v, --version                    Print the version.
        --noprofile                  Do not read and execute the personal initialization script .morpheus_profile
    -C, --nocolor                    Disable ANSI coloring
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

## COMMON OPTIONS

    There are some common options that many commands support. They work the same way for each command.

    -O, --option OPTION              Option value in the format -O var="value" (deprecated soon in favor of first class options)
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it
    -r, --remote REMOTE              Remote Appliance Name to use for this command. The active appliance is used by default.
    -I, --insecure                   Allow for insecure HTTPS communication i.e. bad SSL certificate
    -y, --yes                        Auto confirm, skip any 'Are you sure?' confirmations.
    -r, --quiet                      No Output, when successful.

## MORPHEUS COMMANDS

    We divide morpheus into commands.
    Every morpheus command may have 0-N sub-commands that it supports.
    Commands generally map to the functionality provided in the Morpheus UI.

    You can get help for any morpheus command by using the -h option.

    The available commands and their options are also documented below.

## morpheus

```
Usage: morpheus [command] [options]
Commands:
        access-token
        alias
        apps
        archives
        benchmark
        blueprints
        clouds
        containers
        cypher
        datastores
        deploy
        deployments
        edit-profile
        edit-rc
        execute-schedules
              execution-request
              file-copy-request
              groups
              hosts
              image-builder
              instance-types
              instances
              key-pairs
              library-file-templates
              library-instance-types
              library-layouts
              library-node-types
              library-option-lists
              library-option-types
              library-scripts
              library-upgrades
              license
              load-balancers
              login
              logout
              monitor-apps
              monitor-checks
              monitor-contacts
              monitor-groups
              monitor-incidents
              network-domains
              network-groups
              network-pool-servers
              network-pools
              network-proxies
              network-services
              networks
              passwd
              policies
              power-schedules
              process
              recent-activity
              remote
              roles
              security-group-rules
              security-groups
              shell
              storage-buckets
              tasks
              tenants
              user-groups
              user-settings
              user-sources
              users
              version
              virtual-images
              whoami
              workflows
      Options:
          -v, --version                    Print the version.
              --noprofile                  Do not read and execute the personal initialization script .morpheus_profile
          -C, --nocolor                    Disable ANSI coloring
          -B, --benchmark                  Print benchmark time after the command is finished.
          -V, --debug                      Print extra output for debugging.
          -h, --help                       Print this help
          For more information, see https://github.com/gomorpheus/morpheus-cli/wiki
          ```


          ### morpheus access-token

          ```
          Usage: morpheus access-token [command] [options]
          Commands:
                  details
                  get
                  refresh
          ```

          #### morpheus access-token details

          ```
          Usage: morpheus access-token details
              -r, --remote REMOTE              Remote name. The current remote is used by default.
                  --remote-url URL             Remote url. The current remote url is used by default.
              -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
              -U, --username USERNAME          Username for authentication.
              -P, --password PASSWORD          Password for authentication.
              -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
              -H, --header HEADER              Additional HTTP header to include with requests.
                  --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
              -q, --quiet                      No Output, do not print to stdout
              -C, --nocolor                    Disable ANSI coloring
              -B, --benchmark                  Print benchmark time after the command is finished.
              -V, --debug                      Print extra output for debugging.
              -h, --help                       Print this help

          Print your current authentication credentials.
          This contains tokens that should be kept secret, be careful.
          ```

          #### morpheus access-token get

          ```
          Usage: morpheus access-token get
              -r, --remote REMOTE              Remote name. The current remote is used by default.
                  --remote-url URL             Remote url. The current remote url is used by default.
              -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
              -U, --username USERNAME          Username for authentication.
              -P, --password PASSWORD          Password for authentication.
              -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
              -H, --header HEADER              Additional HTTP header to include with requests.
                  --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
              -q, --quiet                      No Output, do not print to stdout
              -C, --nocolor                    Disable ANSI coloring
              -B, --benchmark                  Print benchmark time after the command is finished.
              -V, --debug                      Print extra output for debugging.
              -h, --help                       Print this help

          Print your current access token.
          This token should be kept secret. Be careful.
          ```

          #### morpheus access-token refresh

          ```
          Usage: morpheus access-token refresh
              -y, --yes                        Auto Confirm
              -r, --remote REMOTE              Remote name. The current remote is used by default.
                  --remote-url URL             Remote url. The current remote url is used by default.
              -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
              -U, --username USERNAME          Username for authentication.
              -P, --password PASSWORD          Password for authentication.
              -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
              -H, --header HEADER              Additional HTTP header to include with requests.
                  --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
              -d, --dry-run                    Dry Run, print the API request instead of executing it
              -j, --json                       JSON Output
              -q, --quiet                      No Output, do not print to stdout
              Use your refresh token.
              This will replace your current access and refresh tokens with a new values.
              Your current access token will be invalidated
              All other users or applications with access to your token will need to update to the new token.
              ```


              ### morpheus alias

              ```
              Usage: morpheus alias [command] [options]
              Commands:
                      add
                      export
                      list
                      remove
              ```

              #### morpheus alias add

              ```
              Usage: morpheus alias add [name]='[command]'
                  -e, --export                     Export this alias to your .morpheus_profile for future use
                  -h, --help                       Print this help

              Define a new alias.
              [name] is required. This is the alias name. It should be one word.
              [command] is required. This is the full command or or expression wrapped in quotes.
              Aliases can be exported for future use with the -e option.
              The `alias add` command can be invoked with `alias [name]=[command]`

              Examples:
                  alias cloud=clouds
                  alias ij='instances get -j'
                  alias new-hosts='hosts list -S id -D'
                  alias infra='clouds list -m 5; networks list -m 5; hosts list -m 5'
                  alias find-answer='(instances get 42 || instances add) || echo "oh dear..."' -e

              For more information, see https://github.com/gomorpheus/morpheus-cli/wiki/Alias
              ```

              #### morpheus alias export

              ```
              Usage: morpheus alias export [alias] [alias2] [alias3]
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help

              Export an alias, saving it to your .morpheus_profile for future use
              ```

              #### morpheus alias list

              ```
              Usage: morpheus alias list
                  -f, --format FORMAT              The format for the output: export, json, list, table (default).
                  -e, --export                     Include the '-e' switch after each alias in the output. This implies --format export.
                  -m, --max MAX                    Max Results
                  -o, --offset OFFSET              Offset Results
                  -s, --search PHRASE              Search Phrase
                  -S, --sort ORDER                 Sort Order
                  -D, --desc                       Reverse Sort Order
                  -j, --json                       JSON Output
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help

              Print list of defined aliases.
              Use the --format option to vary output.
              The `alias list` command can be abbreviated as just `alias`.
              For more information, see https://github.com/gomorpheus/morpheus-cli/wiki/Alias
              ```

              #### morpheus alias remove

              ```
              Usage: morpheus alias remove [alias1] [alias2]
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help

              This is how you remove alias definitions from your .morpheus_profile

              ### morpheus apps

              ```
              Usage: morpheus apps [command] [options]
              Commands:
                      add
                      add-instance
                      apply-security-groups
                      firewall-disable
                      firewall-enable
                      get
                      history
                      list
                      logs
                      remove
                      remove-instance
                      restart
                      security-groups
                      start
                      stop
                      update
              ```

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
                      --refresh [SECONDS]          Refresh until status is running,failed. Default interval is 5 seconds.
                  -O, --option OPTION              Option in the format -O field="value"
                  -P, --prompt                     Always prompts. Use passed options as the default value.
                  -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
                      --payload FILE               Payload from a local JSON or YAML file, skip all prompting
                      --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
                      --payload-json JSON          Payload JSON, skip all prompting
                      --payload-yaml YAML          Payload YAML, skip all prompting
                  -j, --json                       JSON Output
                      --yaml                       YAML Output
                  -d, --dry-run                    Dry Run, print the API request instead of executing it
                  -q, --quiet                      No Output, do not print to stdout
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help

              Create a new app.
              [name] is required. This is the name of the new app. It may also be passed as --name or inside your config.
              ```

              #### morpheus apps add-instance

              ```
              Usage: morpheus apps add-instance [app] [instance] [tier]
                  -O, --option OPTION              Option in the format -O field="value"
                  -P, --prompt                     Always prompts. Use passed options as the default value.
                  -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
                  -j, --json                       JSON Output
                  -d, --dry-run                    Dry Run, print the API request instead of executing it
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help

              Add an existing instance to an app.
              [app] is required. This is the name or id of an app.
              [instance] is required. This is the name or id of an instance.
              [tier] is required. This is the name of the tier.
              ```

              #### morpheus apps apply-security-groups

              ```
              Usage: morpheus apps apply-security-groups [app] [--clear] [-s]
                  -c, --clear                      Clear all security groups
                  -s, --secgroups SECGROUPS        Apply the specified comma separated security group ids
                  -j, --json                       JSON Output
                  -d, --dry-run                    Dry Run, print the API request instead of executing it
                  -C, --nocolor                    Disable ANSI coloring
                  -B, --benchmark                  Print benchmark time after the command is finished.
                  -V, --debug                      Print extra output for debugging.
                  -h, --help                       Print this help
                  ```

                  #### morpheus apps firewall-disable

                  ```
                  Usage: morpheus apps firewall-disable [app]
                      -j, --json                       JSON Output
                      -d, --dry-run                    Dry Run, print the API request instead of executing it
                      -C, --nocolor                    Disable ANSI coloring
                      -B, --benchmark                  Print benchmark time after the command is finished.
                      -V, --debug                      Print extra output for debugging.
                      -h, --help                       Print this help
                  ```

                  #### morpheus apps firewall-enable

                  ```
                  Usage: morpheus apps firewall-enable [app]
                      -j, --json                       JSON Output
                      -d, --dry-run                    Dry Run, print the API request instead of executing it
                      -C, --nocolor                    Disable ANSI coloring
                      -B, --benchmark                  Print benchmark time after the command is finished.
                      -V, --debug                      Print extra output for debugging.
                      -h, --help                       Print this help
                  ```

                  #### morpheus apps get

                  ```
                  Usage: morpheus apps get [app]
                          --refresh [SECONDS]          Refresh until status is running,failed. Default interval is 5 seconds.
                          --refresh-until STATUS       Refresh until a specified status is reached.
                      -j, --json                       JSON Output
                          --yaml                       YAML Output
                          --csv                        CSV Output
                          --csv-delim CHAR             Delimiter for CSV Output values. Default: ','
                          --csv-newline [CHAR]         Delimiter for CSV Output rows. Default: '\n'
                          --csv-quotes                 Wrap CSV values with ". Default: false
                          --csv-no-header              Exclude header for CSV Output.
                      -F, --fields x,y,z               Filter Output to a limited set of fields. Default is all fields.
                          --out FILE                   Write standard output to a file instead of the terminal.
                      -d, --dry-run                    Dry Run, print the API request instead of executing it
                      -r, --remote REMOTE              Remote name. The current remote is used by default.
                          --remote-url URL             Remote url. The current remote url is used by default.
                      -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
                      -U, --username USERNAME          Username for authentication.
                      -P, --password PASSWORD          Password for authentication.
                      -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
                      -H, --header HEADER              Additional HTTP header to include with requests.
                          --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
                      -C, --nocolor                    Disable ANSI coloring
                      -B, --benchmark                  Print benchmark time after the command is finished.
                      -V, --debug                      Print extra output for debugging.
                      -h, --help                       Print this help

                  Get details about an app.
                  [app] is required. This is the name or id of an app. Supports 1-N [app] arguments.
                  ```

                  #### morpheus apps history

                  ```
                  Usage: morpheus apps history [app]
                          --events                     Display sub processes (events).
                          --output                     Display process output.
                      -m, --max MAX                    Max Results
                      -o, --offset OFFSET              Offset Results
                      -s, --search PHRASE              Search Phrase
                      -S, --sort ORDER                 Sort Order
                      -D, --desc                       Reverse Sort Order
                      -Q, --query PARAMS               Query parameters. PARAMS format is 'phrase=foobar&category=web'
                      -j, --json                       JSON Output
                          --yaml                       YAML Output
                          --csv                        CSV Output
                          --csv-delim CHAR             Delimiter for CSV Output values. Default: ','
                          --csv-newline [CHAR]         Delimiter for CSV Output rows. Default: '\n'
                          --csv-quotes                 Wrap CSV values with ". Default: false
                          --csv-no-header              Exclude header for CSV Output.
                      -F, --fields x,y,z               Filter Output to a limited set of fields. Default is all fields.
                      -d, --dry-run                    Dry Run, print the API request instead of executing it
                      -r, --remote REMOTE              Remote name. The current remote is used by default.
                          --remote-url URL             Remote url. The current remote url is used by default.
                      -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
                      -U, --username USERNAME          Username for authentication.
                      -P, --password PASSWORD          Password for authentication.
                      -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
                      -H, --header HEADER              Additional HTTP header to include with requests.
                          --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
