# Database Migrations

_Database migration_ is the process of migrating data from one or more source databases to one or more target databases by using a database migration service. When a migration is finished, the dataset in the source databases resides fully, though possibly restructured, in the target databases. Clients that accessed the source databases are then switched over to the target databases, and the source databases are turned down.



The most important data migration terms for these documents are defined as follows:

**source database:** A database that contains data to be migrated to one or more target databases.

**target database:** A database that receives data migrated from one or more source databases.

**database migration:** A migration of data from source databases to target databases with the goal of turning down the source database systems after the migration completes. The entire dataset, or a subset, is migrated.

**homogeneous migration:** A migration from source databases to target databases where the source and target databases are of the same database management system from the same provider.

**heterogeneous migration:** A migration from source databases to target databases where the source and target databases are of different database management systems from different providers.

**database migration system:** A software system or service that connects to source databases and target databases and performs data migrations from source to target databases.

**data migration process:** A configured or implemented process executed by the data migration system to transfer data from source to target databases, possibly transforming the data during the transfer.

**database replication:** A continuous transfer of data from source databases to target databases without the goal of turning down the source databases. Database replication (sometimes called _database streaming_) is an ongoing process.



In a migration, achieving truly zero downtime for clients is impossible; there are times when clients cannot process requests. However, you can minimize the duration that clients are unable to process requests in several ways (near-zero downtime):

* You can start your test clients in read-only mode against the target databases long before you switch the clients over. With this approach, testing is concurrent with the migration.
* You can configure the amount of data being migrated (that is, in flight between the source and target databases) to be as small as possible when the switch over period approaches. This step reduces the time for draining because there are fewer differences between the source databases and the target databases.
* If new clients operating on the target databases can be started concurrently with existing clients operating on the source databases, you can shorten the switch over time because the new clients are ready to execute as soon as all data is drained.

The expectation is that a database migration is consistent. In the context of migration, _consistent_ means the following:

* **Complete.** All data that is specified to be migrated is actually migrated. The specified data could be all data in a source database or a subset of the data.
* **Duplicate free.** Each piece of data is migrated once, and only once. No duplicate data is introduced into the target database.
* **Ordered.** The data changes in the source database are applied to the target database in the same order as the changes occurred in the source database. This aspect is essential to ensure data consistency.

**Reference:**

[https://cloud.google.com/architecture/database-migration-concepts-principles-part-1#:\~:text=Database%20migration%20is%20the%20process,restructured%2C%20in%20the%20target%20databases.](https://cloud.google.com/architecture/database-migration-concepts-principles-part-1#:\~:text=Database%20migration%20is%20the%20process,restructured%2C%20in%20the%20target%20databases.)\


