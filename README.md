Make a language agnostic documentation generator in the style of jsdoc.

Mainly for shell, because shdoc doesn't work all that well for me.

Make tags work everywhere, not just above functions.

Implement the following tags (the `@` might change to something else)

- @type {int|float|string|path|file|array|constant|global|export|function|void} name
    - each type can also be its own tag, eg `@constant name`
      instead of `@type {constant} name`
- @name value
- @arg {type} name
- @err message
- @return {type} value
- @modifies {type} name
- @imported description
- @requires name
- @ignore

Structure documentation using the following tags. Structural tags are processed in
the order they appear in the source code.

- @introduction text
- @section name
- @description text
  - can be used anywhere, not just atop functions
- @example sample code
- @important message
- @reference [title|url]
- @definition term definition

```
reference other functions / pages in the current docset
@reference [title|internal_url]
```

- @link

```
@link [title|url]
```

- @table name

```
@table test table
Name|Amount|Value
star,15,$450
planet,8,$100
asteroid,2,$700
```

Metadata can be added using the @meta tag followed by a key/value pair.
No duplicate keys, only the first value is valid for two keys with the same name

```
@meta author|alvin charity
@meta created|2023-04-21
```
