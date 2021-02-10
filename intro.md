Morpheus CLI v5.2.1

## Getting Started

The Morpheus CLI is a command line interface for the Morpheus appliance. It's a ruby gem that provides the `morpheus` executable. It works by making HTTP requests to the Morpheus API.

The Morpheus CLI is written in Ruby and requires ruby 2.5 or newer to be installed. Most UNIX-based systems will have this installed already.

Install the CLI using rubygems:

    gem install morpheus-cli

**Installing on Windows:** [https://github.com/gomorpheus/morpheus-cli/wiki/installing-on-windows](https://github.com/gomorpheus/morpheus-cli/wiki/installing-on-windows)<br/>
**Installing Ruby and Ruby Gems:** [https://rvm.io/](https://rvm.io/)

Update to the latest version:

    gem update morpheus-cli

To get started, see the command `remote add` command.

## Guides

**Getting Started:** [https://github.com/gomorpheus/morpheus-cli/wiki/Getting-Started](https://github.com/gomorpheus/morpheus-cli/wiki/Getting-Started)<br/>
**Managing Instances:** [https://github.com/gomorpheus/morpheus-cli/wiki/Managing-Instances](https://github.com/gomorpheus/morpheus-cli/wiki/Managing-Instances)

## Helpful Resources

To learn more about Morpheus Data, visit [https://www.morpheusdata.com](https://www.morpheusdata.com)<br/>
For additional tips on using Morpheus CLI, visit [https://github.com/gomorpheus/morpheus-cli/wiki/Getting-Started](https://github.com/gomorpheus/morpheus-cli/wiki/Getting-Started)<br/>
To learn more about the Morpheus API, visit [https://apidocs.morpheusdata.com](https://apidocs.morpheusdata.com)

## Global Options
```
There are several global options available.

    -v, --version                    Print the version.
        --noprofile                  Do not read and execute the personal initialization script .morpheus_profile
    -C, --nocolor                    Disable ANSI coloring
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help
```
## Common Options
```
There are many common options that are supported by a most commands.

    -O, --option OPTION              Option value in the format -O var="value" (deprecated soon in favor of first class options)
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
        --payload FILE               Payload from a local JSON or YAML file, skip all prompting
        --payload-dir DIRECTORY      Payload from a local directory containing 1-N JSON or YAML files, skip all prompting
        --payload-json JSON          Payload JSON, skip all prompting
        --payload-yaml YAML          Payload YAML, skip all prompting
    -j, --json                       JSON Output
    -d, --dry-run                    Dry Run, print the API request instead of executing it
        --curl                       Dry Run to output API request as a curl command.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
    -U, --username USERNAME          Username for authentication.
    -P, --password PASSWORD          Password for authentication.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -H, --header HEADER              Additional HTTP header to include with requests.
        --timeout SECONDS            Timeout for api requests. Default is typically 30 seconds.
    -y, --yes                        Auto Confirm
    -q, --quiet                      No Output, do not print to stdout
```
## Command Format

```
morpheus [command] [<args>] [options]
```

We divide morpheus into commands. Every morpheus command may have 0-N subcommands that it supports. Commands generally map to the functionality provided in the Morpheus UI.<br/>

You can get help for any morpheus command by using the -h option.<br/>

The available commands and their options are also documented below.
