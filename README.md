# pantheon-tools
Tools to run actions against a Pantheon site

## Pre-requisites
1. Install [Terminus](https://github.com/pantheon-systems/terminus).
2. Add Terminus to your Path.  For example, if Terminus is installed at `~/.composer/vendor/bin/terminus` then you need to add `~/.composer/vendor/bin` to your path.
3. Add the directory containing pantheon-tools to your Path.

### How to add something to your path
  E.g.

```
export PATH="$PATH:$HOME/.composer/vendor/bin"
export PATH="$PATH:$HOME/Sites/pantheon-tools"
```

You typically add these lines to `~/.profile` or `~/.bash_profile`.

Note that an alias will not work.

## Usage
1. This may be getting a lot of updates, so first ensure that you have the latest version.
```
cd /path/to/the/pantheon-tools
git pull
```
2. The scripts are totally interactive.  Just run them.  E.g.:
```
pantheon-security-update
```

## Scripts

### pantheon-security-update

Run security updates on a Pantheon site by first creating a new multi-dev environment.

### pantheon-quick-deploy

Quickly deploy something from dev->test->live.

### pantheon-commit-and-quick-deploy

Commit any local changes and then deploy them.

### pantheon-db-dump

Dump a database from any Pantheon site.  Even VIP clients that require an SSH tunnel to connect to the database.

### pantheon-db-cli

Connect to the database of any Pantheon site.  Even VIP clients that require an SSH tunnel to connect to the database.
