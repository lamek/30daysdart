---
title: Create Hello World Function
description: This is a post on My Blog about agile frameworks.
date: 2025-03-25
tags: closures
---


This is a walkthrough of LeetCode's "Create Hello World Function" from the [30 Days of JavaScript]()
path. This version is for dart.

## Problem

Description of problem

## Solution

```dart
void main() {
  dynamic createHelloWorld() {
    return () {
      return "Hello World";
    };
  }

  // Test cases
  bool runTest(dynamic Function() testFunction, String expectedOutput, String testName) {
    var result = testFunction();
    print("$testName: Expected '$expectedOutput', Got '$result'");
    return result == expectedOutput;
  }

  var f1 = createHelloWorld();
  bool test1Passed = runTest(f1, "Hello World", "Test Case 1");

  var f2 = createHelloWorld();
  bool test2Passed = runTest(() => f2({}, null, 42), "Hello World", "Test Case 2");

  // Check if all tests passed
  if (test1Passed && test2Passed) {
    print("\n🎉 All tests passed successfully! 🎉");
  } else {
    print("\n❌ Some tests failed.");
  }
}
```