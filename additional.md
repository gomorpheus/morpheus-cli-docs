## Environment Variables

Morpheus has only one environment variable that it uses.

### MORPHEUS_CLI_HOME

The **MORPHEUS_CLI_HOME** variable is where morpheus CLI stores its configuration files.
This can be set to allow a single system user to maintain many different configurations
If the directory does not exist, morpheus will attempt to create it.

The default home directory is **$HOME/.morpheus**

To see how this works, run the following:

```shell
MORPHEUS_CLI_HOME=~/.morpheus_test morpheus shell
```

Now, in your new morpheus shell, you can see that it is a fresh environment.
There are no remote appliances configured.

```shell
morpheus> remote list

Morpheus Appliances
==================

You have no appliances configured. See the `morpheus remote add` command.

```

You can use this to create isolated environments (sandboxes), within which to execute your morpheus commands.

```shell
export MORPHEUS_CLI_HOME=~/morpheus_test
morpheus remote add demo https://demo.mymorpheus.com --insecure
morpheus instances list
```

Morpheus saves the remote appliance information, including api access tokens,
to the $MORPHEUS_HOME_DIRECTORY. These files are saved with file permissions **6000**.
So, only one system user should be allowed to execute morpheus with that home directory.
See [Configuration](#Configuration) for more information on the files morpheus reads and writes.

## Configuration

Morpheus reads and writes several configuration files within the $MORPHEUS_CLI_HOME directory.

**Note:** These files are maintained by the program. It is not recommended for you to manipulate them.

### appliances file

The `appliances` YAML file contains a list of known appliances, keyed by name.

Example:
```yaml
:qa:
  :host: https://qa.mymorpheus.com
  :active: true
:production:
  :host: https://mymorpheus.com
```

### credentials file

The `.morpheus/credentials` YAML file contains access tokens for each known appliance.

### groups file

The `.morpheus/groups` YAML file contains the active group information for each known appliance.


## Startup scripts

When Morpheus starts, it executes the commands in a couple of dot files.

These scripts are written in morpheus commands, not bash, so they can only execute morpheus commands and aliases.

### .morpheus_profile file

It looks for `$MORPHEUS_CLI_HOME/.morpheus_profile`, and reads and executes it (if it exists).

This may be inhibited by using the `--noprofile` option.

### .morpheusrc file

When started as an interactive shell with the `morpheus shell` command,
Morpheus reads and executes `$MORPHEUS_CLI_HOME/.morpheusrc` (if it exists). This may be inhibited by using the `--norc` option.

An example startup script might look like this:

```
# .morpheusrc

set-prompt "%cyan%username%reset@%magenta%remote %cyanmorpheus> %reset"
version
remote current
echo "Welcome back %username"
echo

```
