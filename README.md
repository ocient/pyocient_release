# Pyocient Release Notes

## 1.0.12
- Added `--nohistory` command-line option. The history file does not store commands from the session.
- Added `ignorespace` option to command-line history. The history file omits lines that begin with a white space character.

## 1.0.11
- Added a link to the release notes to the package description

## 1.0.10

- Fixed error in the parameter substitution docstring.
- Added support for `SERVICECLASS`, `ADJUSTFACTOR`, `ADJUSTTIME`, and `PSO` query settings.
- Added support for the `SHOW` command.
- Added support for the `CANCEL TASK` command.
- Removed support for `PRIORITY_ADJUSTMENT_FACTOR`, `PRIORITY_ADJUSTMENT_TIME`, `MIN_PRIORITY`, and `MAX_PRIORITY` query settings.
- Deprecate support for the `CHECK DATA` command
- Fixed output of binary types at the command line.

## 1.0.9

- Added CSV output support
- Updated `cryptography` package dependency from `<3.4` to `<=36.0`
- Updated `cffi` and `google-auth` dependencies
- Improved decoding performance by caching the decoders
- Added formal STPoint, STLinestring, and STPolygon classes rather than using tuples and lists
- Added support for `PRIORITY_ADJUSTMENT_FACTOR`, `PRIORITY_ADJUSTMENT_TIME`, `MIN_PRIORITY`, and `MAX_PRIORITY` query settings.
- Enabled the handling of invalid DNS names received from the database


## 1.0.7

- Fixed crash on invalid UTF-8 characters received from the database
- Fixed a bug related to specifying the user through the `connect` API
- Standardized Python(R) code formatting

## 1.0.6

- Updated handling of the `force` option on connections for accuracy

## 1.0.5

- Added additional debug logging to the redirection of connection 

## 1.0.4

- Updated the redirect logic for accuracy

## 1.0.3

- Added multiple host support to the DSN
- Removed `--tables`, `--systables`, and `--views` command-line options
- Added support for the `source`, `connect to`, and `set` commands
- Added support for starting without a DSN
