## Sequel

```
Sequel: The Database Toolkit for Ruby
Usage: sequel [options] <uri|path> [file]

Examples:
  sequel sqlite://blog.db
  sequel postgres://localhost/my_blog
  sequel config/database.yml

For more information see http://sequel.jeremyevans.net

Options:
    -c, --code CODE                  run the given code and exit
    -C, --copy-databases             copy one database to another
    -d, --dump-migration             print database migration to STDOUT
    -D, --dump-migration-same-db     print database migration to STDOUT without type translation
    -e, --env ENV                    use environment config for database
    -E, --echo                       echo SQL statements
    -I, --include dir                specify $LOAD_PATH directory
    -l, --log logfile                log SQL statements to log file
    -L, --load-dir DIR               loads all *.rb under specifed directory
    -m, --migrate-directory DIR      run the migrations in directory
    -M, --migrate-version VER        migrate the database to version given
    -N, --no-test-connection         do not test the connection
    -r, --require LIB                require the library, before executing your script
    -S, --dump-schema filename       dump the schema for all tables to the file
    -t, --trace                      Output the full backtrace if an exception is raised
    -h, -?, --help                   Show this message
    -v, --version                    Show version
```
