#### morpheus alias add

```
Usage: morpheus alias add [name]='[command]'
    -e, --export                     Export this alias to your .morpheus_profile for future use
    -h, --help                       Print this help

Define a new alias.
[name] is required. This is the alias name. It should be one word.
[command] is required. This is the full command wrapped in quotes.
Aliases can be exported for future use with the -e option.
The `alias add` command can be invoked with `alias [name]=[command]`

Examples: 
    alias cloud=clouds
    alias ij='instances get -j'
    alias new-hosts='hosts list -S id -D'
For more information, see https://github.com/gomorpheus/morpheus-cli/wiki/Alias
```
