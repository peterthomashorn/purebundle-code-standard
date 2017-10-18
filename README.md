# PureBundle Code Standard

More a formalized memo to myself than something I intended for wider adoption. I must admit: a few phrases are shamelessly copied from [PSR-1](http://www.php-fig.org/psr/psr-1/) and [PSR-2](http://www.php-fig.org/psr/psr-2/).

The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

## Files

* Files MUST use only UTF-8 without BOM.
* All PureBasic files MUST use the Unix LF (linefeed) line ending.
* Files SHOULD either declare symbols (procedures, constants, etc.) or cause side-effects (e.g. generate output, change files, etc.) but SHOULD NOT do both. Side effects means execution of code not directly related to declaring procedures, constants or similar.

## Line Length

* There MUST NOT be a hard limit on line length; the soft limit MUST be 120 characters; lines SHOULD be 80 characters or less.
* There MUST NOT be trailing whitespace at the end of non-blank lines.
* Blank lines MAY be added to improve readability and to indicate related blocks of code.
* There MUST NOT be more than one statement per line.

## Indentation

* Code MUST use **four spaces** for a level of indentation, not tabs. Generally, maintaining low levels of indentation is an indicator for good code style. But combined with descriptive naming and high indentation levels it can get absurd fast. Four spaces is enough to make the document outline readable.
* Each keyword for control flow MUST increase the level of indentation in the line after.

## Empty Lines

* There MUST always be an empty line before opening control keywords like `If`, `Select` or `Repeat`.
* There MUST always be an empty line after closing control keywords like `EndIf`, `EndSelect` or `ForEver`.

## Naming Things

* PureBasic Code Files MUST be named in `StudlyCaps`.

### Variables

* Variables MUST be declared in `StudlyCaps`.
* Variable names MUST NOT use type prefixes.
* Do not append the `.i` suffix in variable declarations because it is the default type anyway.
* When defining string variables, use the `.s` suffix instead of `$` for the sake of consistency. All other types are declared that way.

### Procedures

* Procedures MUST be declared in `StudlyCaps`.
* Procedures SHOULD consist of a verb and a noun to describe what they do. In example: `ReadFile` or `FreeMemory`.
* In the parameter list, there MUST NOT be a space before each comma, and there MUST be one space after each comma.
* When making a procedure call, there MUST NOT be a space between the procedure name and the opening parenthesis, there MUST NOT be a space after the opening parenthesis, and there MUST NOT be a space before the closing parenthesis. In the parameter list, there MUST NOT be a space before each comma, and there MUST be one space after each comma.

## Constants

* Constants MUST be declared in `StudlyCaps`.
* Constants MAY use underscores to separate words in their names.

## Enumerations

* Constants declared in enumeration blocks should be grouped in separate enumeration blocks based on their semantic correlation. In example: Enumeration of identifiers for application windows should happen in a different block than enumeration of identifiers for the gadgets.
