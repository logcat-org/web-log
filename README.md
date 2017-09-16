# Prefix Compression [Hackerrank](https://www.hackerrank.com/challenges/prefix-compression/problem)

## Description
You are in charge of data transfer between two Data Centers. Each set of data is represented by a pair of strings. Over a period of time you have observed a trend: most of the times both strings share some prefix. You want to utilize this observation to design a data compression algorithm which will be used to reduce amount of data to be transferred.
You are given two strings x and y, representing the data, you need to find the longest common prefix (p) of the two strings. Then you will send substring p, x1 and y1 where x1 and y1 are the substring left after stripping p from them.

## Example
If  "abcdefpr" and  "abcpqr", then  "abc",  "defpr",  "pqr".

## Algorithm

```elixir
defmodule Prefix do
  def takeFirst(prefix, [x | a], [y | b]) when x == y do
    takeFirst([x | prefix], a, b)
  end

  def takeFirst(prefix, a, b) do
    [prefix, a, b]
  end
end
```
