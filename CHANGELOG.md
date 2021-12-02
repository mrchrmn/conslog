# Change Log

## [1.6.6]
- Works with TypeScript now.

## [1.6.1]
- Minor change to "_Log variable_": properly logs objects now.  

## [1.6.0]
- Added basic _Wrap single console.log around selection_ which can wrap multiple lines. 

## [1.5.5]
- Minor change to "_Log variable_" formatting: removed the unnecessary indent.

## [1.5.4]
- Ahem... removed configuration default as it broke "_Log console_".

## [1.5.2]
- Added configuration default: code suggestions are now automatically available in JavaScript snippets to make "_Log variable_" more useful.

## [1.5.0]
- Change: "_Log selection_" now always adds semicolon after `console.log`. 
- Fix: "_Log selection_" can now handle `/` in the code.
- New features (or work-arounds?) to deal with problematic edge cases (see documentation for details):
  - "_Log lines to last semicolon_" 
  - "_Log lines to last closing bracket_"

## [1.4.0]
- New feature: Added "_Log variable_".
- Change: Renamed "_Clear console.logs_" to "_Delete console.logs_" and changed the prefix to `dcl`.
- Fix: "_Log selection_" and "_Delete console.logs_" work with CRLF as end of line sequence.

## [1.3.3]
- Small improvement to "_Log selection_": Comment lines in selection do no longer get logged.

## [1.3.0]

- Added "_Undo log selection_"
- Small improvement to "_Log selection_": Empty lines in selection do no longer get empty console.logs.

## [1.2.0]

- Added "_Clear console.logs_" feature.

## [1.1.0]

- Works across multiple lines now.

## [1.0.0]

- Initial release