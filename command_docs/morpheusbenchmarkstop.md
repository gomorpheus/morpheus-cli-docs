#### morpheus benchmark stop

```
Usage: morpheus benchmark stop [name]
        --exit CODE                  Exit code to end benchmark with. Default is 0 to indicate success.
        --error ERROR                Error message to include with a benchmark that failed.
    -q, --quiet                      No Output, do not print to stdout
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Stop recording a benchmark.
[name] is optional. This is the name of the benchmark to stop. 
The last benchmark is used by default.
```
