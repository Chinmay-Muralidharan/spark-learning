Day 2 

focused on understanding Spark DataFrames and how to safely explore large datasets.
I learned how Spark evaluates DataFrames lazily, the difference between show(), head(), and collect(), 
and why collecting large datasets to the driver can cause memory issues.
I also practiced filtering and selecting columns to inspect data efficiently without loading everything into memory.

Key Learnings 

Spark DataFrames are lazily evaluated
Data inspection should avoid collect() on large datasets
show() and limit() are safe for exploration
Schema awareness is important for correct filtering
