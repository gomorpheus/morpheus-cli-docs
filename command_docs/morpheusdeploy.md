### morpheus deploy

```
Usage: morpheus deploy [environment]
    -y, --yes                        Auto Confirm
    -q, --quiet                      No Output, do not print to stdout
    -r, --remote REMOTE              Remote name. The current remote is used by default.
        --remote-url URL             Remote url. This allows adhoc requests instead of using a configured remote.
    -T, --token TOKEN                Access token for authentication with --remote. Saved credentials are used by default.
    -U, --username USERNAME          Username for authentication.
    -P, --password PASSWORD          Password for authentication.
    -I, --insecure                   Allow insecure HTTPS communication.  i.e. bad SSL certificate.
    -d, --dry-run                    Dry Run, print the API request instead of executing it.
        --curl                       Curl, print the API request as a curl command instead of executing it.
        --scrub                      Mask secrets in output, such as the Authorization header. For use with --curl and --dry-run.
    -C, --nocolor                    Disable ANSI coloring
    -B, --benchmark                  Print benchmark time and exit/error after the command is finished.
    -V, --debug                      Print extra output for debugging.
    -h, --help                       Print this help

Deploy to an instance using the morpheus.yml file, located in the working directory.
[environment] is optional. Merge settings under environments.{environment}. Default is no environment.

First the morpheus.yml YAML file is parsed, merging the specified environment's nested settings.
The specified instance must exist and the specified deployment version must not exist.
If the settings are valid, the new deployment version will be created.
If is a file type deployment, all the discovered files are uploaded to the new deployment version.
Finally, it deploys the new version to the instance using any specified config options.

The morpheus.yml should be located in the working directory.
This YAML file contains the settings that specify how to execute the deployment.

File Settings
==================

* name - (required) The instance name being deployed to, also the default name of the deployment.
* version - (required) The version identifier of the deployment being created (userVersion)
* deployment - The name of the deployment being created, name is used by default
* type - The type of deployment, file, 'git' or 'fetch', default is 'file'.
* script - The initial script to run, happens before finding the files to be uploaded.
* files - (required) List of file patterns to use for uploading files and their target destination. 
          Each item should contain path and pattern, path may be relative to the working directory, default pattern is: '**/*'
          only applies to type 'file'
* url - (required) The url to fetch files from, only applies to types 'git' and 'fetch'.
* ref - The git reference, default is master (main), only applies to type git.
* config - Map of deployment config options depending on deployment type
* options - alias for config
* post_script - A post operation script to be run on the local machine
* stage_only - If set to true the deploy will only be staged and not actually run
* environments - Map of objects that contain nested properties for each environment name

It is possible to nest these properties in an "environments" map to override based on a passed environment.

Example
==================

name: mysite
version: 5.0
script: "rake build"
files: 
- path: build
environments:
  production:
    files:
    - path: production-build


Git Example
==================

name: morpheus-apidoc
version: 5.0.0
type: git
url: "https://github.com/gomorpheus/morpheus-apidoc"

```
