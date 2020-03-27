# NoSQL Concepts

## Philosophy

1. Schema on write, not on read.
1. Nested values are common and fields are not structured.

## Types

1. Document Store
    - In a structure like JSON.
    - Organized by collections
    - Documents can have unique structures.
    - Documents have specific keys
    - Can query a document by fields.
1. Key-Value Store
    - Queries by keys
    - Cannot query anything but the keys
    - Can define more than one key
    - Used for caching
1. BigTable/tabular
    - Named after Googles priorietary "BigTable" implementation
    - Rows can have different columns
    - Design for large number of columns
    - Rows are typically versioned
1. Graph
    - Designed for innterconnecte nodes.
1. Object
    - Persistence layer to OO
    - Link through pointers.

## Mechanics

1. Easily create web apps with customizable fields.
1. Used as caching layer
1. Stores as binary files
1. Serve full web apps

## Tradeoffs

1. Will not solve scalability.
1. Does have flexibility in reading.

## Tools of the trade

1. Queries
1. Indexes and Keys
1. JavaScript
1. JSON

## CouchDB

1. [Fauxton](http://127.0.0.1:5984/_utils)
1. [All dbs](http://127.0.0.1:5984/_all_dbs)
1. [All docs for db](http://127.0.0.1:5984/db/_all_docs)

### CouchDB Map

1. Map functions are used to only extract the data you need.
1. Design doc used for mapping to app.
    - Design documents contain views and all parts of the app through attachments.
1. Reduce functions are run on map function keys, once.
1. Use ``cradle`` as an NPM package to connect to it.

## Other Concepts
1. Partitions include
    1. Ranges: A-M M-Z
    1. List: types, etc.
    1. Hash: Determes membership
    1. Why?
        1. Storage limitations
        1. Performance
        1. Availability
1. Relational dbs can be partitioned horizontally or vertically
1. Horizontal partitions rows, Vertical partitions columns
1. Parititoning non-relational dbs depends on type.
1. CAP Theorem - Consistency, Availability, Partition Tolerance. Only two of the three.
    - Relational db trends toward consistency and availability
    - NoSQL trends toward parition-tolerance
    - CouchDB is AP (available and partition tolerant)

## CouchDB vs Others

1. MongoDB
    - Is consistent and partition tolerant.
    - Queries use drivers
    - Does not support views
    - Master/Slave replicas
    - Based on shards
    - Structured on dbs/collections/records
    - Map reduce functions
1. Cassandra
    - Invented by FB.
    - Available., partition tolerant with some config on consistency.
    - Queries use drives
    - KV and tabular
    - No downtime by adding nodes
    - Keys mapped to columns
    - CQL query language
1. Riak are similar to CouchDB
    - AP database
    - Bucket/key/value
    - Query syntax is close to Lucene
    - MapReduce functions.
1. Redis
    - Is consistent, partition-tolerant db.
    - Native drivers
    - KV store
    - Mac and Linux
    - Master/Slave
    - Query by key, and sometimes hash
        - lists, sets, hashes

## Trivia

1. Hashes are mostly associated with NoSQL databases.
1. When data is best represented as interconnected nodes, the NoSQL database type is a graph.
1. A couple of the ways you can use NoSQL include as a caching layer or to store binary files.
1. When you run CouchDB on your local computer, the Futon user interface comes up automatically.
1. Use ``sudo apt-get install couchdb`` to install CouchDB on Ubuntu.
1. ``_rev`` gets automatically added when adding fields to a newly created document.
1. ``[]`` is used to creating a field that is an array of values.
1. ``/db/_all_docs`` to the URL to get the records in the Student database.
1. Use JavaScript to query for data in CouchDB.
1. If there are four documents with the key of "abc", a reduce function will be called 1 time.
1. The db name, id of the document, and the name of the file makes up the url of the image.
1. ``if (doc._attachments.hasOwnProperty(key) && typeof(key) !== 'function')``
1. Horizontal partitioning puts different rows on different partitions.
1. CAP Theorem only guarantees two of the three attributes (consistent, available, partition-tolerant).
1. MongoDB has native drivers for each language.
1. Cassandra is available, and partition-tolerant.
1. You cannot query over HTTP with Redis.
