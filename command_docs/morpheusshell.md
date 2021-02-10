### morpheus shell

```
Usage: morpheus shell
    -e, --exec EXPRESSION            Execute the command expression and exit. Expression can be a single morpheus command or several by using parenthesis and operators (, ), &&, ||, and ;
        --norc                       Do not read and execute the personal initialization script .morpheusrc
    -I, --insecure                   Allow for insecure HTTPS communication i.e. bad SSL certificate
    -Z, --temporary                  Temporary shell. Use a temporary shell with the current remote configuration, credentials and history loaded. Temporary shells do not save changes to remote configuration changes and command history.
    -z, --clean                      Clean shell. Use a temporary shell without any remote configuration, credentials or command history loaded.
    -C, --nocolor                    Disable ANSI coloring
    -V, --debug                      Print extra output for debugging.
    -B, --benchmark                  Print benchmark time after each command is finished
    -h, --help                       Print this help
```
