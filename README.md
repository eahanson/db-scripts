# DB Scripts

Contains shell scripts for starting, stopping, and restarting a Postgres database that has been installed
via [asdf](https://asdf-vm.com) and whose data directory is stored in a `priv/postgres` subdirectory of
the current working directory.

I often have multiple projects on my computer that require different versions of Postgres. Asdf allows me to
easily have mutliple versions of Postgres installed, and storing the database's files in each project directory
allows me to use versions of Postgres whose data formats are incompatible. Storing the database's files in each
project directory also allows me to delete the entire DB without impacting other projects.

Another solution would be to use Docker, but I find that Docker adds complexity and slows down development
enough that I don't want to use it on simpler projects.

## Usage

`db-start`: starts a Postgres database, or fails with a (hopefully) helpful error message.

`db-stop`: stops any running Postgres database.

`db-restart`: stops and then starts a Postgres database.
