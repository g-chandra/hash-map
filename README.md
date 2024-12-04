# hash-map

Hash Table is a data structure which organizes data using hash functions in order to support quick insertion and search. 
In this article, we will take a look at the principle of the hash table.

The key idea of Hash Table is to use a hash function to map keys to buckets. To be more specific,

When we insert a new key, the hash function will decide which bucket the key should be assigned and the key will be stored in the corresponding bucket;
When we want to search for a key, the hash table will use the same hash function to find the corresponding bucket and search only in the specific bucket.
 

An Example
| key     | Hash Function | Bucket |
| --------|---------------|--------|
| 0       | f(n)          | 0    |
| 1987    | f(n)          | 2    |
| 24      | f(n)          | 4    |
| 2       | f(n)          | 2    |


In the example, we use y = x % 5 as our hash function. Let's go through the insertion and search strategies using this example:

**Insertion**: we parse the keys through the hash function to map them into the corresponding bucket.
e.g. 1987 is assigned to bucket 2 while 24 is assigned to bucket 4.

**Search**: we parse the keys through the same hash function and search only in the specific bucket.
e.g. if we search for 1987, we will use the same hash function to map 1987 to 2. So we search in bucket 2 and we successfully find out 1987 in that bucket.
e.g. if we search for 23, will map 23 to 3 and search in bucket 3. And We find out that 23 is not in bucket 3 which means 23 is not in the hash table.
