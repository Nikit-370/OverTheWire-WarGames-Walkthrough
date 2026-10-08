# Natas Level 24 → Level 25

## Topic

`strcmp()` type confusion

## Objective

Obtain the password required for the next Natas level.

## Solution

The application uses `strcmp()` to compare the supplied password.

The comparison assumes the input is a string, but PHP can receive an array instead.

Submit the parameter as an array, for example:

```text
passwd[]=anything
```

This causes the comparison to behave differently and bypass the intended check.

The lesson is that PHP functions can have surprising behavior when supplied with unexpected types.

## Key Concepts

This level is primarily about **`strcmp()` type confusion**.

## Next Level

After obtaining the password, log in as:

```text
natas25
```

and continue with [Level 25 → Level 26](level25.md) if that file exists.
