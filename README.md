# Pyocient Release Notes

## 3.3.2

- Fixed ending SSO sessions when you close the connection.

## 3.3.0

- Pinned the cryptography package to a version earlier than 42.0.0 for stability purposes.
- Added OIDC single sign on (SSO).
- Added the `performance mode` command.
- Enabled the display of nulls as NULL when using the table format.
- Set the command-line default fetch size to 30000.
- Fixed the implementation of the `set serviceclass` command.
- Changed `pyocient.Warning` to be a subclass of the Python `Warning` class.
- Added the `set printuuid on` command.
- Added the `--version` option at the command line.
- Set the TCP `keepalive` options on connections.
- Added a valid error message when the system rejects a connection without SSL encryption.

## 3.0.3

- The `TypeCodes` class has been changed to a Python® `IntEnum`.
- GIS types \_STPoint, \_STLinestring, and \_STPolygon have been renamed to STPoint, STLinestring, and STPolygon, respectively.
- The `user` and `password` fields have been removed from the `Connection` object. This object no longer stores these fields.
- You can pass the `security_token` from another connection to the `connect` function.
- The `Session` object has been removed.
- The `custom_type_to_json` function has been moved into the pyocient API to allow the consistent conversion of the result set to the JSON format.
- The `patch` portion of the pyocient version is sent to and logged in the database.
- The `--nooutput` command-line parameter does not throw a Python exception.
- The `local variable 'return_code' referenced before assignment` error has been fixed.
- Added the `--rows` argument to the command-line program to load the result set in batches.

## 2.0.0

- Packaging has been significantly refactored to match Python® packaging standards.
- Python context manager support has been added to connections and cursors.
- Python type annotations have been added to the pyocient API.
- Fixed the command-line interface (CLI) to return a non-zero code for statements that fail.
- CLI output has been standardized to either go to the output file or standard output (stdout).
- The option to echo statements has been added as a command-line option.
- The `pyocient.SyntaxError` exception, which conflicted with the built-in Python `SyntaxException`, has been removed.
- `pyocient.version` has been removed in favor of the more standard `pyocient.__version__`.

## 1.0.15

- The dependency on protobuf has been upgraded from `>=3.12.0,<=3.19.1` to `>=3.20.0,<=4.22.0`.
- Fixed an error that occurs when you do not specify the host parameter in the `connect()` api.

## 1.0.14

- Updated pyocient dependencies to eliminate some unused dependencies and tighten
  the dependencies on protobuf and dsnparse.

## 1.0.13

- Fixed bug that left `Cursor.rowcount` unset after Data Manipulation Language (DML) query execution.
- The `cryptography` package requirement of version 36 or lower is no longer required.

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
