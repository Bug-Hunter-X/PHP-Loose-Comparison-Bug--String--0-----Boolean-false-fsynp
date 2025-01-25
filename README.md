# PHP Loose Comparison Bug

This repository demonstrates a subtle but important bug in PHP related to loose comparison (`==`) of strings and booleans.  Specifically, the string '0' is considered equal to the boolean `false` when using loose comparison.

## The Bug

PHP's type juggling can lead to unexpected results when using loose comparison.  The example script shows that '0' (string) and `false` (boolean) are considered equal when compared with `==` because PHP converts `false` to the integer 0 during comparison.

Strict comparison (`===`) is recommended to prevent these issues.

## How to Reproduce

1. Clone this repository.
2. Run `bug.php` using a PHP interpreter.

## Solution

The solution file (`bugSolution.php`) shows how to correct this by using strict comparison (`===`).