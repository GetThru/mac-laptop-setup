# Mac Laptop Setup Script

This script will install everything you need to start developing for GetThru on a Mac laptop. It installs things, but doesn't necessarily configure them.

Note: not tested on an M1-powered Mac laptop

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
- [Diff-so-fancy](https://github.com/so-fancy/diff-so-fancy), useful for colorful git diffs
- [Starship](https://starship.rs) for a great out-of-the-box command line prompt
- Git, so you have an updated version
- Various updated developer packages

### Languages

- [asdf language version manager](https://asdf-vm.com)
- Erlang
- Elixir
- Node.js
- Python 3 (through Homebrew) for access to Pip

### Databases

- Postgres
- Redis

### Deploy / Devops Stuff

- Kubernetes CLI
- Helm for Kubernetes package management
- AWS Vault for more secure front-end deploys


## Why is there a yes/no option to install things?

If you've installed something before, like Postgres, trying to reinstall it could mess things up. You can also skip sections that were already installed if the script fails part-way through for some reason.


## Managing Services with Homebrew

To see which services are running via Homebrew, type:

```
brew services list
```

Any `status` color besides green means something is wrong.

You can stop, start, and restart services (`postgresql` in this example) with:

```
brew services stop postgresql
brew services start postgresql
brew services restart postgresql
```

Sometimes this will fix a particular service that isn't working.


## Where to go from here

- Set up and configure your command line prompt ([Starship](https://starship.rs) was installed but needs to be configured)
- Configure your preferred IDE or editor
- Clone and set up the main GetThru repositories: [ThruText](https://github.com/GetThru/monorepo) and [ThruTalk](https://github.com/GetThru/talk)
- Clone and run the DevOps helper repository, [team-tools](https://github.com/GetThru/team-tools)
