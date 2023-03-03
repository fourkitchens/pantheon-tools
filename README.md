# pantheon-tools
Tools to improve your development workflow on Pantheon sites including:
* Tips to make your workflow smoother/faster/less-risky.
* automating important steps that are easy to forget.

This includes things like:
* Sort out configuration problems before you move on to the next step.
* Create a backup before deploying.
* Merge the main/master branch into a multidev before going the other direction.
* Pause a deployment if there's undeployed code in the next environment. 
* General standardization around development process.
* etc.

## Pre-requisites
1. Install [Terminus](https://github.com/pantheon-systems/terminus).
2. `terminus auth:login` to store an access token.
3. Upload your SSH key to the Pantheon dashboard.
4. Add Terminus to your Path.  For example, if Terminus is installed at `~/.composer/vendor/bin/terminus` then you need to add `~/.composer/vendor/bin` to your path.
5. Use Git to checkout this pantheon-tools repository, maybe to the same place you store your other code projects.  
6. Add the directory containing pantheon-tools to your Path.

### How to add something to your path
  E.g.

```
export PATH="$PATH:$HOME/.composer/vendor/bin"
export PATH="$PATH:$HOME/path/to/pantheon-tools"
```

Depends on the system you are using, you need to add the above two paths to `~/.profile`, `~/.bash_profile`, or `~/.zshrc`.

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
