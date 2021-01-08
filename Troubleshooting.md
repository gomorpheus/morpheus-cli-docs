# Troubleshooting

This document is a resource for troubleshooting errors encountered with the Morpheus CLI.

Please feel free to log any issues you find with the Morpheus CLI in Github. See [Issues](https://github.com/gomorpheus/morpheus-cli/issues).

## Common Errors

### SSL Certificate Error

If you are using HTTPS and are have an unverified SSL Certificate, the CLI will raise an exception. This error can be supressed by configuring your client with `verify_ssl: false` to ignore SSL Certificate errors.  Always be sure to point your client to a trusted appliance `url`.

```bash
morpheus remote add demo https://mymorpheus.com --insecure`
```

You can also mark an existing appliance as insecure.

```bash
morpheus remote update demo --insecure`
```

## Known Issues

This is a list of outstanding well known issues with the Morpheus CLI.  This list will hopefully remain very small.  Look for issues to be fixed quickly.

### shell backspace is broken on Windows 

For some reason, backspace does not seem to always work correctly when using `morpheus shell` on Windows.  It seems that the backspace key event registers, but the characters do not appear to be erased.
