Cassandra Pitfalls
=========

**Cassandra schema:**

  When choosing creating a table in cassandra the selection of a primary key there is more to think about than just whether or not the key is unique.  If the keys in a cassandra table are not carefully chosen then it may be slow or impossible to perform the kinds of queries that the user wants.  

http://www.datastax.com/dev/blog/a-deep-look-to-the-cql-where-clause

A simple example that we ran into involved our tweets.  Originally we set up our tables that contained tweets for each of the presidential candidates with the primary key as “PRIMARY KEY (tweet_id, created_at)”.  This was a unique primary key but in order to run a query that got the tweets in the table for a range of time we needed to add a statement at the end of our query that said “ALLOW FILTERING”.

  Using the ALLOW filtering statement in cassandra is sometimes necessary when performing queries in cassandra but it should be avoided whenever possible.  Allow filtering works but retrieving every row in a table and then filtering out the values that don’t apply to your query.  So every time you query a range of one hour or even one minute of time you would be pulling the entire table into memory and looking at every entry in the table.  

  In the 2016 election Donald Trump received a large number of tweets.  So many in fact that we reached the point where running a query with ‘allow filtering’ on his table crashed our database because it took more memory than we had.

  The fix for this was simple.  We changed our primary key structure to...
PRIMARY KEY (candidate, created_at, tweet_id)
    The first key from left to right in a primary key in cassandra is called the partition key.  The partition key determines which partition in the cassandra cluster the data is stored on.  A consequence of this is this is that if you cannot run a ranged query on the partition key.

  For example if our primary key has been PRIMARY KEY (created_at, tweet_id)
  We would not be able to query on a range of created_at times.

  But with the candidate’s name included we could now run a query like
SELECT * from candidate where name = ‘sanders’ and created_at > 20160425000000
Where the created_at field is formatted as YYYYMMDDHHMMSS.

http://www.datastax.com/dev/blog/allow-filtering-explained-2
“The only way Cassandra can execute this query is by retrieving all the rows from the table blogs and then by filtering out the ones which do not have the requested value for the time1 column.

If your table contains for example a 1 million rows and 95% of them have the requested value for the time1 column, the query will still be relatively efficient and you should use ALLOW FILTERING.

On the other hand, if your table contains 1 million rows and only 2 rows contain the requested value for the time1 column, your query is extremely inefficient. Cassandra will load 999, 998 rows for nothing. If the query is often used, it is probably better to add an index on the time1 column.”

http://docs.datastax.com/en/cql/3.1/cql/cql_reference/copy_r.html?scroll=reference_ds_mh1_1hs_xj__specifying-the-source-or-destination-files
