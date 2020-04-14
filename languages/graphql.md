# GraphQL

## Philosophy

Declarative data fetching from server to client.

## Benefits

1. Avoids multiple REST calls
1. Is backward compatible and version free
1. Can wrap around existing APIs
1. Is language agnostic

## Items

1. Invented by FB
1. Open Sourced in 2015
1. Has "graphiQL" interface

## Schema

1. Use *__schema* to query meta
1. Use *__type* to query meta
1. ! after type is **required**
1. Types associated are
    1. Integer
    1. Float
    1. String
    1. Boolean
    1. Null
    1. Enum
    1. List
    1. Object

## Aliases & Fragments

1. Use <name:> object for the alias.
1. Use ...fragmentName to spread in object query.

## Pagination

1. Use ```first: <num>``` and ```last: <num>``` in object parameters.

## Named Query and Variables

1. Use ```query <name>($param: type) { ... }```

## Mutations

Changes data guided by the schema. Considered PUT and DELETE.

1. ```mutation Function($input: <object>)```
