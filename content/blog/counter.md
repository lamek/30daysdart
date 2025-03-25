---
title: Counter
description: Return a counter function
date: 2025-03-25
tags: closures
---

This problem is from LeetCode's [30 Days of JavaScript](https://leetcode.com/studyplan/30-days-of-javascript/)
path. This version is for dart.

## Problem

Description of problem

## Solution

```dart
void main() {
  // Example 1 Test
  int n1 = 10;
  Counter counter1 = createCounter(n1);
  assert(counter1() == 10);
  assert(counter1() == 11);
  assert(counter1() == 12);
  print('Example 1 tests passed');

  // Example 2 Test
  int n2 = -2;
  Counter counter2 = createCounter(n2);
  assert(counter2() == -2);
  assert(counter2() == -1);
  assert(counter2() == 0);
  print('Example 2 tests passed');

  print('All tests passed successfully!');
}

typedef Counter = int Function();

Counter createCounter(int n) {
  int currentCount = n;
  return () {
    int valueToReturn = currentCount;
    currentCount++;
    return valueToReturn;
  };
}
```