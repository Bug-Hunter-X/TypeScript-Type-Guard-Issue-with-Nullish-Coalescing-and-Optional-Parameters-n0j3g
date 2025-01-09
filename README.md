# TypeScript Type Guard Issue with Nullish Coalescing and Optional Parameters

This repository demonstrates a subtle bug in TypeScript related to type guards and optional parameters.  The `greet` function is designed to handle null values gracefully, but it throws a runtime error when an undefined value is passed.

## Problem

The issue arises because TypeScript's type guards may not perfectly handle undefined values when dealing with optional parameters or nullish coalescing.  In this particular case, the compiler doesn't fully recognize that undefined should be treated like null in the context of this function's signature and logic.

## Solution

A solution is provided to explicitly check for both null and undefined values.