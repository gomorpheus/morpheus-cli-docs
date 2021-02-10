#### morpheus library-option-lists add

```
Usage: morpheus library-option-lists add [name] [options]
        --name VALUE                 Name
        --description VALUE          Description (optional)
        --type VALUE                 Type - Option List Type. eg. rest, api, ldap, manual. Default: rest
        --visibility VALUE           Visibility (optional). Default: private
        --sourceUrl VALUE            Source Url - A REST URL can be used to fetch list data and is cached in the appliance database.
        --ignoreSSLErrors [on|off]   Ignore SSL Errors (optional)
        --realTime [on|off]          Real Time (optional)
        --sourceMethod VALUE         Source Method. Default: GET
        --apiType VALUE              Option List - The code of the api list to use, eg. clouds, servers, etc.
        --sourceUsername VALUE       Source Username (optional) - An LDAP Username for use when type is 'ldap'.
        --sourcePassword VALUE       Source Username (optional) - An LDAP Password for use when type is 'ldap'.
        --ldapQuery VALUE            LDAP Query (optional) - LDAP Queries are standard LDAP formatted queries where different objects can be searched. Dependent parameters can be loaded into the query using the <%=phrase%> syntax.
        --initialDataset VALUE       Initial Dataset (optional) - Create an initial json dataset to be used as the collection for this option list. It should be a list containing objects with properties 'name', and 'value'. However, if there is a translation script, that will also be passed through.
        --translationScript VALUE    Translation Script (optional) - Create a js script to translate the result data object into an Array containing objects with properties name, and value. The input data is provided as data and the result should be put on the global variable results.
        --requestScript VALUE        Request Script (optional) - Create a js script to prepare the request. Return a data object as the body for a post, and return an array containing properties name and value for a get. The input data is provided as data and the result should be put on the global variable results.
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

Create a new option list.
```
