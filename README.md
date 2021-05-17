# Mac Laptop Setup Script

This script will install everything you need to start developing on a Mac laptop.

## Running the Script

Download the script:

```
curl --remote-name https://raw.githubusercontent.com/getthru/mac-laptop-setup/master/setup_laptop
```

Run the script:

```
sh setup_laptop 2>&1 | tee ~/laptop.log
```

Optionally, review the log:

```
less ~/laptop.log
```

## What It Installs

### System-level Tools

- Homebrew
- AWS CLI
- Watchman
- Diff-so-fancy

### Languages

- asdf language version manager
- Erlang
- Elixir
- Node.js

### Databases

- Postgres
- Redis
