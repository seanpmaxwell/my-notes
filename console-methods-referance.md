## JavaScript `console` Object — Methods Reference

| Method | Description | Environment |
|---|---|---|
| `console.log()` | General-purpose output for messages, variables, or objects. | Universal |
| `console.info()` | Informational message; functionally identical to `log()` in most browsers, sometimes styled differently. | Universal |
| `console.warn()` | Displays a warning, usually with a yellow highlight/icon in dev tools. | Universal |
| `console.error()` | Displays an error, usually with a red highlight/icon and a stack trace. | Universal |
| `console.debug()` | Debug-level message; behaves like `log()` in most environments, may be hidden by default in some. | Universal |
| `console.trace()` | Prints the current call stack, showing the chain of function calls that led to this point. | Universal |
| `console.assert()` | Logs an error message only if the given assertion (first argument) is falsy; does nothing if truthy. | Universal |
| `console.table()` | Displays tabular data (arrays/objects) as a formatted table. | Universal |
| `console.dir()` | Displays an interactive list of an object's properties, useful for DOM elements (shows object structure rather than HTML). | Universal |
| `console.dirxml()` | Displays an XML/HTML representation of a node, if possible; falls back to `dir()`-style output otherwise. | Browser only |
| `console.group()` | Starts a new, expandable/collapsible group of console output, indenting subsequent logs. | Universal |
| `console.groupCollapsed()` | Same as `group()`, but the group starts collapsed by default (in Node, behaves like `group()` since there's no collapsing UI). | Universal |
| `console.groupEnd()` | Closes the most recently opened group. | Universal |
| `console.count()` | Logs the number of times `count()` has been called with a given label. | Universal |
| `console.countReset()` | Resets the counter for a given label used with `count()`. | Universal |
| `console.time()` | Starts a timer with a given label, for measuring how long an operation takes. | Universal |
| `console.timeLog()` | Logs the current elapsed time for a timer started with `time()`, without stopping it. | Universal |
| `console.timeEnd()` | Stops a timer started with `time()` and logs the total elapsed time. | Universal |
| `console.timeStamp()` | Adds a marker to the browser's Performance/Timeline tool (mainly for performance recording, not console output). | Browser only |
| `console.clear()` | Clears all output from the console (clears the terminal in Node if it's a TTY). | Universal |
| `console.profile()` | Starts a JavaScript CPU profile (in supporting dev tools) under a given label. | Browser only |
| `console.profileEnd()` | Stops a CPU profile started with `profile()`. | Browser only |
| `console.exception()` | Deprecated, non-standard alias for `console.error()`; logs an error message with a stack trace. | Browser only |
| `console.memory` | (Property, not a method) Non-standard, Chrome-only — reports heap size/memory usage info. | Browser only |

**Notes:**
- "Universal" means available in modern browsers (Chrome/Firefox/Safari) and Node.js, though exact formatting/output styling can differ between them.
- Node.js writes `error()`, `warn()`, and `trace()` to `stderr`, while the rest go to `stdout` — browsers don't distinguish streams this way.
- A few methods (`profile`, `profileEnd`, `timeStamp`, `memory`, `exception`, `dirxml`) are non-standard or DevTools-specific and won't exist in Node.
