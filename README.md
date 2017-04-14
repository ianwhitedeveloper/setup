# Laptop Setup - Ruby Microservices Workshop

## Software Prerequisites

- Ruby (minimum version: 2.4)
- Postgres (minimum version: 9.5)
- Git (minimum version: 2)
- GCC (already included with Apple XCode Developer Tools)

## Quick Test of Your Setup

### Start Postgres

If you've installed Postgres through Homebrew on Mac:

```
launchctl load -w ~/Library/LaunchAgents/homebrew.mxcl.postgresql.plist
```

If you don't want to start it as a daemon, open a new terminal window and run:

```
postgres -D /usr/local/var/postgres
```

On nix:

```
sudo systemctl start postgresql
```

### Clone the Test Repository

Clone the skeleton of the example project that we'll be working with through the course of the workshop:

```
git clone git@github.com:eventide-tutorial/account-component-skeleton.git
```

### Change Directory to the Project Directory

```
cd account-component-skeleton
```

### Install the Gems

```
./install_gems.sh
```

### Create the Database

A database named `event_source` along with a user of the same name will be created.

Run:

```
bundle exec evt-pg-recreate-db
```

### Run the Test

```
./test.sh
```

If everything is working correctly, you should see the following output:

```
Running /Users/sbellware/projects/eventide/tutorial/account-component-skeleton/test/automated/database_connection.rb
Database Connection
  Connects on first use

Finished running 1 file
Ran 1 test in 0.052s (19.264s tests/second)
1 passed, 0 skipped, 0 failed, 0 total errors
```
