# Questions-AS-PostgreSQL-DBA

```
1. 1. How connection is established in postgres?
2. Explain the postgres architecture ?
3. What are some important background processes in postgres?
4. What are the memory components in postgres?
5. When wal writer write data to wal segement?
6. When bgwriter writes data to disk?
7. What are some wal related parameter in postgrs.conf file? 
8. What is checkpoint? When checkpoint happens in postgres?
9. Lets say your work_mem is 4MB. However your query is doing heavy sorting, for which work_mem required might be more than 4MB. So will the query execution be successful?
10. What are the different phases of statement processing?
11. Which parameters controls the behaviour of BGWriter?
12. Does postgres support direct i/o.?
13. How authentication happens in postgres?
14. What is the significance of pg_ident.conf file?
15. What is this wal_level parameter , different values of wal_level?
16. What is visibility map in postgres?
17. What is free space mapping(FSM) in postgres?
18. What is initial fork?
19. What is  TOAST?
20. What happens in the background during vacuuming process?
21. What is transaction id wraparound? How to overcome it.
22. What is the significance of search_path in postgres?
24. What are the advantages and disadvantages of MVCC?
25. Difference between pg_log, pg_clog, pg_xlog?
26. What is ctid?
27. What is oid?
28. difference between oid and relfilenode?
29. Difference between postgres.conf and postgres.auto.conf file?
30. What is timeline in postgres?
31. what is full page write in postgres?
32. What is xmin and xmax in postgres?
33. What is a ring buffer in postgres?
34. What do you mean by postgres cluster?
35. What is single user mode in postgres?
36. What is a timeline history file?
37. Are you aware of archive_library feature in postgres 15?
38. What is the use of wal files/segments?
39. What is LSN?
40. What are the three special transaction ids in  postgres?

---------------------------------------For DBA ---------------------------------------------


1. What is the default port in postgres?
2. What is the default block size in postgres? Can we set different block size?
3. What is a tablespace?
4. What are the tablespaces created by default after installing postgres cluster?
5. What is the use of temporary tablespace? 
6.What are the default databases created after setting up postgres cluster? 
7.What is the significance of template0 and template1 databases? What the difference between these two?
8. What are common database object names in postgres compare to industry terms.
9. Difference between user and schema in postgres?
10. Difference between role and user in postgres? Can we convert a role to user?
11. Difference mode to stop a postgres cluster using pg_ctl?
12. Can you give comparison of shutdown modes between oracle and postgres?
13. Can we stop a particular database in postgres cluster?
14.  What are foreign data wrappers? What is its use?
15.  what is the use of share_preload_libraries in postgres.conf file?
16. what different types of streaming replications are present in postgres? And which parameters control that.
18.What is random page cost?
19.Difference between explain and explain analyze in postgres?
20. What are the different datatypes in postgres?
21. what is the maximum file size of table or index in postgres? Can we increase that ?
22. Is there a way in which we can rebuild/reorg a table online to release free space?
23. How pg_repack works internally?
24. How can i check the version of postgres?
25. What is the latest version of postgres in market?
26. While dropping a postgres database i am getting error? What might be the issue?
27. What are some key difference between oracle and postgres?
28. Between postgres and nosql database like mongodb , which one is better?
29. What is table partitioning in postgres? What are the advantages?
30. How you monitor long running queries in postgres?
31. How to kill a session in postgres?
32. What is an extension in postgres? Which extensions you have used ?
pg_stat_statements
pg_track_settings
pg_profile
33. What are the popular tools for managing backup and recovery in postgres?
34. How can we use connection pooling in postgres?
35. Which utility is used to upgrade postgres cluster?
36. How can we encrypt specific columns in postgres?
37. What is the use of pgbench utility?
38. What is difference between pg_cancel_backend vs pg_terminate_backend?
5. Do we have synonyms in postgres?
5. How can we convert a non partitioned table to partitioned table in postgres?
5. How can we convert a non partitioned table to partitioned table in postgres?
5. Can we create invisible index in postgres?
5. Suppose we have some views using a table  and if drop that table, what will be the impact on those views?
5. Difference between open source installation and edb installation?
5. What is the difference between pgpool and pgbouncer?

------------------------------------Maintenance------------------------------------------------
1. What is vacuuming in postgres?
2. Difference between vacuum and vacuum full?
3. What do you mean by vacuum freeze? And when we use it?
4. What is auto vaccuming in postgres?
5. How can we increase the performance of auto vacuuming?
6. How can i disable autovacuuming?
7. What is the data fragmentation or bloating in postgres?
8. Difference between normal transaction id and frozen transaction id?
9. How statistics were updates in postgres?
10. What CLUSTER command does? When and how it helps.?
11. What is reindexing and when we should do reindex?
1. How can i rebuild index?
2. Will there be any impact on the database, if i run reindex command .
2. What happens internally when we rebuild indexes?
12. Lets says autovacuuming already running in background and You again ran the vaccum command manually? What will happen?
13. Can i disable autovacuum for few tables in the database?
14. What is fill factor and how it impacts the autovacuuming performance.
15. What exactly happens when we do vacuum full?

--------------------------------Replication------------------------------------------------

1. Explain the basic streaming replication architecture.
2. How can you check whether the database is primary or standby(replication).
3. I have a master and slave setup with streaming replication. Now I want to break the replication and open the standby server for some testing purpose and once the testing is done, the server again need to be a standby of that primary with replication enabled. How can i do that?
4. How pg_rewind works?
5. How can i do switchover in postgres without efm?
6.Difference between standby.signal and recovery.signal?
7. In streaming replication which additional processes run on primary and standby?
8. What is the default streaming replication mode SYNC or ASYNC?
9. Explain different types of replications methods available in postgres?
10. What is the significance of the parameter synchronous_commit?
11. Suppose A is primary and B is standby ? Now failover happened and then A becomes standby and B becomes primary. Now i want to make the A as primary again and B as standby . How can i achieve that?
12. Explain the architecture of EFM?
13. What are some common reasons which cause streaming replication to fail.
14. What are the changes related to recovery.conf happened in postgres 12.
15. When we do failover, what happens in the timeline.
16. Like snapshot standby in oracle, can we use slave server in postgres as snapshot standby and revert it back to slave server once testing is done?
17.Is there any mandatory parameter for pg_rewind to work?
18.Is replication possible between different versions of postgres?
19.What is replication slot?
5. Do you see any disadvantage of replication slot?
5. How many types of replication slots are there?

--------------------------Backup &  Recovery ------------------------------

1. Explain different backup methods in postgres?
5. difference between pg_dump and pg_dumpall?
5. Can i take backup of complete cluster using pg_dump?
5. What is the use of -globals options in pg_dumpall?
1. What pg_basebackup does internally?
1. Explain how postgres does crash recovery?
1. Can we take incremental backup using postgres? and how?
1. Which important parameter is used for point in time recovery ?
1. What do you mean by continuous archiving in postgres?
17.Can I take export of only users using pg_dump?
3. Different type of indexes present in postgres ?
4.  Does create index puts lock on the table? If yes , then any workaround to avoid this locking?
5. What is index only scan in postgres?

---------------------PATCH & UPGRADE---------------
1. What is major version upgrade and minor version upgrade in postgres?
2. Explain how you do a major upgrade in postgres?
3. What is the user of link option in pg_upgrade?
4. What are the advantages and disadvantages of using link option?
4. How do you find which objects are bloated in db?
```
