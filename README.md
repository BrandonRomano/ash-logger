# Logger

Logger is an [Ash](https://github.com/ash-shell/ash) module that offers sensible logging in Bash.

## Getting started

Ash-Logger is part of the Ash core, so you can just start using it in your Ash modules.

## Example Usage

Here's some example usage:

```sh
# Logs + Alerts
Logger__log "Standard logs"
Logger__alert "Alerts"

# Custom Prefix
Logger__set_prefix "Custom Prefix"

# Errors + Warnings
Logger__error "Errors"
Logger__warning "Warnings"

# Prompts
Logger__prompt "Prompts: "; read variable

# Success
Logger__success "Success: $variable"

# Prefix Switch
Logger__disable_prefix
Logger__warning "No Prefix"
Logger__enable_prefix
Logger__success "Prefix"
```

Outputs:

![Imgur](http://i.imgur.com/lGBwpaa.png?1)

### Logging to a file

Logger supports logging to a file by using `Logger__log`.  You can specify the file to log to in your [~/.ashrc file](https://github.com/ash-shell/ash#the-ashrc-file) with the variable `LOGGER_OUTPUT_FILE`.

In your `~/.ashrc` file:

```bash
export LOGGER_OUTPUT_FILE="/Users/brandon/desktop/ashlogs.log"
```

In code:

```
Logger__debug "Hello World!"
```

## License

[MIT](license.txt)
