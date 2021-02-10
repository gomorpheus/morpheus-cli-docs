#### morpheus remote use

```
Usage: morpheus remote use [name]
        --offline                    Do this offline without an api request to refresh the remote appliance status.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

[name] is required. This is the name of a remote to begin using.
Start using a remote, making it the active (current) remote appliance.
This switches the remote context of your client configuration for all subsequent commands.
It is important to always be aware of the context your commands are running in.
The command `remote current` will return the current remote information.
Instead of using an active remote, the -r option can be specified with each command.

It is recommeneded to set a custom prompt to show the current remote name.
For example, add the following to your .morpheusrc file:

  # set your shell prompt to display the current username and remote
  set-prompt "%green%username%reset@%magenta%remote %cyanmorpheus> %reset"

```
