# spark-clickhouse-connector

Read and write clickhouse cluster in parallel

![image](https://user-images.githubusercontent.com/22080060/113481081-27627280-94ca-11eb-8855-ec66fbc4bef1.png)

# Read

![image](https://user-images.githubusercontent.com/22080060/113481254-09494200-94cb-11eb-8c3f-304d5c9e9624.png)

`The actual number of partitions = the number of scan partitions * the number of shard`

The scan partition will be assigned to each shard, and each shard will get data from ClickHouse through the conditions of the scan partition

# Write

![image](https://user-images.githubusercontent.com/22080060/113481211-cbe4b480-94ca-11eb-83f5-c869c273d069.png)

A write partition will be allocated to a shard, and the data will be written to the clickhosue that can be reached under the shard
