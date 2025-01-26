# JavaScript Type Coercion Bug

This repository demonstrates a common yet subtle bug in JavaScript related to type coercion and null checks. The code uses strict equality (`===`) to check for null values, but this can lead to unexpected behavior when dealing with other falsy values.

## Bug Description

The `foo` function intends to check for null inputs and return null if either `a` or `b` is null; otherwise, it adds `a` and `b`. However, the strict equality check doesn't consider cases where `a` or `b` might be 0 or an empty string, resulting in an incorrect calculation in those situations.

## Bug Solution

The solution modifies the null check to explicitly handle null values using loose comparison (`==`) or by checking for null and undefined separately. This ensures a proper check for null and avoids unexpected behavior due to type coercion.