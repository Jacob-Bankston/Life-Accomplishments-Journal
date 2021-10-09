# DUNGEONS, DRAGONS, AND GRAPH DATABASES

## GUY ROYSE

[Slide Deck](https://github.com/guyroyse/dnd-and-graph-databases/tree/main/slides)

Developer Advocate @ Redis
@guyroyse
github.com/guyroyse
guy.dev

"Miro for Lean Coffee"

Graph Database - Instead of using tables and rows and columns, I can use nodes and information

GraphQL is a protocol for making requests over HTTP

Graph Database would pair really well with a GraphQL, but they are not the same thing

## What's a Graph Database

A graph is a series of vertices and edges

- This node is connected to this node
- This edge is connected to these vertices

- null graph - nothing
- relationships - connections between nodes
- directed nodes - have relationships where data gets sent to or connected to
- undirected nodes - do not have relationships where data gets sent
- degrees - the number of relationships that a node has
- in degree - the number of relationships that are incoming
- out degree - the number of relationships that are outgoing
- NOTE - anything can connect to anything! any node, itself, etc...

#### A Graph Database is taking this structure of database and layering data on top of it

## Info on Nodes and Relationships

nodes (key value pairs)

- represent items
  - can have labels
  - can have attributes
- can stand alone

:Room
id: 3
name: 'Armoury'

NOTE - If you get rid of a node, then you get rid of all of it's relationships as well

relationships

- represent connections
  - connect two nodes
  - have a type
  - have a direction
  - can have attributes
- cannot exist without nodes to connect

:Room -> :Contains -> :Monster

## Table Talk

Compare SQL to Cypher

SQL

- SELECT
  - r.id, r.name, t.id, t.name, t.gp m.id,

Cypher

- parenthesis matches a node
- square brackets matches a relationship
- `(r:Room) - [c:CONTAINS] -> (m:Monster)`

SQL

```sql
SELECT id, name
FROM Rooms
WHERE id = 1;
```

CYPHER

```
MATCH (r:Room)
WHERE r.id = 1
RETURN r
```

SQL

```sql
UPDATE Rooms
SET name = 'Statue Hall'
WHERE id = 1;
```

Cypher

```sql
MATCH (r:Room)
WHERE r.id = 1
UPDATE r.name = 'Statue Hall'

DELETE FROM Rooms
WHERE id = 1;

MATCH (r:Room)
WHERE r.id = 1
DELETE r

MATCH (r:Room) WHERE r.id = 1

MATCH (r:Room { id: 1 })

CREATE (:Room {
  id: 1, name: 'Statue Room'
})
```

In relational database you have to set up a one-to-many relationship
In a Graph database, you would set up a relationship like this!

```sql
MATCH (r:Room {id:1})
MATCH (m:Monster {id:4})
CREATE (r) - [:CONTAINS] -> (m)
```

To get the relationships and all the information in a Relational Database, you need to do a join
In a Graph database this is the code

```sql
MATCH (r:Room) - [:CONTAINS] -> (m:Monster)
RETURN r.id, r.name, m.xp
ORDER BY m.xp DESC
```

In order to create a relationship between two rooms in the same table, you need to make an additional table to show the relationships between the tables. Querying to this will get complicated really quick.

```sql
MATCH (r1:Room {id:1})
MATCH (r2:Room {id:2})
CREATE (r1) - [:LEADS_TO] -> (r2)
```

finding paths within your graph database

```sql
(r1:Room) -  [:LEADS_TO*] -> (r2: Room)
```

The asterisk - matches multiple leads_to relationships

```sql
(r1:Room) -  [:LEADS_TO*1..3] -> (r2: Room)
```

The numbers after the asterisk will limit from the minimum hops to maximum hops

- Find the longest path through the dungeon
- The room with the biggest treasure
- The path to the gold

[Total Code Repo](https://github.com/guyroyse/dnd-and-graph-databases)
