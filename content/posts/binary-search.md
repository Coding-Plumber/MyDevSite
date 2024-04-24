---
author: "Kyle McAndrew"
title: "Binary Search"
date: "2024-04-22"
tags:
  - DSA
  - algorithms
---

I've been learning algorithms for a while and it's part of my constant learning goal for the year and i have commited to atleast 100 posts on this page so this next one i have done on binary search.

Ever searched through a massive phone book for a name starting with 'K'? Yeah probably not if your still in your 20's! Anyway you’ll have to imagine it. Instead of starting at the beginning, you'd likely flip to the middle. This is the essence of a binary search.

We keep halving the data until we find our target. If we land on 'L', we know 'K' must be to the left, instantly discarding half the phone book. We halve again, find our section, and bam! – only 25% of the original data remains after just two steps. Compare this to a linear search, where you'd check every name, potentially going through the entire phone book.

<br>

Think of it like a number guessing game with numbers 1 to 10.

![10 sorted ints](/images/1to10.png)

To minimize guesses, you start with 5 or 6

![5 sorted ints](/images/1to5.png)

instantly reducing the possibilities by half. Say your next guess is 3, and I say "lower." You now only have to worry about 1-3.

![3 sorted ints](/images/1to3.png)

One more guess (2), and you nail it.

![2 is king](/images/2withcrown.png)

It took 4 guesses for 10 numbers, which might seem unimpressive. But scale it up:

- 100 numbers: 7 guesses
- 1000 numbers: 10 guesses
- 100,000 numbers: Only 17 guesses!

Notice how even doubling the input (100,000 to 200,000) only needs one extra guess! A linear search gets linearly slower as the input grows.

This efficiency is expressed in Big O notation:

- Binary search: O(log n) - logarithmic growth
- Linear search: O(n) – growth directly tied to input size

<br>

### Brief explanation on logarithms...

This is taken from a book i'm working through called 'Grokking algorithms' by Aditya Y. Bhargava which i would recommend if DSA interests you and you don't know where to start.

You may not remember what logarithms are, but you probably know what exponentials are. log10 100 is like asking “How many 10s do we multiply together to get 100?” The answer is 2: 10 x 10. So log10 100 = 2. Logs are the inverse of exponentials.

10² = 100 ↔ log10 100 = 2  
10³ = 1000 ↔ log10 1000 = 3  
2³ = 8↔ log2 8= 3  
2⁴ = 16 ↔ log2 16 = 4  
2⁵ = 32 ↔ log2 32 = 5

**Logs are the inverse of exponentials.**

<br>

### Worst-case scenario is what matters

Worst-case scenario is what matters in Big O notation, for example if n = 100 there are 100 possibilities and there is nothing stopping us finding it on attempt 1 of 100 and that iteration would in theory be O(1) however we use worst case to determine speeds but it is occasionally possible for a O(n) to out perform a O(log n).

Binary search can only be used on sorted data because of the nature of how it searches so there is added time complexities behind the scenes for sorting the data that should be accounted for.

<br>

### Some real-world use cases for binary search:

- Databases and range queries
- Isolating faults in a complex system, by testing the midpoint of a process it can eliminate half very quickly.
- The ‘middle out’ compression algorithm by Pied Piper 👀 ...Ok, I’m sure it would have been.
