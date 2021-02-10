#### morpheus remote add

```
Usage: morpheus remote add [name] [url]
        --use [true|false]           Start using remote right now. By default this is true if it's the first remote, otherwise false.
        --secure                     Prevent insecure HTTPS communication.  Default is true.
        --insecure                   Allow insecure HTTPS communication.  i.e. Ignore SSL errors. Default is false.
    -O, --option OPTION              Option in the format -O field="value"
    -P, --prompt                     Always prompts. Use passed options as the default value.
    -N, --no-prompt                  Skip prompts. Use default values for all optional fields.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Add a new remote to your morpheus client configuration.
[name] is required. A unique name for your appliance. eg. demo
[url] is required. The URL of your appliance eg. https://demo.morpheusdata.com
First, this inspects the remote url to check the appliance status and version.
If remote is ready, it will prompt to login, see the command `login`.
If remote is freshly installed, it will prompt to initialize the appliance, see the command `setup`.
The option --use can be included to start using the new remote right away.
The remote will be used by default if it is the first remote in the configuration.
The --quiet option can be used to to skip prompting.

```
