# LocationId Criterion

The [`LocationId` Search Criterion](https://github.com/ezsystems/ezpublish-kernel/blob/v8.0.0-beta3/eZ/Publish/API/Repository/Values/Content/Query/Criterion/LocationId.php)
searches for content based in the Location ID.

## Arguments

- `value` - int(s) representing the Location ID(s).

## Example

``` php
$query->query = new Criterion\LocationId(62);
```
