# pantheon-tools
Tools to run actions against a Pantheon site

# Pre-requisites
1. Install [Terminus](https://github.com/pantheon-systems/terminus).
2. Add Terminus to your Path.  For example, if Terminus is installed at `~/.composer/vendor/bin/terminus` then you need to add that directory to your path.
3. Add the directory containing these scripts to your Path.

## How to add something to your path
  E.g.

```
export PATH="$PATH:$HOME/.composer/vendor/bin"
export PATH="$PATH:$HOME/Sites/pantheon-tools"
```

You typically add these lines to `~/.profile` or `~/.bash_profile`.

Note that an alias will not work.

# Usage
1. This may be getting a lot of updates, so first ensure that you have the latest version.
`git pull`
2. The scripts are totally interactive.  Just run them.  E.g.:
```
pantheon-update
```
