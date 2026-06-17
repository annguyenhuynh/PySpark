* union(): matches columns by order, so if the column order is different, your data can get mixed up. Can use .distinct() to remove duplicates columns

* unionByName(): matches columns by name. If you have additional columns in one dataframe, you can use **allowMissingColumns=True**

* Nested inside **expr** is "pure" SQL queries in SELECT clause

* To change the number of cores, instances, and memory, configure the desired values when defining Spark Session

```
spark = SparkSession.builder \
    .master("local[*]") \
    .appName("test") \
    **.congig("spark.executor.instances",4) \**
    **.config("spark.executor.cores",4)** \
    **.config("spark.executor.memory", "512M")
    .getOrCreate()