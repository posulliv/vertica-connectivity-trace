simple java class to execute `select version()` against a remote vertica database 
with debug logging for the JDBC driver enabled.

# Instructions

1. compile with `mvn clean install -DskipTests`

2. Run like so:

```
./target/simple-oracle-jdbc-test-1.0-SNAPSHOT-executable.jar test_connection --user VERITCA_USER --password VERTICA_PASSWORD --jdbcUrl "jdbc:vertica://vertica:5433/"
```

The `jdbcUrl` parameter can in any valid format that the Vertica JDBC driver supports.

3. Vertica debug logs will be in the `/tmp` folder by default. The location debug logs are written to can be 
changed with the `--logdir` parameter

# Example run

```
❯ ./vertica-connectivty-trace-1.0-SNAPSHOT-executable.jar test_connection --user starburst --password --jdbcUrl "jdbc:vertica://vertica:5433/"
Enter value for --password (Vertica password): 
vertica version: Vertica Analytic Database v23.4.0-0
finished in 31 ms

root@478b64cff1af /tmp 10s
❯ 
```
