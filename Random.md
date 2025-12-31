You can't understand your SQL query performance by looking at the SQL code. You need the execution plan. 

Take the SQL : 

select id from student where grade >= 99 

It doesn’t tell you how fast it will run.

If there isn’t an index on the grade column, it will do a full table scan taking multiple seconds depends on how many rows it returns.

Add an index on the grade field, run the same query now it takes few seconds 

Make it a covering index (add id as included column to the grade index) and now it’s an index only scan even faster.

Insert a million students into the table and re execute the query immediately (don’t give a chance for MVCC garbage collection to run) and the query will slow down again, because we need to go to the heap to see if the row is visible.

In all the four examples above the backend app code running the query didn’t change, same code, same query.

However, the performance of the query varies every time based on the state of the database.

The execution plan tells us what how the SQL was executed in each of those four examples. It is the key.
