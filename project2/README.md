# SF Crime Statistics with Spark Streaming

*How did changing values on the SparkSession property parameters affect the throughput and latency of the data?*

In the Spark UI, I noticed that jobs completed much more quickly (in 0.3s vs 5-7s) depending on the SparkSession parameters.

*What were the 2-3 most efficient SparkSession property key/value pairs? Through testing multiple variations on values, how can you tell these were the most optimal?*

Following the guidelines on https://spark.apache.org/docs/latest/sql-performance-tuning.html and https://spark.apache.org/docs/latest/tuning.html, I found the most optimal settings to be adjusted were `spark.default.parallelism`:20 and `spark.sql.shuffle.partitions`:10.

