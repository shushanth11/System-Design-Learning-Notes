# Redis — Complete Deep-Dive Study Notes

A comprehensive Redis study guide covering computer memory, Redis internals, request processing, data structures, concurrency, persistence, caching, clustering, scaling, and production architecture.

---

## 1. What Exactly Is Redis?

**Redis (Remote Dictionary Server)** is an in-memory data store that can be used as:

* Cache
* Key-value database
* Message broker
* Pub/Sub system
* Queue
* Session store
* Distributed counter
* Distributed coordination/locking mechanism
* Real-time data store
* Stream/event-processing system

The simplest Redis model is:

```text
KEY → VALUE

user:1001 → "Alice"
```

Redis also provides specialized data structures:

* String
* Hash
* List
* Set
* Sorted Set
* Stream
* Bitmap
* HyperLogLog
* Geospatial

The central idea:

> Keep frequently accessed data in memory and provide highly optimized operations on that data.

---

## 2. Why Was Redis Created?

Traditional databases solve a broad set of problems:

* Tables
* Rows
* Columns
* Indexes
* SQL
* JOINs
* Transactions
* Constraints
* Foreign keys
* MVCC
* Isolation
* Durability
* Query optimization

But many application operations are much simpler:

```text
Give me the value for this key.
```

For example:

```text
GET user:123
```

Or:

```text
Increment this counter.
```

Redis is optimized around these kinds of operations.

---

## 3. The First Misconception: "Redis Is Fast Because RAM Is Fast"

This statement is incomplete.

Redis performance comes from multiple factors:

```text
Red
```
