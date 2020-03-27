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

## Trivia

1. Hashes are mostly associated with NoSQL databases.
1. When data is best represented as interconnected nodes, the NoSQL database type is a graph.
1. A couple of the ways you can use NoSQL include as a caching layer or to store binary files.
