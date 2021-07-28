# pantheon-tools
Tools to run actions against a Pantheon site.

## Pre-requisites
1. Install [Terminus](https://github.com/pantheon-systems/terminus).
2. `terminus auth:login` to store an access token.
3. Upload your SSH key to the Pantheon dashboard.
4. Add Terminus to your Path.  For example, if Terminus is installed at `~/.composer/vendor/bin/terminus` then you need to add `~/.composer/vendor/bin` to your path.
5. Add the directory containing pantheon-tools to your Path.

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

The script will ask you questions along the way (and give you hints when there's ways to add arguments to make things faster).

## Scripts

### pantheon-security-update

Run security updates on a Pantheon site by first creating a new multi-dev environment.

### pantheon-multidev-create

Create a new multi-dev environment.

### pantheon-multidev-merge

Merge a multi-dev environment into master (the dev environment).

### pantheon-quick-deploy

Quickly deploy something from dev->test->live.

### pantheon-commit-and-quick-deploy

Commit any local changes and then deploy them.

### pantheon-db-dump

Dump a database from any Pantheon site.  Even VIP clients that require an SSH tunnel to connect to the database.

### pantheon-db-cli

Connect to the database of any Pantheon site.  Even VIP clients that require an SSH tunnel to connect to the database.

### pantheon-module-report

Get a list of which sites use which version of a module.

### pantheon-sites-report

Get a metric about all sites (e.g. PHP version, or Upstream).

### pantheon-offboard

Offboard a staff member from your organization.

### pantheon-deploy

Deploy dev->test or test->live.

### pantheon-drupal-status-report

Report a summary of the Status Report for every Drupal site.
