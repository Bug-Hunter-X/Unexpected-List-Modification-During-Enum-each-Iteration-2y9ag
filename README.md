# Elixir List Modification Bug
This repository demonstrates a common issue in Elixir when attempting to modify a list while iterating over it using `Enum.each`.  The provided code attempts to remove the element `3` from the list while iterating, but this doesn't work as expected because `Enum.each` does not modify the original list. The solution showcases alternative approaches to achieve the desired outcome.

## Bug Description
The bug arises from the misconception that modifying the list inside the `Enum.each` callback function will directly update the original list.  In Elixir, lists are immutable, and `List.delete` creates a new list. The original list remains unchanged, causing unexpected behavior.

## Solution
The solution demonstrates how to correctly remove elements from a list using functional approaches like `Enum.filter` or `List.delete/2` followed by reassignment of the list.