# Interface

This projects serves two REST resources:

- Book resource by library-shelf : basic CRUD functionality over the Book entity.
- Stat resource by library-stats : only one GET endpoint is available (`/api/stat`)
    
Both resource is available in Swagger UI with param descriptions and example values, for more information check [usage](docs/usage.md).

## More info about stat resource

A stat can provide information about different types of objects:

- an author
- a publisher
- the whole library (global stat)

The exact information which is provided by the stat is called "statType".

Example stat type: COUNT_BY_AUTHOR. Its stat object type is author, and it will return the count of all books by a given author in the library.
