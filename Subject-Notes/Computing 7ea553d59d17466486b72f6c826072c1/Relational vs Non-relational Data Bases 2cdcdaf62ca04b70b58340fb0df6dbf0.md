# Relational vs Non-relational Data Bases

# What are relational Data Bases

- Relational data bases, also called Relational Database Management Systems (RDBMS) or most commonly known as an SQL database. Some popular ones are, Microsoft SQL, MySQL etc.
- They are mostly used in large enterprise scenarios, but MySQL can also be used to store data for Web Applications

# Main Differences Between Relational and Non-Relational Databases

## Relational Databases

### Pros

- Work with structured data
- They support ACID (atomicty, consistency, isolation and durability, which leaves the database in a valid state) transactional consistency. And supports joins ( a command clause that combines records from two or more tables in a database. It is a means of combining data in fields from two tables by using values common to each table).
- They come with built-in data integrity and a large eco-system.
    
    [Data Integrity](Data%20Integrity%20108b7c5a9ed080218253c7f68c5570c0.md)
    
- Relationships in this system have constraints
- There is limitless indexing. Strong SQL.

### Cons

- Relational Databases don't scale out horizontally very well (concurrency and data size), only vertically.
- Data is normalized, meaning lots of joins, which affects speed.
- They have problems working with semi-structured data. (doesn't follow the tabular structure associated with relational databases or other forms of data tables).

## Non-relational/NoSQL

### Pros

- They scale out horizontally and work with unstructured and semi-structured data. Some support ACID transactional consistency.
- Schema-free or Schema-on-read options (all data is stored in JSON-style documents that can have different fields with different data types in each one).
- High availability
- While many NoSQL databases are open source and so “free”, there are often considerable training, setup, and developments costs. There are now also numerous commercial products available.

### Cons

- Weaker or eventual consistency (BASE) instead of ACID.
- Limited support for joins.
- Data is de normalized, requiring mass updates (i.e. product name change).
- Does not have built-in data integrity (must do in code).
- Limited indexing.

# When to Choose NoSQL

- When bringing in new data with a lot of volume and/or variety.
- Data is non-relational/semi-structured.
- Your team will be trained in these new technologies (NoSQL).
- You have enough information to correctly select the type and product of NoSQL for your situation.
- You can relax transactional consistency when scalability or performance is more important.
- You can service a large number of user requests vs rigorously enforcing business rules.