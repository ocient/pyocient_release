# pyocient Release Notes

## 1.0.9

- Add CSV output support
- Updated `cryptography` package dependency from `<3.4` to `<=36.0`
- Updated `cffi` and `google-auth` dependencies
- Improved decoding performance by caching the decoders
- Add formal STPoint, STLinestring and STPolygon classes rather than using tuples and lists
- Add support for `PRIORITY_ADJUSTMENT_FACTOR`, `PRIORITY_ADJUSTMENT_TIME`, `MIN_PRIORITY` and `MAX_PRIORITY` query settings.
- Handle invalid DNS names received from the database


## 1.0.7

- Fixed crash on invalid UTF-8 characters received from the database
- Fixed a bug in related to specifying the user through the `connect` API
- Standardized python code formatting

## 1.0.6

- Updated handling of the `force` option on connections to be more correct

## 1.0.5

- Added additional debug logging to connection redirecting

## 1.0.4

- Updated the redirect logic to be more correct

## 1.0.3

- Multiple host support added to the DSN
- `--tables`, `--systables`, and `--views` command line options removed
- Added support for the `source`, `connect to` and `set` commands
- Added support for starting without a DSN

pyocient release notes
