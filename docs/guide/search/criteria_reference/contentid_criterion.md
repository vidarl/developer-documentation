# ContentId Criterion

The [`ContentId` Search Criterion](https://github.com/ezsystems/ezpublish-kernel/blob/v8.0.0-beta3/eZ/Publish/API/Repository/Values/Content/Query/Criterion/ContentId.php)
searches for content by its ID.

## Arguments

- `value` - int(s) representing the Content ID(s).

## Example

``` php
$query->query = new Criterion\ContentId([62, 64]);
```
