#### morpheus storage-buckets list-files

```
Usage: morpheus storage-buckets list-files [provider:/path]
    -a, --all                        Show all files, including subdirectories under the /path.
    -m, --max MAX                    Max Results
    -o, --offset OFFSET              Offset Results
    -s, --search PHRASE              Search Phrase
    -S, --sort ORDER                 Sort Order. DIRECTION may be included as "ORDER [asc|desc]".
    -D, --desc                       Reverse Sort Order
    -Q, --query PARAMS               Query parameters. PARAMS format is 'foo=bar&category=web'
    -j, --json                       JSON Output
    -y, --yaml                       YAML Output
        --csv                        CSV Output
        --csv-delim CHAR             Delimiter for CSV Output values. Default: ','
        --csv-newline [CHAR]         Delimiter for CSV Output rows. Default: '\n'
        --csv-quotes                 Wrap CSV values with ". Default: false
        --csv-no-header              Exclude header for CSV Output.
    -f, --fields x,y,z               Filter Output to a limited set of fields. Default is all fields for json,csv,yaml.
        --all-fields                 Show all fields present in the data.
        --wrap                       Wrap table columns instead hiding them when terminal is not wide enough.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

List files in a storage bucket. 
Include [/path] to show files under a directory.
```
