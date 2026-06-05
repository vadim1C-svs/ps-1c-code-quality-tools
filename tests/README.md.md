# Code Review Test Cases

## Test Case 1 — Query inside loop

### Input

1C code contains a database query inside a loop.

### Expected result

The review should detect a performance risk and recommend replacing multiple queries with one query using `В (&СписокЗначений)`.

### Severity

High