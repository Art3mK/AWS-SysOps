## Multi-AZ failover

- MySQL, Oracle, PostgreSQL -> replication
- SQL Server -> mirroring

`Failover -> RDS DNS endpoint doesn't change`

what for:
- HA
- Backups from secondary
- Restores are take from secondary
- Not a scaling solution
- For scaling use read replicas

You can force failvoer by rebooting instance. `RebootDBInstance` API call

## Read Replicas

scale out for read-heavy workloads, async, `CreateDBInstanceReadReplica` API

- scaling beyond compute or I/O capacity of a single DB instance
- reporting/data warehousing on replicas
- have own DNS endpoint
- could be promoted to standalone DB
- up to 5 read replicas for MySQL, PostgreSQL & MariaDB
- could be in different regions
- async only
- supported for multi-az
- RR can't be multi-az
- chained replication is allowed
- snapshots/automated backups from RR
- `ReplicaLag` cloudwatch metric

### engines

- MySQL
    - native sync
- PostgreSQL
    - native sync
- MariaDB
    - native sync
- Aurora
    * SSD backed virtualized storage layer, replicas share the same storage

### Creating read replicas

```
if !Mutli-Az
    snapshot of primary DB, brief I/O suspension for ~1 minute
else
    snapshot of secondary DB, no performance hits for primary
```
