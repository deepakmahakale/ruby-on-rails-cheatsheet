---
date: 2023-09-04
title: How to get random number in ruby?
categories:
  - basic
description: How to generate random numbers in ruby between a specified range.
type: Document
image: /images/og/how-to-generate-random-number-in-ruby.jpg
---

## Without an argument

Returns number between `0.0` - `1.0`, including `0.0` and excluding `1.0`.

```ruby
3.1.4 :001 > rand
#=> 0.43273184407039833
```

## With max limit

Returns a random integer greater than or equal to `0` and less than `max.to_i.abs`.

```ruby
3.1.4 :002 > rand(10)
#=> 4
```

## With a range

Returns a random integer number between the provided range including both the numbers.

```ruby
3.1.4 :003 > rand(1..10)
#=> 8
```
