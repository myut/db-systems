### Why NoSQL



---

## Case Studies:

1. Google App Engine:

Stores: Cloud SQL, Datastore, Cloud Storage.

**Datastore**
* Built for scale(Size and Traffic)
  * 2 **Trillion** operations per month.
  * Fully managed **NoSQL** solution.

**Cloud SQL**
* Pure Mysql


MySQL: Supports SQL queries which are standard
NoSQL: Now supports a subset of SQL. Beyond SQL: contains all/any(In).
       Scales in the size of the result set.
       
NoSQL: Aggregates: MapReduce for aggregates. Materialized views to track updates.
SQL: Group By.

**SQL:** put average info on map.
SELECT AVG(people.age), cities.name, cities.latitude, cities.longitude
FROM people, cities
WHERE people.city_id = cities.city_id
GROUP BY people.city_id

SQL: Joins. Queries to everything is better.


Transactions:
**NoSQL**: Entity groups to handle transactions.

Cross entity transactions are possible. 2-PC commit. Doesn't scale if number of transactions are large. Limited to 5 entities. 

Replication at transaction level. No master. 

Parallel replication: scales based on the number of resources.

**SQL**: Much better transactions support. 


**Replication**

MySQL: 
Traditionally:
Single master to gurantee strong consistency. 
Async. replicates changes to its slave. 
If master crashes you loose data

However, Google app engine synchronously replicates changes.

**Scalability**



Off the shelf software. 

SQL works best when data fits in memory.

Store archived listings in the datastore.
