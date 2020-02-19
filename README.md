# udacity-spark-kafka-sf-crime
For udacity data streaming degree: Analyzing SF crime statistics using kafka and spark

Question 1
- By increasing `spark.streaming.kafka.maxRatePerPartition`, I expect that I will have much higher throughput data on kafka side thus increasing performance for Spark analysis. However, the time to finish the jobs only took 1-2s faster.

Question 2
- Changing `spark.sql.shuffle.partitions` is expected to change the speed that the jobs taken to finish. I had tried 100, 200 and 1000. Turns out that 200 is the optimal.
- The local machine on workspace has 2 cores. I changed `spark.default.parallelism` to only 1 and observed that there's only slight decrease in running time (1s). The optimal one is setting `spark.default.parallelism` to 2.
