# Terminal

The Morpheus CLI gem provides the **Morpheus::Terminal** class for use in your own ruby scripts and modules. Terminal can share the same configuration with the `morpheus` binary command, or it may be kept separate with its own [Home Directory](#home-directory).

If you would prefer to interact with the Morpheus API directly and are not interested in executing the CLI commands in their familiar format, then consider using the lower level [APIClient](/gomorpheus/morpheus-cli/wiki/APIClient) instead.

## Home Directory

The `morpheus` binary itself uses Terminal to execute commands too. So by default, your scripts will share the same environment. That means you will be able to use all the same remote appliance names, urls and saved credentials. The same active appliance and/or group is used by default too. 

If you do not want **Morpheus::Terminal** to share its configuration with the `morpheus` binary, then simply use a different `MORPHEUS_CLI_HOME`.

The default home directory is `~/.morpheus`.

### Set Home Directory

You can export the home directory in your bash environment.

```bash
export MORPHEUS_CLI_HOME="~/morpheus-terminal"
```

Alternatively, you can set the home directory in your script.

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new()
terminal.home_directory = "~/morpheus-terminal"
terminal.execute("whoami")
```

## Terminal Usage

If you have already configured the CLI using `morpheus remote add` to connect to your appliance, then you can just execute morpheus commands the same way you would in bash or morpheus shell.


## Execute Commands with Terminal

Here is an example that prints the first 100 users.

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
terminal.execute("users list -m 100")
```

## Add Remote with Terminal

You can also have your script add and remove its own remote each time.

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
# terminal.execute("remote get term -q && remote remove term -y")
terminal.execute("remote add term https://mymorpheus.com --insecure --use -y")
terminal.execute("remote users list -m 100")
terminal.execute("remote remove term -y")
```

Note that this will prompt for input values to login. The option `-N`  can be used to supress prompting, but you will need to pass all the required options.

## Login with Terminal

You can also have your script login directly

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
terminal.execute("login")
```

Or to only login if needed you could use:

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
terminal.execute("whoami -q || login")
```

The above example could be written this way as well:

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
exit_code, err = terminal.execute("whoami -q")
if exit_code != 0
    terminal.execute("login")
end
```

## Login with Terminal

You can also have your script add and remove its own remote each time.

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new
# terminal.execute("remote get term -q && remote remove term -y")
terminal.execute("remote add term https://mymorpheus.com --insecure --use -y")
terminal.execute("remote users list -m 100")
terminal.execute("remote remove term -y")
```

## Terminal Output

Terminal allows directing where output is written to.

You can customize your client's stdin, stdout, sterr and home directory:

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new(STDIN, STDOUT, STERR, "~/.morpheus")
```

The above example passes all the default values, so it is the same as:

```ruby
require 'morpheus'
terminal = Morpheus::Terminal.new()
```

You can have terminal write output to a file instead. Use `file.sync = true` to write the file continuously, as commands are executed, rather than when the terminal is closed.

```ruby
require 'morpheus'
outfile = File.new("morpheus-terminal.out", "w+")
outfile.sync = true
outfile = morph_stdout
terminal = Morpheus::Terminal.new(STDIN, outfile, outfile)
terminal.execute("instances list")
```

To inspect the above example's output, you could use:

```bash
tail morpheus-terminal.out
```

### Terminal Return Value

The return value of `terminal.execute(cmd)` is an Array with two values in the format `[0,nil]`. The first value is the exit code as a number, `0` indicates the command was successful. An error will be indicated by any non zero exit code such as `1`. The second value is the error message a string, `nil`. A command can fail and return non-zero with a nil error message, although is is typical for a command to return the error message with a bad exit code.

If you want to work with JSON data, you're better off using [APIClient](/gomorpheus/morpheus-cli/wiki/APIClient) instead.
