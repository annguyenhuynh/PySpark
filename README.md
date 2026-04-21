* union(): matches columns by order, so if the column order is different, your data can get mixed up. Can use .distinct() to remove duplicates columns

* unionByName(): matches columns by name. If you have additional columns in one dataframe, you can use **allowMissingColumns=True**

* Nested inside **expr** is "pure" SQL queries in SELECT clause