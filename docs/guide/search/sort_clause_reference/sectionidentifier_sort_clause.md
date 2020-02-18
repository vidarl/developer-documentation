# SectionIdentifier Sort Clause

The [`SectionIdentifier` Sort Clause](https://github.com/ezsystems/ezpublish-kernel/blob/6.13.7/eZ/Publish/API/Repository/Values/Content/Query/SortClause/SectionIdentifier.php)
sorts search results by the Section IDs of the Content items.

## Arguments

- `sortDirection` (optional) - Query or LocationQuery constant, either `Query::SORT_ASC` or `Query::SORT_DESC`.

!!! note

    Solr search engine uses the `Query::SORT_DESC` sort direction by default.

## Example

``` php
$query = new LocationQuery();
$query->sortClauses = [new SortClause\SectionIdentifier()];
```